---
description: 'Más información sobre: JET_INDEXCREATE2 estructura'
title: Estructura de JET_INDEXCREATE2
TOCTitle: JET_INDEXCREATE2 Structure
ms:assetid: c574500e-8695-4f29-8e9d-6dff987af2a2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294082(v=EXCHG.10)
ms:contentKeyID: 32765697
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
ms.openlocfilehash: d792bba4641f4fdadd873bac194ff409e15ffef1
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983988"
---
# <a name="jet_indexcreate2-structure"></a>Estructura de JET_INDEXCREATE2


_**Se aplica a:** Windows | Windows Servidor_

La **JET_INDEXCREATE2** estructura contiene la información necesaria para crear un índice sobre los datos en una base de datos extensible Storage motor de base de datos (ESE). La estructura la usan funciones como [JetCreateIndex2](./jetcreateindex2-function.md)y en estructuras [como JET_TABLECREATE](./jet-tablecreate-structure.md) y [JET_TABLECREATE2](./jet-tablecreate2-structure.md).

La **JET_INDEXCREATE2** estructura se introdujo en el sistema operativo Windows 7.

```cpp
typedef struct tagJET_INDEXCREATE2 {
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
  JET_SPACEHINTS* pSpacehints;
} JET_INDEXCREATE;
```

### <a name="members"></a>Miembros

**cbStruct**

Tamaño, en bytes, de esta estructura. Establezca este miembro en sizeof( JET_INDEXCREATE2 ).

**szIndexName**

Nombre del índice que se creará.

El nombre debe cumplir las condiciones siguientes:

  - Debe ser menor que JET_cbNameMost, sin incluir el valor null de terminación.

  - Debe constar del siguiente conjunto de caracteres: de 0 (cero) a 9, de A a Z, de a a z y de todos los demás signos de puntuación excepto " \! " (signo de exclamación), "," (coma), " " (corchete de apertura) y " " (corchete de cierre), es decir, caracteres \[ \] ASCII 0x20, 0x22 a 0x2d, 0x2f a 0x5a, 0x5c y 0x5d a 0x7f.

  - No debe comenzar con un espacio.

  - Debe contener al menos un carácter que no sea de espacio.

**szKey**

Puntero a una cadena terminada en doble null de tokens delimitados por NULL.

Cada token tiene el formato \<direction-specifier\> \<column-name\> " ", donde direction-specification es "+" o "-". Por ejemplo, un **szKey** de "+abc 0-def 0+ghi 0" indexará sobre las tres columnas \\ \\ \\ "abc" (en orden ascendente), "def" (en orden descendente) y "ghi" (en orden ascendente). En el lenguaje C, los literales de cadena tienen un terminador **NULL** implícito, por lo que la cadena anterior finalizará con un valor null doble.

El número de columnas especificado en **szKey** no debe superar JET_ccolKeyMost (una constante dependiente de la versión).

Al menos una columna debe tener el nombre **szKey**.

Comportamiento obsoleto: después del terminador de doble NULL, es posible especificar un identificador de idioma (una palabra que se pasa a MAKELCID( langid, SORT_DEFAULT ) ) como una manera de especificar el LCID para el índice. No es válido especificar un identificador de idioma en **szKey** y un LCID en JET_UNICODEINDEX [(estableciendo](./jet-unicodeindex-structure.md) JET_bitIndexUnicode en *grbit*).

En desuso: después del identificador de idioma, es posible pasar **cbVarSegMac** como un **tipo de datos USHORT.** El comportamiento no está definido si USHORT se establece en **szKey** y si **cbVarSegMac** está establecido en la estructura .

**cbKey**

Longitud, en bytes, de **szKey**, incluidos los dos valores NULL finales.

**grbit**

