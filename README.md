function infected=extrapolation(Day,Y,fit1)
x=Day;
Data=Y;
p1=fit1.coeff(:,1);
p2=fit1.coeff(:,2);
p3=fit1.coeff(:,3);
p4=fit1.coeff(:,4);
p5=fit1.coeff(:,5);
 for i=1:x
x=i;
infected(1,i) = p1*x^4 + p2*x^3 + p3*x^2 + p4*x^1 + p5;
 end  
 figure;
 plot(Data,'*');
 hold on;
 plot(infected,'-')
end
