Rails Command:

1.
change_table :products do |t|
	t.change :price, :string
end

2.
drop_table :products

MySQL Equivalent:

1.
ALTER TABLE products
Modify price string

2.
DROP TABLE products