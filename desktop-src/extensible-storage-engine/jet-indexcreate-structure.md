---
description: 'Más información sobre: JET_INDEXCREATE estructura'
title: Estructura de JET_INDEXCREATE
TOCTitle: JET_INDEXCREATE Structure
ms:assetid: 0c55f25c-d42a-49ba-a1fe-549850fdc9a6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269186(v=EXCHG.10)
ms:contentKeyID: 32765489
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 31b6b72cba336e3f7251bacfb1836673086ba9c2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467632"
---
# <a name="jet_indexcreate-structure"></a>Estructura de JET_INDEXCREATE


_**Se aplica a:** Windows | Windows Servidor_

La **JET_INDEXCREATE** estructura contiene la información necesaria para crear un índice sobre los datos en una base de datos extensible Storage motor de base de datos (ESE). La estructura la usan funciones como [JetCreateIndex2](./jetcreateindex2-function.md)y en estructuras [como JET_TABLECREATE](./jet-tablecreate-structure.md) y [JET_TABLECREATE2](./jet-tablecreate2-structure.md).

``` c++
typedef struct tagJET_INDEXCREATE {
  unsigned long cbStruct;
  tchar* szIndexName;
  tchar* szKey;
  unsigned long cbKey;
  JET_GRBIT grbit;
  unsigned long ulDensity;
  union {
    unsigned long lcid;
    JET_UNICODEINDEX* pidxunicode;
  };
  union {
    unsigned long cbVarSegMac;
    JET_TUPLELIMITS* ptuplelimits;
  };
  JET_CONDITIONALCOLUMN* rgconditionalcolumn;
  unsigned long cConditionalColumn;
  JET_ERR err;
  unsigned long cbKeyMost;
} JET_INDEXCREATE;
```

### <a name="members"></a>Miembros

**cbStruct**

Tamaño, en bytes, de esta estructura. Establezca este miembro en sizeof( JET_INDEXCREATE ).

**szIndexName**

Nombre del índice que se creará.

El nombre del índice debe cumplir las condiciones siguientes:

  - Debe ser menor que JET_cbNameMost, sin incluir el valor null final.

  - Debe constar de los siguientes caracteres: de 0 (cero) a 9, de A a Z, de a a z y de todos los demás signos de puntuación excepto " \! " (signo de exclamación), "," (coma), " " (corchete de apertura) y " " (corchete de cierre), es decir, caracteres \[ \] ASCII 0x20, 0x22 a través de 0x2d, 0x2f a través de 0x5a, 0x5c, 0x5d a 0x7f.

  - No debe comenzar con un espacio.

  - Debe constar de al menos un carácter que no sea de espacio.

**szKey**

Puntero a una cadena terminada en doble null de tokens delimitados por NULL.

Cada token tiene el formato \<direction-specifier\> \<column-name\> " ", donde direction-specification es "+" o "-". Por ejemplo, un **szKey** de "+abc 0-def 0+ghi 0" indexará sobre las tres columnas \\ \\ \\ "abc" (en orden ascendente), "def" (en orden descendente) y "ghi" (en orden ascendente). En el lenguaje C, los literales de cadena tienen un **terminador NULL** implícito; por lo tanto, la cadena anterior finalizará con un valor double-NULL.

El número de columnas especificadas en **szKey** no puede superar el valor de **JET_ccolKeyMost** (una constante dependiente de la versión).

Al menos una columna debe tener el nombre **szKey**.

Comportamiento obsoleto: después del terminador de doble NULL, es posible especificar un identificador de idioma (una palabra que se pasa a MAKELCID( langid, SORT_DEFAULT ) ) como una manera de especificar el LCID para el índice. No es válido especificar un identificador de idioma en **szKey** y un LCID en [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) (estableciendo JET_bitIndexUnicode en *grbit*).

En desuso: después del identificador de idioma, es posible pasar **cbVarSegMac** como USHORT. El comportamiento no está definido si USHORT se establece en **szKey** y si **cbVarSegMac** está establecido en la estructura .

