### Dev Skill Test


#### 1- Quais são os três principais tipos de componentes do Docker?

#### 2- Quais as principais métricas que podemos utilizar para definir uma política de escalabilidade para tasks de um App java em um cluster ECS?

#### 3- O que são Terraform e CloudFormation?

#### 4- Usando o Princípio Aberto-Fechado (OCP) refatore o código abaixo para que futuramente seja possível adicionar novos tipos de pagamento sem a necessidade de acrescentar uma nova condição no `if` do método `processarPagamento`. Explique quais as vantagens de utilizar esse princípio.

```java
//imports

public class Pagamento {
    private double valor;
    private String tipoPagamento;
    
    public Pagamento(double valor, String tipoPagamento) {
        this.valor = valor;
        this.tipoPagamento = tipoPagamento;
    }
    
    public void processarPagamento() {
        if (tipoPagamento.equals("cartao")) {
            // processar pagamento com cartão de crédito
        } else if (tipoPagamento.equals("boleto")) {
            // processar pagamento com boleto bancário
        } else {
            // processar pagamento com outra forma de pagamento
        }
    }
}
```

#### 5- Um analista desenvolveu uma API para buscar produtos ativos para um determinado segmento de cliente, e você precisa fazer o Code Review dessa funcionalidade. Aponte possíveis problemas ou possibilidades de melhoria conforme ache necessário.


```java
//imports

@RestController("ecommerce.api.prod.ihf/")
public class ProdutosController {

    private final ProdutoRepository produtoRepository;

    @PostMapping(value = "/produtos/segmentoCliente={segmento}&statusProduto=ATIVO")
    public List<Produto> buscarProdutos(@PathVariable("segmento") final String segmento){

        final List<Produto> produtos = produtoRepository.findAllBySegmento(segmento);

        return produtos;
    }
}
```

#### 6- Qual a função da anotação `com.fasterxml.jackson.annotation.JsonProperty`? Dado o trecho de codigo abaixo, qual seria o output JSON do `Produto` em uma requisição REST?

```java
//imports

@Data
@Builder
public class Produto {

    @JsonProperty("nome_produto")
    private String nomeProduto;

    @JsonAlias("situacao_produto")
    @JsonProperty("status_produto")
    private String status;

    @JsonProperty("descricao_produto")
    private String descricao;

}

```

#### 7- Qual arquitetura você consegue identificar na estrutura desse projeto? e por quê? 

![image](https://github.com/leonardobugoni/dev-skill-test/assets/26549166/e80e6df8-2b87-4c8e-8de1-779672f17a1b)





