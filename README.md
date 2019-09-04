# uniapp_test_fields
uniapp_test_fields
复现步骤
[复现问题的步骤]
1,复制下面代码到某个组件的methods
2,组件加载的时候调用该方法
3,在支付宝小程序运行该组件

[或者可以直接贴源代码]
let view = uni.createSelectorQuery().select("#sss");
view.fields({size: true}, function(data){
console.log(data);
}).exec();
预期结果
输入相应节点的对应的尺寸信息

实际结果
TypeError: execCallback is not a function
