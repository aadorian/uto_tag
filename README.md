# Ontology Tagg

Ontology tagging: um componente para classificação de conteúdo baseado em ontologia


A integração de ontologias de domínio com folksonomia visa facilitar o compartilhamento, a busca e a recuperação do conteúdo disponibilizado na web, por parte das máquinas. Este artigo apresenta o modelo denominado Ontology Tagging que utiliza ontologias de domínio como base para geração de tags e assim classificar conteúdos na web ou indexar informações em outras aplicações. Outro ponto desse artigo foi a criação de um algoritmo para representação visual de tags, em forma de nuvem, utilizando os relacionamentos entre os conceitos da ontologia como base para sua navegação. Para avaliação presenta-se um experimento prático com uma Ontologia desenvolvida no software Protégé a partir do tutorial da Universidade de Manchester, 

http://repositoriosenaiba.fieb.org.br/bitstream/fieb/504/1/Ontology%20...%20MCTI.pdf

Upper Tag Ontology (UTO) For
Integrating Social Tagging Data


The Upper Tag Ontology (UTO) is an **upper-level ontology** for social tagging that is designed to circumvent the complexity and potential redundancy inherent in user-generated tagging vocabularies.

UTO is based on Gruber’s (2007) suggestion that an **ontology can be used to model tagging data**, but it extends this idea with its focus on alignment between ontologies and the integration of tagging data
with other sources of social metadata.

Ontology: UTO-Ontology

Concepts:
- Tag ⊆ Concept
- Comment
- Source ⊆ Community
- Vote
- Date
- Tagger ⊆ Agent ∩ Usergroup
- Tagging
- Object ⊆ {Document, Image, Post}

Roles:
- hasDate: Tagging → Date
- hasObject: Tagging → Object
- hasTag: Tagging → Tag
- hasComment: Tagging → string
- hasRelatedTag: Tag → Tag
- hasCreator: Tagging → Tagger
- hasSource: Object → Source

Axioms:
- ∀x.(Tag(x) → Concept(x))
- ∀x.(Source(x) → Community(x))
- ∀x.(Tagger(x) → Agent(x) ∧ Usergroup(x))
- ∀x.(Object(x) → Document(x) ∨ Image(x) ∨ Post(x))
