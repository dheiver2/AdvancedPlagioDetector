# Advanced Plagio Detector

Um sistema avançado de detecção de plágio com análise sintática e semântica.

## 📋 Sumário

- [Características](#características)
- [Requisitos](#requisitos)
- [Instalação](#instalação)
- [Como Usar](#como-usar)
- [Funcionalidades Detalhadas](#funcionalidades-detalhadas)
- [Exemplos](#exemplos)
- [Estrutura do Projeto](#estrutura-do-projeto)
- [Contribuindo](#contribuindo)
- [Licença](#licença)

## ✨ Características

- Análise sintática e semântica separadas
- Detecção de similaridade usando TF-IDF e SequenceMatcher
- Identificação de palavras-chave comuns
- Análise de contexto
- Detecção de alterações de palavras
- Relatórios detalhados
- Suporte a textos em português
- Identificação de trechos similares
- Métricas de similaridade configuráveis

## 📋 Requisitos

```plaintext
numpy
scikit-learn
nltk
```

## 🚀 Instalação

1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/enhanced-plagio-detector.git
cd enhanced-plagio-detector
```

2. Instale as dependências:
```bash
pip install -r requirements.txt
```

3. Baixe os recursos necessários do NLTK:
```python
import nltk
nltk.download('punkt')
nltk.download('stopwords')
```

## 💻 Como Usar

### Uso Básico

```python
from plagio_detector import EnhancedPlagioDetector

# Criar instância do detector
detector = EnhancedPlagioDetector()

# Textos para análise
texto_original = "Seu texto original aqui..."
texto_suspeito = "Texto para comparação aqui..."

# Realizar análise
relatorio = detector.verificar_plagio(texto_original, texto_suspeito)

# Apresentar resultados
detector.apresentar_resultados(relatorio)
```

### Personalização dos Parâmetros

```python
detector = EnhancedPlagioDetector(
    limiar_sintatico=0.6,      # Ajuste o limiar de similaridade sintática
    limiar_semantico=0.6,      # Ajuste o limiar de similaridade semântica
    tamanho_minimo_trecho=8    # Ajuste o tamanho mínimo dos trechos
)
```

## 🔍 Funcionalidades Detalhadas

### Análise Sintática
- Calcula similaridade TF-IDF
- Detecta sequências idênticas de palavras
- Identifica alterações de palavras
- Analisa padrões estruturais

### Análise Semântica
- Calcula similaridade de sequência
- Identifica trechos similares
- Encontra palavras-chave comuns
- Analisa contexto

### Relatório de Resultados
- Resultado geral de plágio
- Métricas detalhadas
- Trechos similares encontrados
- Palavras alteradas
- Estatísticas e metadados

## 📝 Exemplos

### Exemplo 1: Plágio Direto
```python
texto_original = """
O aquecimento global é um fenômeno climático que indica o aumento da 
temperatura média da Terra ao longo das últimas décadas.
"""

texto_suspeito = """
O aquecimento global é um fenômeno climático que mostra o aumento da 
temperatura média do planeta Terra nas últimas décadas.
"""
```

### Exemplo 2: Plágio com Paráfrase
```python
texto_original = """
A Revolução Industrial, iniciada na Inglaterra no século XVIII,
foi um período de grandes transformações tecnológicas e sociais.
"""

texto_suspeito = """
As transformações tecnológicas e sociais marcaram o período conhecido
como Revolução Industrial, que começou na Inglaterra durante o século XVIII.
"""
```

## 📁 Estrutura do Projeto

```
enhanced-plagio-detector/
├── plagio_detector/
│   ├── __init__.py
│   ├── detector.py
│   ├── analise_sintatica.py
│   └── analise_semantica.py
├── examples/
│   └── exemplos.py
├── tests/
│   └── test_detector.py
├── requirements.txt
└── README.md
```

## 🤝 Contribuindo

1. Faça um Fork do projeto
2. Crie sua Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a Branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## 📄 Licença

Distribuído sob a licença MIT. Veja `LICENSE` para mais informações.

## 🎯 Melhorias Futuras

- [ ] Suporte para mais idiomas
- [ ] Interface gráfica
- [ ] Análise de documentos PDF e DOCX
- [ ] API REST
- [ ] Integração com sistemas acadêmicos
- [ ] Base de dados de textos conhecidos
- [ ] Relatórios em diferentes formatos
- [ ] Análise de código-fonte
- [ ] Suporte a comparações múltiplas

## 📧 Contato

Seu Nome - [@dheiver](https://twitter.com/dheiver) - dheiver.santos@gmail.com

Link do Projeto: [https://github.com/seu-usuario/enhanced-plagio-detector](https://github.com/seu-usuario/enhanced-plagio-detector)
