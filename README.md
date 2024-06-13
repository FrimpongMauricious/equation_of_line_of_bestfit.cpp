# equation_of_line_of_bestfit.cpp
#include <iostream>

using namespace std;

int main()
{
    int n;
    cout<<"enter number of points: ";
    cin>>n;
    double x,y,sumx=0, sumy=0,sumxy=0,sumxsquared=0,x_squared;
    for(int i=1; i<=n; i++){
        cout<<"enter x coordinate of the point: ";
        cin>>x;
        cout<<"enter the y coordinate of the point: ";
        cin>>y;
        sumx=sumx+x;
        sumy=sumy+y;
        sumxy=sumxy+(x*y);
        sumxsquared=sumxsquared+(x*x);
    }
    double b=((sumxy-(sumx*sumy))/n)/(sumxsquared-(sumx*sumx));
    double a=sumy-(b*sumx)/n;
    cout<<"the equation of the line of bestfit is "<<" y= "<<a<<"x + "<<b;
}