Grupo de bits que contienen cero o más de las opciones de valor que se muestran en la tabla siguiente.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitIndexUnique</p> | <p>No se pueden duplicar las entradas de índice (claves). Esto se aplica cuando se <a href="gg269288(v=exchg.10).md">llama a JetUpdate,</a> no cuando se llama a <a href="gg294137(v=exchg.10).md">JetSetColumn.</a></p> | 
| <p>JET_bitIndexPrimary</p> | <p>El índice es un índice principal (agrupado). Cada tabla debe tener exactamente un índice principal. Si no se define explícitamente ningún índice principal en una tabla, el motor de base de datos creará su propio índice principal.</p> | 
| <p>JET_bitIndexDisallowNull</p> | <p>Ninguna de las columnas en las que se crea el índice puede contener <strong>un valor</strong> NULL.</p> | 
| <p>JET_bitIndexIgnoreNull</p> | <p>No agregue una entrada de índice para una fila si todas las columnas que se indizan son <strong>NULL.</strong></p> | 
| <p>JET_bitIndexIgnoreAnyNull</p> | <p>No agregue una entrada de índice para una fila si alguna de las columnas que se indexa es <strong>NULL.</strong></p> | 
| <p>JET_bitIndexIgnoreFirstNull</p> | <p>No agregue una entrada de índice para una fila si la primera columna que se indexa es <strong>NULL.</strong></p> | 
| <p>JET_bitIndexLazyFlush</p> | <p>Especifica que las operaciones de índice se registrarán de forma lazily.</p><p>JET_bitIndexLazyFlush no afecta a la latencia de las actualizaciones de datos. Si la operación de indexación se interrumpe por la terminación del proceso, soft recovery seguirá siendo capaz de conseguir que la base de datos tenga un estado coherente, pero es posible que el índice no esté presente.</p> | 
| <p>JET_bitIndexEmpty</p> | <p>No intente compilar el índice, ya que todas las entradas se evaluarían como <strong>NULL.</strong> <strong>grbit</strong> TAMBIÉN DEBE especificar JET_bitIgnoreAnyNull cuando JET_bitIndexEmpty se pasa. Se trata de una mejora del rendimiento. Por ejemplo, si se agrega una nueva columna a una tabla y, a continuación, se crea un índice sobre esta columna recién agregada, se examinan todos los registros de la tabla aunque no se agregan al índice. Al especificar JET_bitIndexEmpty se omite el examen de la tabla, lo que podría tardar mucho tiempo.</p> | 
| <p>JET_bitIndexUnversioned</p> | <p>JET_bitIndexUnversioned hace que la creación de índices sea visible para otras transacciones. Normalmente, una sesión de una transacción no podrá ver una operación de creación de índices en otra sesión. Esta marca puede ser útil si es probable que otra transacción cree el mismo índice. La segunda creación de índice simplemente producirá un error en lugar de provocar muchas operaciones de base de datos innecesarias. Es posible que la segunda transacción no pueda usar el índice inmediatamente. La operación de creación de índices debe completarse antes de poder usarse. La sesión no debe estar actualmente en una transacción para crear un índice sin información de versión.</p> | 
| <p>JET_bitIndexSortNullsHigh</p> | <p>Si se especifica esta marca, <strong>los valores NULL</strong> se ordenan después de los datos de todas las columnas del índice.</p> | 
| <p>JET_bitIndexUnicode</p> | <p>La especificación de esta marca afecta a la interpretación del campo de unión lcid/pidnicde en la estructura . Establecer el bit significa que el campo pidxunicode apunta realmente a <a href="gg294097(v=exchg.10).md">una JET_UNICODEINDEX</a> estructura. JET_bitIndexUnicode no es necesario para indexar datos Unicode. Solo es necesario para personalizar la normalización de los datos Unicode.</p> | 
| <p>JET_bitIndexTuples</p> | <p>Especifica que el índice es un índice de tupla. Consulte <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> para obtener una descripción de un índice de tupla.</p><p>El JET_bitIndexTuples se introdujo en el sistema operativo Windows XP.</p> | 
| <p>JET_bitIndexTupleLimits</p> | <p>Especificar esta marca afecta a la interpretación del campo de unión <strong>cbVarSegMac/ptuplelimits</strong> en la estructura . Establecer este bit significa que el campo <strong>ptuplelimits</strong> apunta realmente <a href="gg269207(v=exchg.10).md">a</a> una estructura JET_TUPLELIMITS para permitir límites de índice de tupla personalizados (implica JET_bitIndexTuples).</p><p>El <strong>JET_bitIndexTupleLimits</strong> se introdujo en el sistema operativo Windows Server 2003.</p> | 
| <p>JET_bitIndexCrossProduct<br />0x00004000</p> | <p>Si se especifica esta marca para un índice que tiene más de una columna de clave que es una columna de varios valores, se creará una entrada de índice para cada resultado de un producto cruzado de todos los valores de esas columnas de clave. De lo contrario, el índice solo tendría una entrada para cada valor múltiple en la columna de clave más significativa que es una columna de varios valores y cada una de esas entradas de índice usaría el primer valor múltiple de cualquier otra columna de clave que sea columnas con varios valores.</p><p>Por ejemplo, si especificó esta marca para un índice sobre la columna A que tiene los valores "red" y "blue" y sobre la columna B que tiene los valores "1" y "2", se crearían las siguientes entradas de índice: "red", "1"; "red", "2"; "blue", "1"; "blue", "2". De lo contrario, se crearían las siguientes entradas de índice: "red", "1"; "blue", "1".</p><p>El <strong>JET_bitIndexCrossProduct</strong> se introdujo en Windows Vista.</p> | 
| <p>JET_bitIndexKeyMost<br />0x00008000</p> | <p>Si se especifica esta marca, el índice usará el tamaño máximo de clave especificado en el <strong>campo cbKeyMost</strong> de la estructura . De lo contrario, el índice usará JET_cbKeyMost (255) como tamaño máximo de clave.</p><p>El <strong>JET_bitIndexKeyMost</strong> se introdujo en Windows Vista.</p> | 
| <p>JET_bitIndexDisallowTruncation<br />0x00010000</p> | <p>Si se especifica esta marca, se producirá un error en cualquier actualización del índice que provocaría un error en una clave truncada con el código JET_errKeyTruncated respuesta. De lo contrario, las claves se truncarán en modo silencioso. Para obtener más información sobre el truncamiento de claves, <a href="gg269329(v=exchg.10).md">vea JetMakeKey</a>.</p><p>El <strong>JET_bitIndexDisallowTruncation</strong> se introdujo en Windows Vista.</p> | 