**cbKey**

Longitud, en bytes, de **szKey,** incluidos los dos valores NULL finales.

**grbit**

Grupo de bits que incluye cero o más de los valores enumerados en la tabla siguiente.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitIndexUnique</p> | <p>No se permiten entradas de índice duplicadas (claves). Esto se aplica cuando se <a href="gg269288(v=exchg.10).md">llama a JetUpdate,</a> no cuando se llama a <a href="gg294137(v=exchg.10).md">JetSetColumn.</a></p> | 
| <p>JET_bitIndexPrimary</p> | <p>El índice es un índice principal (agrupado). Cada tabla debe tener exactamente un índice principal. Si no se define explícitamente ningún índice principal en una tabla, el motor de base de datos creará su propio índice principal.</p> | 
| <p>JET_bitIndexDisallowNull</p> | <p>Ninguna de las columnas en las que se crea el índice puede contener <strong>un valor</strong> NULL.</p> | 
| <p>JET_bitIndexIgnoreNull</p> | <p>No agregue una entrada de índice para una fila si todas las columnas que se indizan son <strong>NULL.</strong></p> | 
| <p>JET_bitIndexIgnoreAnyNull</p> | <p>No agregue una entrada de índice para una fila si alguna de las columnas que se indexa es <strong>NULL.</strong></p> | 
| <p>JET_bitIndexIgnoreFirstNull</p> | <p>No agregue una entrada de índice para una fila si la primera columna que se indexa es <strong>NULL.</strong></p> | 
| <p>JET_bitIndexLazyFlush</p> | <p>Las operaciones de índice se registrarán de forma lazi.</p><p>JET_bitIndexLazyFlush no afecta a la latencia de las actualizaciones de datos. Si la operación de indexación se interrumpe por la terminación del proceso, la recuperación flexible seguirá siendo capaz de conseguir que la base de datos tenga un estado coherente, pero es posible que el índice no esté presente.</p> | 
| <p>JET_bitIndexEmpty</p> | <p>No intente compilar el índice, porque todas las entradas se evaluarían como <strong>NULL.</strong> <strong>Grbit</strong> también debe especificar JET_bitIgnoreAnyNull cuando JET_bitIndexEmpty se pasa. Se trata de una mejora del rendimiento. Por ejemplo, si se agrega una nueva columna a una tabla, se crea un índice sobre esta columna recién agregada y se examinan todos los registros de la tabla aunque no se agregan al índice. Al especificar JET_bitIndexEmpty omite el examen de la tabla, lo que podría tardar mucho tiempo.</p> | 
| <p>JET_bitIndexUnversioned</p> | <p>Hace que la creación de índices sea visible para otras transacciones. Normalmente, una sesión de una transacción no podrá ver una operación de creación de índices en otra sesión. Esta marca puede ser útil si es probable que otra transacción cree el mismo índice. La segunda creación de índice producirá un error en lugar de provocar muchas operaciones de base de datos innecesarias. Es posible que la segunda transacción no pueda usar el índice inmediatamente. La operación de creación de índices debe completarse antes de poder usarse. La sesión no debe estar actualmente en una transacción para crear un índice sin información de versión.</p> | 
| <p>JET_bitIndexSortNullsHigh</p> | <p>Si se especifica esta marca, <strong>los valores NULL</strong> se ordenan después de los datos de todas las columnas del índice.</p> | 
| <p>JET_bitIndexUnicode</p> | <p>La especificación de esta marca afecta a la interpretación del campo de unión lcid/pidnicde de la estructura . Establecer el bit significa que el <strong>campo pidxunicode</strong> apunta realmente a <a href="gg294097(v=exchg.10).md">una JET_UNICODEINDEX</a> estructura. JET_bitIndexUnicode no es necesario para indexar datos Unicode. Solo se usa para personalizar la normalización de datos Unicode.</p> | 
| <p>JET_bitIndexTuples</p> | <p>Especifica que el índice es un índice de tupla. Consulte <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> para obtener una descripción de un índice de tupla.</p><p>JET_bitIndexTuples se introdujo en el sistema operativo Windows XP.</p> | 
| <p>JET_bitIndexTupleLimits</p> | <p>Especificar esta marca afecta a la interpretación del campo de unión <strong>cbVarSegMac/ptuplelimits</strong> en la estructura . Establecer este bit significa que el campo <strong>ptuplelimits</strong> apunta realmente a una estructura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> para permitir límites de índice de tupla personalizados (implica JET_bitIndexTuples).</p><p>JET_bitIndexTupleLimits se introdujo en el sistema operativo Windows Server 2003.</p> | 
| <p>JET_bitIndexCrossProduct 0x00004000</p> | <p>Si se especifica esta marca para un índice que tiene más de una columna de clave que es una columna de varios valores, se creará una entrada de índice para cada resultado de un producto cruzado de todos los valores de esas columnas de clave. De lo contrario, el índice solo tendría una entrada para cada valor múltiple en la columna de clave más significativa que es una columna de varios valores y cada una de esas entradas de índice usaría el primer valor múltiple de cualquier otra columna de clave que sea de varias columnas.</p><p>Por ejemplo, si especificó esta marca para un índice sobre la columna A que tiene los valores "red" y "blue" y sobre la columna B que tiene los valores "1" y "2", se crearían las siguientes entradas de índice: "red", "1"; "red", "2"; "blue", "1"; "blue", "2". De lo contrario, se crearían las siguientes entradas de índice: "red", "1"; "blue", "1".</p><p>JET_bitIndexCrossProduct se introdujo en el sistema operativo Windows Vista.</p> | 
| <p>JET_bitIndexKeyMost 0x00008000</p> | <p>Si se especifica esta marca, el índice usará el tamaño máximo de clave especificado en el <strong>campo cbKeyMost</strong> de la estructura . De lo contrario, el índice usará JET_cbKeyMost (255) como tamaño máximo de clave.</p><p>JET_bitIndexKeyMost se introdujo en Windows Vista.</p> | 
| <p>JET_bitIndexDisallowTruncation 0x00010000</p> | <p>Si se especifica esta marca, se producirá un error en cualquier actualización del índice que provocaría un error en una clave truncada con JET_errKeyTruncated. De lo contrario, las claves se truncarán en modo silencioso. Para más información sobre el truncamiento de claves, consulte la <a href="gg269329(v=exchg.10).md">función JetMakeKey.</a></p><p><strong>Windows Vista: JET_bitIndexDisallowTruncation</strong> se introdujo en Windows Vista.</p> | 
| <p>JET_bitIndexNestedTable 0x00020000</p> | <p>Si se especifica esta marca, se actualizará el índice en varias columnas de varios valores, pero solo con valores de la misma <strong>itagSequence</strong>.</p><p>JET_bitIndexNestedTable se introdujo en Windows Vista.</p> | 



