#include<iostream>
using namespace std;
int main()
{
	char again = 'y'/'n';
	do {
		int price, quantity, taxrate;
		cout << "Enter the price of product" << endl;
		cin >> price;
		cout << "Enter the Quantity" << endl;
		cin >> quantity;
		cout << "Enter the tax rate" << endl;
		cin >> taxrate;
		const float discountrate = 0.1;
		float total_price_before_tax = price * quantity;
		float discount_amount = total_price_before_tax * discountrate;
		float total_price_after_dsicount = total_price_before_tax - discount_amount;
		float taxamount = total_price_after_dsicount * (taxrate) / 100;
		float totalcostwithtax = total_price_after_dsicount - taxamount;
		if (quantity >= 10)
		{
			cout << "Total price before tax : " << total_price_before_tax << endl;
			cout << "Discount amount : " << discount_amount << endl;
			cout << "Total price after discount : " << total_price_after_dsicount << endl;
			cout << "Tax amount : " << taxamount << endl;
			cout << "Total cost with no tax : " << totalcostwithtax << endl;
		}
		else
		{
			cout << "Due to the low quantity, The total price with no discount is : " << total_price_before_tax << endl;
		}
		cout << "Again?? (y/n)" << endl;
		cin >> again;
	} while (again == 'y');
	return 0;
}
