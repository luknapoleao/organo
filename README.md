Organo
Organo é um projeto de organograma desenvolvido com React, utilizando JavaScript. Este projeto permite a criação de cards para colaboradores com informações detalhadas sobre nome, cargo, imagem e o time ao qual pertencem.

Funcionalidades
Formulário de Criação de Cards
O componente Formulario permite a criação de novos cards para colaboradores, com os seguintes campos:

Nome: Campo de texto para o nome do colaborador.
Cargo: Campo de texto para o cargo do colaborador.
Imagem: Campo de texto para o endereço da imagem do colaborador.
Time: Lista suspensa com os times disponíveis.

import Botao from '../Botao'
import CampoTexto from '../CampoTexto'
import ListaSuspensa from '../ListaSuspensa'
import './Formulario.css'

const Formulario = () => {
    const times = [
        'Programação',
        'Front-End',
        'Data Science',
        'Devops',
        'UX e Design',
        'Mobile',
        'Inovação e Gestão'
    ]

    return (
        <section className="formulario">
            <form>
                <h2>Preencha os dados para criar o card do colaborador.</h2>
                <CampoTexto label="Nome" placeholder="Digite seu nome"/>
                <CampoTexto label="Cargo" placeholder="Digite seu cargo" />
                <CampoTexto label="Imagem" placeholder="Digite o endereço da imagem" />
                <ListaSuspensa label="Time" itens={times} />
                <Botao>Criar Card</Botao>
            </form>
        </section>
    )
}

export default Formulario

Lista Suspensa
O componente ListaSuspensa é usado para selecionar o time do colaborador a partir de uma lista de opções.

import './ListaSuspensa.css'

const ListaSuspensa = (props) => {
    return (
        <div className='lista-suspensa'>
            <label>{props.label}</label>
            <select>
                {props.itens.map(item => {
                    return <option key={item}>{item}</option>
                })}
            </select>
        </div>
    )
}

export default ListaSuspensa

Como Iniciar o Projeto
Este projeto foi inicializado com Create React App. Para começar a usar, siga os passos abaixo:

Scripts Disponíveis
No diretório do projeto, você pode executar:

npm start
Executa o aplicativo no modo de desenvolvimento.
Abra http://localhost:3000 para visualizá-lo no navegador.

A página será recarregada se você fizer edições.
Você também verá quaisquer erros de lint no console.

npm test
Inicia o executor de testes no modo interativo de observação.
Veja a seção sobre execução de testes para mais informações.

npm run build
Cria o aplicativo para produção na pasta build.
Ele agrupa corretamente o React no modo de produção e otimiza a construção para obter o melhor desempenho.

A compilação é minificada e os nomes dos arquivos incluem os hashes.
Seu aplicativo está pronto para ser implantado!

Veja a seção sobre implantação para mais informações.

npm run eject
Nota: esta é uma operação sem volta. Uma vez que você eject, você não pode voltar atrás!

Se você não estiver satisfeito com a ferramenta de construção e as escolhas de configuração, você pode eject a qualquer momento. Este comando removerá a única dependência de construção do seu projeto.

Esse é um projeto colaborativo e de aprendizagem fique à vontade para contribuir com ele =) 