**ulDensity**

Densidad porcentual del árbol B+ del índice inicial. La especificación de un número menor que 100 consume más espacio para crear el índice inicialmente, pero permite que el crecimiento futuro del índice esté en su lugar, lo que evita la fragmentación interna.

**lcid**

Identificador de configuración regional (LCID) que se va a usar al normalizar los datos cuando no JET_bitIndexUnicode valor de configuración regional en el *parámetro grbit.* El LCID afecta a la normalización si el índice está sobre columnas Unicode.

**pidxunicode**

Puntero a una [estructura JET_UNICODEINDEX](./jet-unicodeindex-structure.md) si se especifica el JET_bitIndexUnicode en el *parámetro grbit.* Esto permite al usuario especificar marcas personalizadas que se pasan a la [función LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) durante la normalización Unicode.

**cbVarSegMac**

Longitud máxima, en bytes, de cada columna que se va a almacenar en el índice cuando el valor JET_bitIndexTupleLimits no se especifica en el *parámetro grbit.*

Especificar un valor de 0 (cero) para este campo equivale a:

  - Especificar JET_cbPrimaryKeyMost para un índice principal.

  - Especificar JET_cbSecondaryKeyMost para un índice secundario.

**ptuplelimits**

Puntero a una [estructura JET_TUPLELIMITS](./jet-tuplelimits-structure.md) si el JET_bitIndexTupleLimits se especifica en el *parámetro grbit.*

