# 训练命令，从命令行进入所在文件运行
python run_classifier.py --task_name=mytask --do_train=true --do_eval=true --data_dir=data --vocab_file=chinese_L-12_H-768_A-12\vocab.txt --bert_config_file=chinese_L-12_H-768_A-12\bert_config.json --init_checkpoint=chinese_L-12_H-768_A-12\bert_model.ckpt --max_seq_length=128 --train_batch_size=32 --learning_rate=1e-5 --num_train_epochs=3.0 --output_dir=output
# 测试命令
python run_classifier.py --task_name=mytask --do_predict=true --data_dir=data --vocab_file=chinese_L-12_H-768_A-12\vocab.txt --bert_config_file=chinese_L-12_H-768_A-12\bert_config.json --init_checkpoint=output --max_seq_length=128 --output_dir=output
