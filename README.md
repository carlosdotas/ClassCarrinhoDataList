# ClassCarrinhoDataList
 Implementa a Class Carrinho em Datalist Easyui

## Funções Basicas 

	const carrinho = new carrinhoEasyui({
		elemento:'#carrinho',
		columns:[[
	        {field:'cod',title:'Codigo'},
	        {field:'name',title:'Nome'},
	        {field:'preco',title:'Preco',align:'right'},
	        {field:'qnt',title:'Qnt',align:'center'},
	        {field:'total',title:'Total',align:'right'},
	    ]],
		onSet:function(row,object){
			console.log(object);
			$('#valorTotal').val(object.valorTotal)
			$('#valorPago').val(object.valorPago)
			$('#valorTroco').val(object.valorTroco)
		}
	});
	
	
		carrinho.insertItem({
			data:{cod:$('#cod').val(),name:$('#name').val(),preco:$('#preco').val(),qnt:$('#qnt').val()},
		});
	

		carrinho.removeItem({
			data:{cod:$('#cod').val(),name:$('#name').val(),preco:$('#preco').val(),qnt:$('#qnt').val()},
		});

	
		carrinho.delItem({
			data:{cod:$('#cod').val(),name:$('#name').val(),preco:$('#preco').val(),qnt:$('#qnt').val()},
		});
	