ptuplelimits se introdujo en Windows Server 2003.

**rgconditionalcolumn**

Parámetro opcional para una matriz de [estructuras JET_CONDITIONALCOLUMN,](./jet-conditionalcolumn-structure.md) que se usan para especificar las columnas condicionales en el índice.

**cConditionalColumn**

Recuento de estructuras de la **matriz rgconditionalcolumn.**

**Err**

Contiene el código de retorno para crear este índice.

**cbKeyMost**

Especifica el tamaño máximo permitido, en bytes, para las claves del índice. Este parámetro se omite si el JET_bitIndexKeyMost no se especifica en el *parámetro grbit.* Si este parámetro se establece en cero y JET_bitIndexKeyMost se especifica en el parámetro *grbit,* se producirá un error en la función de llamada JET_err_InvalidDef.

El tamaño máximo de clave mínimo admitido es JET_cbKeyMostMin (255), que es el tamaño máximo de clave heredado.

El tamaño máximo de clave depende del tamaño de página de la base de datos (JET_paramDatabasePageSize), como se muestra a continuación:

  - Si JET_paramDatabasePageSize = 2048, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost2KBytePage (500)

  - Si JET_paramDatabasePageSize = 4096, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost4KBytePage (1000)

  - Si JET_paramDatabasePageSize = 8192, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost8KBytePage (2000)

El tamaño máximo de clave admitido para la instancia también se puede leer desde el JET_paramKeyMost del sistema.

**cbKeyMost** se introdujo en Windows Vista.

### <a name="remarks"></a>Comentarios

ESE admite la indexación sobre columnas de clave que contienen varios valores. Para usar esta característica, la columna debe ser un tipo de columna etiquetado (JET_bitColumnTagged) y debe marcarse para que sus varios valores se indexe con JET_bitColumnMultiValued. En versiones de Windows anteriores a Windows Vista, solo la primera columna de clave multivalor del índice tendrá sus valores expandido en el índice. Todas las demás columnas multivalor y etiquetadas solo tendrán sus primeros valores expandido en el índice.

Suponiendo que las filas siguientes existen en una tabla (la columna Alpha no tiene varios valores, mientras que las columnas Beta, Gamma y Delta son de varios valores) y se crea un índice como "+Alpha \\ 0+Beta \\ 0+Gamma \\ 0+Delta \\ 0 \\ 0":


| <p>Alpha</p> | <p>Beta</p> | <p>Gamma</p> | <p>Delta</p> | 
|--------------|-------------|--------------|--------------|
| <p>1</p> | <p>ABC<br />GHI<br />JKL</p> | <p>MNO<br />PQR<br />STU</p> | <p>VWX<br />YZ</p> | 
| <p>2</p> | <p>EL</p> | <p>LLUVIA<br />ESPAÑA</p> | <p>IN<br />CAE</p> | 



Las tuplas de índice que se van a bajar se almacenarán:

{1,ABC,MNO,VWX}  
{1,GHI,MNO,VWX}  
{1,JKL,MNO,VWX}  
{2,THE,RAIN,IN}

Tenga en cuenta que {2,THE,SPAIN,IN} no está almacenado, aunque la columna Alfa de la segunda fila tenga un único valor múltiple.

En versiones de Windows a partir de Windows Vista, todas las columnas de varios valores se pueden expandir en el índice especificando JET_bitIndexCrossProduct.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JET_ INDEXCREATE_W</strong> (Unicode) <strong>y JET_ INDEXCREATE_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Consulte también

[JET_COLTYP](./jet-coltyp.md)  
[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TUPLELIMITS](./jet-tuplelimits-structure.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)  
[JetUpdate](./jetupdate-function.md)
