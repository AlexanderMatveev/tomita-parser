# Список терминалов

Терминал может быть леммой слова заключенной в одинарные кавычки или одним из зарезервированных имен терминалов из приведенной ниже таблицы. Обратите внимание, что терминалы описывают не только отдельные слова, но и многословные сущности (уже собранные грамматикой или иным способом), вершины которых удовлетворяют определению терминала. Большинство терминалов совпадает с известными частями речи, однако часто это совпадение неполное. Например, терминал Adj не распознает краткие прилагательные.

Некоторые терминалы распознают пунктуацию, например Comma, LBracket. Знаки пунктуации для которых не существует соответствующего терминала могут быть описаны сочетанием терминала AnyWord с пометой wff (см. [список помет](all-labels-list.md)), например: `Anyword<wff="!">;`

Терминал | **Значение**
----- | -----
'...' | Морфологическая лемма. Записывается в одинарных кавычках
AnyWord | Любая последовательность символов без пробелов. Нужно быть острожнее с конструкцией `AnyWord*`, так как парсер в этом случае будет строить очень много вариантов и его работа сильно замедлится.
Word | Любое слово, состоящее из букв русского или латинского алфавита. Также разрешаются слова записанные через дефис. Под это определение не попадают цепочки, которые содержат знаки пунктуации (кроме дефиса), специальные ASCII символы и цепочки цифр.
Noun | Существительное (слово с граммемой <q>S</q>). Сюда не входят имена, фамилии и отчества.
Adj | Прилагательное, причастие, порядковое числительное или местоименное прилагательное: слово с граммемой <q>A</q>, <q>partcp</q>,<q> ANUM</q> или <q>APRO</q>. Краткие прилагательные сюда не входят.
OrdinalNumeral | Порядковое числительное: слово с граммемой <q>ANUM</q>.
Adv | Наречие: слово с граммемой <q>ADV</q>.
Participle | Причастие: слово с граммемой <q>partcp</q>.
Verb | Глагол: слово с граммемой <q>V</q>.
Prep | Предлог: слово с граммемой <q>PR</q>.
UnknownPOS | Нераспознанное морфологией слово. К этому нетерминалу не относятся несловарные слова, которые описаны в газетире. Морфологический компонент строит парадигму для таких слов, и они становятся словарными, если соответствующие статьи упоминаются в данной грамматике.
SimConjAnd | Слово <q>и</q>.
QuoteDbl | Двойные кавычки.
QuoteSng | Одинарные кавычки.
LBracket | Открывающая скобка.
RBracket | Закрывающая скобка.
Hyphen | Тире.
Punct | Точка.
Comma | Запятая.
Colon | Двоеточие.
Percent | Цепочка символов, включающая символ %.
Dollar | Цепочка символов, включающая символ $.
PlusSign | Знак плюс +.
EOSent | Символ конца предложения.