**ulDensity**

Densidad porcentual del árbol B+ del índice inicial. La especificación de un número menor que 100 consume más espacio para crear el índice inicialmente, pero permite que el crecimiento futuro del índice esté en su lugar, lo que evita la fragmentación interna.

**lcid**

Identificador de configuración regional (LCID) que se va a usar al normalizar los datos cuando el valor JET_bitIndexUnicode no se especifica en el *parámetro grbit.* El LCID afecta a la normalización si el índice está sobre columnas Unicode.

**pidxunicode**

Puntero a una [estructura JET_UNICODEINDEX](./jet-unicodeindex-structure.md) si el JET_bitIndexUnicode se especifica en el *parámetro grbit.* Esto permite al usuario especificar marcas personalizadas que se pasan a la [función LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) durante la normalización Unicode.

**cbVarSegMac**

Longitud máxima, en bytes, de cada columna que se va a almacenar en el índice cuando el valor JET_bitIndexTupleLimits no se especifica en el *parámetro grbit.*

Especificar un valor de 0 (cero) para este campo es equivalente a lo siguiente:

  - Especificar JET_cbPrimaryKeyMost para un índice principal.

  - Especificar JET_cbSecondaryKeyMost para un índice secundario.

**ptuplelimits**

Puntero a una [estructura JET_TUPLELIMITS](./jet-tuplelimits-structure.md) si se especifica el JET_bitIndexTupleLimits en el *parámetro grbit.*

