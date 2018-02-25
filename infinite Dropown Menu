var page = 'post.php';
$(function(){
	$('div').delegate('a.getMenu', 'click', function(){
		li_last = $(this).parent().parent('li');	
		
		var value = $(this).parent('p').html().split('-');
		var id = parseInt(value[0]);
		var nome = value[1].trim().split(' ');
		var ct_ul = li_last.children('ul.infinite_menu');
		
		if(ct_ul.length == 0){ //Verifica se o elemento já existe no documento
			
		$.post(page, { id:id , data:'getInfo'}, function(x){
           
			li_last.append('<ul class="infinite_menu">');
			
			 var ul = li_last.children('ul.infinite_menu');
			 
			 console.log('d');
			
			for(i in x){
				
				ul.append('<li><p>'+x[i].autor+'-'+x[i].titulo+'<a class="getMenu">[+]</a></p></li>');
			}
			
			 li_last.append('</ul>');
			
			},'json');
			
		}else{
			if(ct_ul.is(':visible')){
				ct_ul.hide('fast');
			}else{
				ct_ul.show('fast');
			}
			//Verifica se o elemento está visivel
			
		}
		
		//Fecha o Delegate da Classe
		return false;
		});
	
	});//FEcha o Jquery 
