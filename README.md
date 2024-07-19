# Cadastro de Funcionarios

## Resumo

Fiz um crud simples utilizando JavaScript puro para as funcionalidades, é um crud para cadastro de funcionarios onde podemos colocar nome, função e salario, editar e excluir todas as informações ou apenas algumas.


## Techs Utilizadas

 - HTML5
 - CSS 3
 - JavaScript

## Um Pouco do Codigo
```
   function openModal(edit = false, index = 0) {
  modal.classList.add('active')

  modal.onclick = e => {
    if (e.target.className.indexOf('modal-container') !== -1) {
      modal.classList.remove('active')
    }
  }

  if (edit) {
    sNome.value = itens[index].nome
    sFuncao.value = itens[index].funcao
    sSalario.value = itens[index].salario
    id = index
  } else {
    sNome.value = ''
    sFuncao.value = ''
    sSalario.value = ''
  }
  
}

function editItem(index) {

  openModal(true, index)
}

function deleteItem(index) {
  itens.splice(index, 1)
  setItensBD()
  loadItens()
}
```

## Print do Site
[link do projeto](https://crud-one-ochre.vercel.app/)
![image](https://github.com/devcarlosrlima/CRUD/assets/136191341/a4675b43-61cf-4cd8-b4fb-a152c21d8332)
