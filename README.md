# t-test
数据分析
t=linspace(0,2*pi,500)
y=100*sin(t)
noise=normrnd(0,15,500,1)
y=y+noise
figure;
plot(t,y)
xlabel('t')
xlabel('t')
ylabel('y=sin(t)+噪声')
yy1=smmoth(y,30);
figure;
plot(t,y,'k:');
hold on 
plot(t,yy1,'k','linewidth',3)
xlabel('t')
ylabel('moving')
legend('假造波形','平滑后波形')
yy2 =smooth(y,30,'lowness');
figure;
plot（t,y,'k');
hold on;
plot(t,yy2,'k','linewidth');
xlabel('t')
ylabel('lowess')
legend('加噪波形','平滑后波形')

yy3=smooth(y,30,'rlowess')
figure;
plot(t,y,'k')
hold on;
plot(t,y,'k','linewidth',3)
xlabel('rlowess')
legend('加噪波形','平滑后的波形')

yy4=smmoth(y,30,'loess')
figure;
plot(t,y,'k:')
hold on;
plot(t,yy4,'k','linewidth',3);
xlabel('t')
ylabel('lowess')
legend('加噪声波形','平滑后的波形')

yy5 =smooth(y,30,'sgolay',3);
figure;
plot(t,y,'k:')
hold on 
plot(t,yy5,'k','linewidth',3)
xlabel('sgolay')
legend('加噪声波形','平滑后的波形')
