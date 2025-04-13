# Análise de Sentimentos com Azure Language Studio 🎯

Este projeto demonstra o uso do **Azure AI Language Studio** para realizar análise de sentimentos em sentenças de texto em português. O objetivo é aplicar inteligência artificial para classificar emoções e sentimentos expressos em frases.

---

## 🚀 Etapas do Projeto

### 1. Criação do Arquivo de Entrada

Criei o arquivo `inputs/frases.txt` contendo diversas frases com sentimentos variados (positivos, negativos e neutros).

### 2. Acesso ao Language Studio

Acesse o [Azure Language Studio](https://language.cognitive.azure.com/):

- Clique em **Analyze Text**
- Escolha **Sentiment Analysis**
- Faça upload do arquivo `frases.txt` ou cole o conteúdo manualmente
- Selecione o idioma como **Português**
- Execute a análise

### 3. Resultados Obtidos

Após a análise, o Azure retornou os seguintes insights:

| Frase                                           | Sentimento |
|------------------------------------------------|------------|
| Hoje o dia está incrível e estou muito feliz!  | Positivo   |
| Não gostei do atendimento da loja              | Negativo   |
| Estou animado com o novo projeto!              | Positivo   |
| Esse filme é totalmente sem graça              | Negativo   |
| Preciso melhorar meu desempenho no trabalho    | Neutro     |

---

## 📸 Resultado do Processo

> Abaixo esta o arquivo JSON que mostra como foi feita a análise no Language Studio:

'''
{
    "documents": [
        {
            "id": "id__366",
            "sentiment": "mixed",
            "confidenceScores": {
                "positive": 0.5,
                "neutral": 0.01,
                "negative": 0.49
            },
            "sentences": [
                {
                    "sentiment": "positive",
                    "confidenceScores": {
                        "positive": 1,
                        "neutral": 0,
                        "negative": 0
                    },
                    "offset": 0,
                    "length": 46,
                    "text": "Hoje o dia está incrível e estou muito feliz!  ",
                    "targets": [],
                    "assessments": []
                },
                {
                    "sentiment": "negative",
                    "confidenceScores": {
                        "positive": 0,
                        "neutral": 0,
                        "negative": 1
                    },
                    "offset": 46,
                    "length": 48,
                    "text": "Não gostei do atendimento da loja, foi péssimo.  ",
                    "targets": [
                        {
                            "sentiment": "negative",
                            "confidenceScores": {
                                "positive": 0,
                                "negative": 1
                            },
                            "offset": 61,
                            "length": 11,
                            "text": "atendimento",
                            "relations": [
                                {
                                    "relationType": "assessment",
                                    "ref": "#/documents/0/sentences/1/assessments/0"
                                },
                                {
                                    "relationType": "assessment",
                                    "ref": "#/documents/0/sentences/1/assessments/1"
                                }
                            ]
                        },
                        {
                            "sentiment": "negative",
                            "confidenceScores": {
                                "positive": 0,
                                "negative": 1
                            },
                            "offset": 76,
                            "length": 4,
                            "text": "loja",
                            "relations": [
                                {
                                    "relationType": "assessment",
                                    "ref": "#/documents/0/sentences/1/assessments/1"
                                }
                            ]
                        }
                    ],
                    "assessments": [
                        {
                            "sentiment": "negative",
                            "confidenceScores": {
                                "positive": 0,
                                "negative": 1
                            },
                            "offset": 51,
                            "length": 6,
                            "text": "gostei",
                            "isNegated": true
                        },
                        {
                            "sentiment": "negative",
                            "confidenceScores": {
                                "positive": 0,
                                "negative": 1
                            },
                            "offset": 86,
                            "length": 7,
                            "text": "péssimo",
                            "isNegated": false
                        }
                    ]
                },
                {
                    "sentiment": "positive",
                    "confidenceScores": {
                        "positive": 0.99,
                        "neutral": 0.01,
                        "negative": 0
                    },
                    "offset": 94,
                    "length": 34,
                    "text": "Estou animado com o novo projeto!  ",
                    "targets": [
                        {
                            "sentiment": "positive",
                            "confidenceScores": {
                                "positive": 1,
                                "negative": 0
                            },
                            "offset": 121,
                            "length": 7,
                            "text": "projeto",
                            "relations": [
                                {
                                    "relationType": "assessment",
                                    "ref": "#/documents/0/sentences/2/assessments/0"
                                }
                            ]
                        }
                    ],
                    "assessments": [
                        {
                            "sentiment": "positive",
                            "confidenceScores": {
                                "positive": 1,
                                "negative": 0
                            },
                            "offset": 102,
                            "length": 7,
                            "text": "animado",
                            "isNegated": false
                        }
                    ]
                },
                {
                    "sentiment": "negative",
                    "confidenceScores": {
                        "positive": 0,
                        "neutral": 0.02,
                        "negative": 0.98
                    },
                    "offset": 128,
                    "length": 35,
                    "text": "Esse filme é totalmente sem graça.  ",
                    "targets": [
                        {
                            "sentiment": "negative",
                            "confidenceScores": {
                                "positive": 0.05,
                                "negative": 0.95
                            },
                            "offset": 136,
                            "length": 5,
                            "text": "filme",
                            "relations": [
                                {
                                    "relationType": "assessment",
                                    "ref": "#/documents/0/sentences/3/assessments/0"
                                }
                            ]
                        }
                    ],
                    "assessments": [
                        {
                            "sentiment": "negative",
                            "confidenceScores": {
                                "positive": 0.05,
                                "negative": 0.95
                            },
                            "offset": 155,
                            "length": 9,
                            "text": "sem graça",
                            "isNegated": false
                        }
                    ]
                },
                {
                    "sentiment": "neutral",
                    "confidenceScores": {
                        "positive": 0.09,
                        "neutral": 0.53,
                        "negative": 0.38
                    },
                    "offset": 163,
                    "length": 44,
                    "text": "Preciso melhorar meu desempenho no trabalho.",
                    "targets": [],
                    "assessments": []
                }
            ],
            "warnings": []
        }
    ],
    "errors": [],
    "modelVersion": "2025-01-01"
}
'''

---

## 💡 Insights e Possibilidades

- O Language Studio é excelente para análise de sentimentos em diferentes idiomas, inclusive o português.
- Muito útil para aplicações como:
  - Monitoramento de redes sociais
  - Análise de feedback de usuários
  - Detecção de satisfação do cliente
- A IA reconhece polaridades (positivo, negativo, neutro) e pode ser treinada para ajustar a sensibilidade.

---

## 🧠 Aprendizados

- O Azure facilita o uso de IA com interfaces visuais simples.
- Ferramentas como o Language Studio são poderosas mesmo para quem não é desenvolvedor e também pra quem é.
- Podemos integrar esses modelos em APIs para análise automatizada de grandes volumes de dados.

---

## 📁 Arquivos

- `inputs/frases.txt` – arquivo com frases utilizadas
- `imagens/` – prints do processo
- `README.md` – documentação do projeto

---

## 👨‍💻 Autor

Silas Oliveira

---