**ptuplelimits** se introdujo en Windows Server 2003.

**rgconditionalcolumn**

Parámetro opcional para una matriz de [estructuras JET_CONDITIONALCOLUMN,](./jet-conditionalcolumn-structure.md) que se usan para especificar las columnas condicionales en el índice.

**cConditionalColumn**

Recuento de estructuras de la **matriz rgconditionalcolumn.**

**Err**

Contiene el código de retorno para crear este índice.

**cbKeyMost**

Especifica el tamaño máximo permitido, en bytes, para las claves del índice. Este parámetro se omite si JET_bitIndexKeyMost no se especifica en *el parámetro grbit.* Si este parámetro se establece en cero y JET_bitIndexKeyMost especifica en el miembro *grbit,* se producirá un error en la función de llamada JET_err_InvalidDef.

El tamaño máximo de clave mínimo admitido es JET_cbKeyMostMin (255), que es el tamaño máximo de clave heredado.

El tamaño máximo de clave depende del tamaño de página de la base de datos (JET_paramDatabasePageSize) como se muestra a continuación:

  - Si JET_paramDatabasePageSize = 2048, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost2KBytePage (500)

  - Si JET_paramDatabasePageSize = 4096, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost4KBytePage (1000)

  - Si JET_paramDatabasePageSize = 8192, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost8KBytePage (2000)

El tamaño máximo de clave admitido para la instancia también se puede leer desde JET_paramKeyMost parámetro del sistema.

**cbKeyMost** se introdujo en Windows Vista.

**pSpacehints**

Puntero a una [JET_SPACEHINTS](./jet-spacehints-structure.md) estructura.

**pSpacehints** se introdujo en Windows 7.

### <a name="remarks"></a>Observaciones

ESE admite la indexación sobre columnas de clave que contienen varios valores. Para usar esta característica, la columna debe ser un tipo de columna etiquetado (JET_bitColumnTagged) y debe marcarse para que sus varios valores se indexe con JET_bitColumnMultiValued. En versiones de Windows anteriores a Windows Vista, solo la primera columna de clave multivalor del índice tendrá sus valores expandido en el índice. Todas las demás columnas multivalor y etiquetadas solo tendrán sus primeros valores expandido en el índice.

Suponiendo que las filas siguientes existen en una tabla (la columna Alpha no tiene varios valores, mientras que las columnas Beta, Gamma y Delta son de varios valores) y se crea un índice como "+Alpha \\ 0+Beta \\ 0+Gamma \\ 0+Delta \\ 0 \\ 0":


| <p>Alpha</p> | <p>Beta</p> | <p>Gamma</p> | <p>Delta</p> | 
|--------------|-------------|--------------|--------------|
| <p>1</p> | <p>ABC<br />GHI<br />JKL</p> | <p>MNO<br />PQR<br />STU</p> | <p>VWX<br />YZ</p> | 
| <p>2</p> | <p>EL</p> | <p>LLUVIA<br />ESPAÑA</p> | <p>IN<br />CAE</p> | 



Se almacenarán las siguientes tuplas de índice:

{1,ABC,MNO,VWX}  
{1,GHI,MNO,VWX}  
{1,JKL,MNO,VWX}  
{2,THE,RAIN,IN}

Tenga en cuenta que {2,THE,SPAIN,IN} no está almacenado, aunque la columna Alfa de la segunda fila tenga un único valor múltiple.

En las versiones de Windows a partir de Windows Vista, todas las columnas multivalor se pueden expandir en el índice especificando JET_bitIndexCrossProduct.

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JET_ INDEXCREATE2_W</strong> (Unicode) <strong>y JET_ INDEXCREATE2_A</strong> (ANSI).</p> | 



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
