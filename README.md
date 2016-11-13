# exp_manager
 exp_manager comes from parent project: tools

###实验服务类，支持优雅的实验管理和日志定制

	        with ExpManager("Mock") as (exp, logger):
	   
           	    from collections import OrderedDict
           	    user_info = OrderedDict(user_id=1, account_id=123, campaign_id=1234)
           	    if exp and exp.has_user(user_info):
               		# main logic
               		print 'user exists in exp'
               		logger.debug('user_id[%d] account_id[%d] campaign_id[%d] participate exp' % tuple(user_info.values()))
		        else:
               		print 'user not exists in exp'
               		logger.debug('user_id[%d] account_id[%d] campaign_id[%d] dont participate exp' % tuple(user_info.values()))     
###运行/测试

          python exp_manager.py
          python test_exp_manager.py
