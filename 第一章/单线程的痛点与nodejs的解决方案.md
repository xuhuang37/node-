# 单线程的痛点
    1.无法利用多核cpu

    2.错误会引起应用退出，应用的健壮性值得考研

    3.大量计算占用cpu导致无法继续调用异步i/o

# nodejs的解决方案
方案：
    child_process(子进程)

    子进程的出现，使Node可以从容应对单线程在健壮性和无法利用多核CPU的问题
实现：
    
    将计算分发到各个子进程，将大计算量分解掉，通过进程之间的时间消息来传递结果，很好保持应用模型的简单依赖，
