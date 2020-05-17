<p align="center"><img src="https://res.cloudinary.com/dtfbvvkyp/image/upload/v1566331377/laravel-logolockup-cmyk-red.svg" width="400"></p>

# Laravel Udemy

## Relacionamento um para muitos

## MySQL

Os tipo de **id** de tabela geralmente são **BigInteger**

```
$table->BigInteger('categoria_id')->unsigned(); 
```

## Seeder

Seeder sem factory

Adicionar uma chamada para classes no *DatabaseSeeder.php*

```
	$this->call(CategoriaSeeder::class);
	$this->call(ProdutoSeeder::class);
```



Comando *php artisan db:seed*

```
DB::table('produtos')->insert(
        	['nome' => 'Camiseta Polo', 'preco' => 100,
            'estoque' = 4, 'categoria_id' => 1]);
```