---
description: 'Más información acerca de: estructura de JET_INDEXCREATE2'
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
ms.openlocfilehash: ac0d9a40e159a8aa5054228d18e431cee8d0319f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003181"
---
# <a name="jet_indexcreate2-structure"></a>Estructura de JET_INDEXCREATE2


_**Se aplica a:** Windows | Windows Server_

La estructura de **JET_INDEXCREATE2** contiene la información necesaria para crear un índice sobre los datos en una base de datos del motor de almacenamiento extensible (ese). La estructura la usan funciones como [JetCreateIndex2](./jetcreateindex2-function.md)y en estructuras como [JET_TABLECREATE](./jet-tablecreate-structure.md) y [JET_TABLECREATE2](./jet-tablecreate2-structure.md).

La estructura de **JET_INDEXCREATE2** se presentó en el sistema operativo Windows 7.

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

Tamaño, en bytes, de esta estructura. Establezca este miembro en sizeof (JET_INDEXCREATE2).

**szIndexName**

Nombre del índice que se va a crear.

El nombre debe cumplir las siguientes condiciones:

  - Debe ser menor que JET_cbNameMost, sin incluir el carácter null de terminación.

  - Debe constar del siguiente conjunto de caracteres: 0 (cero) a 9, de la a a la Z, de la a a la z, y todos los demás signos de puntuación excepto " \! " (signo de exclamación), "," (coma), " \[ " (corchete de apertura) y " \] " (corchete de cierre), es decir, caracteres ASCII 0x20, 0x22 a 0x2d, 0x2f a 0x5a, 0x5c y 0x5d a 0x7F.

  - No debe comenzar con un espacio.

  - Debe contener al menos un carácter que no sea un espacio.

**szKey**

Puntero a una cadena terminada en NULL de tokens delimitados por null.

Cada token tiene el formato " \<direction-specifier\> \<column-name\> ", donde Direction-Specification es "+" o "-". Por ejemplo, un **szKey** de "+ ABC \\ 0-Def \\ 0 + GHI \\ 0" indexará las tres columnas "ABC" (en orden ascendente), "def" (en orden descendente) y "GHI" (en orden ascendente). En el lenguaje C, los literales de cadena tienen un terminador **null** implícito, por lo que la cadena anterior se terminará con un valor null nulo.

El número de columnas especificado en **szKey** no debe superar JET_ccolKeyMost (una constante dependiente de la versión).

Al menos una columna debe tener un nombre en **szKey**.

Comportamiento obsoleto: después del terminador de doble nulo, es posible especificar un identificador de idioma (una palabra que se pasa a MAKELCID (langid, SORT_DEFAULT)) como una manera de especificar el LCID para el índice. No es válido especificar un identificador de idioma en **szKey** y un LCID en [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) (estableciendo JET_bitIndexUnicode en *grbit*).

En desuso: después del identificador de idioma, es posible pasar **cbVarSegMac** como un tipo de datos **USHORT** . El comportamiento es indefinido si USHORT se establece en **szKey** y si **cbVarSegMac** se establece en la estructura.

**cbKey**

La longitud, en bytes, de **szKey**, incluidos los dos valores NULL de terminación.

**grbit**

Grupo de bits que contiene cero o más de las opciones de valor que se enumeran en la tabla siguiente.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Value</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitIndexUnique</p></td>
<td><p>No se permiten entradas de índice duplicadas (claves). Esto se aplica cuando se llama a <a href="gg269288(v=exchg.10).md">JetUpdate</a> , no cuando se llama a <a href="gg294137(v=exchg.10).md">JetSetColumn</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexPrimary</p></td>
<td><p>El índice es un índice principal (clúster). Cada tabla debe tener exactamente un índice principal. Si no se define un índice principal explícitamente en una tabla, el motor de base de datos creará su propio índice principal.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexDisallowNull</p></td>
<td><p>Ninguna de las columnas en las que se crea el índice puede contener un valor <strong>null</strong> .</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexIgnoreNull</p></td>
<td><p>No agregue una entrada de índice para una fila si todas las columnas que se van a indizar son <strong>null</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexIgnoreAnyNull</p></td>
<td><p>No agregue una entrada de índice para una fila si alguna de las columnas que se van a indizar es <strong>null</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexIgnoreFirstNull</p></td>
<td><p>No agregue una entrada de índice para una fila si la primera columna que se va a indizar es <strong>null</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexLazyFlush</p></td>
<td><p>Especifica que las operaciones de índice se registrarán de forma diferida.</p>
<p>JET_bitIndexLazyFlush no afecta a la Laziness de las actualizaciones de datos. Si la terminación del proceso interrumpe la operación de indexación, la recuperación de software seguirá pudiendo ser capaz de obtener la base de datos en un estado coherente, pero es posible que el índice no esté presente.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexEmpty</p></td>
<td><p>No intente compilar el índice, ya que todas las entradas se evaluarían como <strong>null</strong>. <strong>grbit</strong> También debe especificar JET_bitIgnoreAnyNull cuando se pasa JET_bitIndexEmpty. Se trata de una mejora del rendimiento. Por ejemplo, si se agrega una nueva columna a una tabla y, a continuación, se crea un índice sobre esta columna recién agregada, se examinan todos los registros de la tabla, aunque no se agreguen al índice. Al especificar JET_bitIndexEmpty se omite el examen de la tabla, lo que podría tardar mucho tiempo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexUnversioned</p></td>
<td><p>JET_bitIndexUnversioned hace que la creación de índices sea visible para otras transacciones. Normalmente, una sesión de una transacción no podrá ver una operación de creación de índices en otra sesión. Esta marca puede ser útil si es probable que otra transacción cree el mismo índice. La segunda operación index-Create simplemente producirá un error en lugar de producir potencialmente muchas operaciones de base de datos innecesarias. Es posible que la segunda transacción no pueda usar el índice inmediatamente. La operación de creación de índices debe completarse antes de poderse usar. La sesión no debe estar actualmente en una transacción para crear un índice sin información de versión.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexSortNullsHigh</p></td>
<td><p>Si se especifica esta marca, se ordenarán los valores <strong>null</strong> después de los datos de todas las columnas del índice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexUnicode</p></td>
<td><p>La especificación de esta marca afecta a la interpretación del campo de Unión LCID/pidxunicde en la estructura. Establecer el bit significa que el campo pidxunicode apunta realmente a una estructura de <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> . JET_bitIndexUnicode no es necesario para indizar los datos Unicode. Solo es necesario personalizar la normalización de los datos Unicode.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexTuples</p></td>
<td><p>Especifica que el índice es un índice de tupla. Consulte <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> para obtener una descripción de un índice de tupla.</p>
<p>El valor JET_bitIndexTuples se presentó en el sistema operativo Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexTupleLimits</p></td>
<td><p>La especificación de esta marca afecta a la interpretación del campo de Unión <strong>cbVarSegMac/ptuplelimits</strong> de la estructura. Establecer este bit significa que el campo <strong>ptuplelimits</strong> apunta realmente a una estructura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> para permitir límites de índice de tupla personalizados (implica JET_bitIndexTuples).</p>
<p>El valor <strong>JET_bitIndexTupleLimits</strong> se presentó en el sistema operativo Windows Server 2003.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexCrossProduct<br />
0x00004000</p></td>
<td><p>Si se especifica esta marca para un índice que tiene más de una columna de clave que es una columna de varios valores, se creará una entrada de índice para cada resultado de un producto cruzado de todos los valores de esas columnas de clave. De lo contrario, el índice solo tendrá una entrada para cada multivalor de la columna de clave más importante que sea una columna de varios valores y cada una de esas entradas de índice usaría el primer valor de múltiples columnas de clave que son columnas de varios valores.</p>
<p>Por ejemplo, si especificó esta marca para un índice en la columna A que tiene los valores &quot; rojo &quot; y &quot; azul &quot; y sobre la columna B que tiene los valores &quot; 1 &quot; y &quot; 2 &quot; , se crearán las siguientes entradas de índice: &quot; rojo &quot; , &quot; 1 &quot; ; &quot; rojo &quot; , &quot; 2 &quot; ; &quot; azul &quot; , &quot; 1 &quot; ; &quot; azul &quot; , &quot; 2 &quot; . De lo contrario, se crearán las siguientes entradas de índice: &quot; rojo &quot; , &quot; 1 &quot; ; &quot; azul &quot; , &quot; 1 &quot; .</p>
<p>El valor <strong>JET_bitIndexCrossProduct</strong> se presentó en Windows Vista.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexKeyMost<br />
0x00008000</p></td>
<td><p>Si se especifica esta marca, el índice usará el tamaño de clave máximo especificado en el campo <strong>cbKeyMost</strong> de la estructura. De lo contrario, el índice usará JET_cbKeyMost (255) como tamaño máximo de la clave.</p>
<p>El valor <strong>JET_bitIndexKeyMost</strong> se presentó en Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexDisallowTruncation<br />
0x00010000</p></td>
<td><p>Si se especifica este marcador, se producirá un error en cualquier actualización del índice que dé lugar a una clave truncada con el código de respuesta JET_errKeyTruncated. De lo contrario, las claves se truncarán de forma silenciosa. Para obtener más información sobre el truncamiento de claves, vea <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</p>
<p>El valor <strong>JET_bitIndexDisallowTruncation</strong> se presentó en Windows Vista.</p></td>
</tr>
</tbody>
</table>


**ulDensity**

Densidad porcentual del árbol B + del índice inicial. Si se especifica un número menor que 100, se usa más espacio para crear el índice inicialmente, pero se permite el crecimiento futuro del índice, lo que evita la fragmentación interna.

**lcid**

Identificador de configuración regional (LCID) que se va a usar al normalizar los datos cuando el valor de JET_bitIndexUnicode no se especifica en el parámetro *grbit* . El LCID afecta a la normalización si el índice está en columnas Unicode.

**pidxunicode**

Puntero a una estructura de [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) si el valor de JET_bitIndexUnicode se especifica en el parámetro *grbit* . Esto permite al usuario especificar las marcas personalizadas que se pasan a la función [LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) durante la normalización Unicode.

**cbVarSegMac**

Longitud máxima, en bytes, de cada columna que se va a almacenar en el índice cuando el valor de JET_bitIndexTupleLimits no se especifica en el parámetro *grbit* .

Especificar un valor de 0 (cero) para este campo es equivalente a lo siguiente:

  - Especificar JET_cbPrimaryKeyMost para un índice principal.

  - Especificar JET_cbSecondaryKeyMost para un índice secundario.

**ptuplelimits**

Puntero a una estructura de [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) si el valor de JET_bitIndexTupleLimits se especifica en el parámetro *grbit* .

**ptuplelimits** se presentó en Windows Server 2003.

**rgconditionalcolumn**

Un parámetro opcional para una matriz de estructuras [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) , que se usan para especificar las columnas condicionales en el índice.

**cConditionalColumn**

Recuento de estructuras de la matriz **rgconditionalcolumn** .

**ERR**

Contiene el código de retorno para crear este índice.

**cbKeyMost**

Especifica el tamaño máximo permitido, en bytes, para las claves del índice. Este parámetro se omite si JET_bitIndexKeyMost no se especifica en el parámetro *grbit* . Si este parámetro se establece en cero y se especifica JET_bitIndexKeyMost en el miembro *grbit* , se producirá un error en la función de llamada con JET_err_InvalidDef.

El tamaño máximo de clave compatible mínimo es JET_cbKeyMostMin (255), que es el tamaño de clave máximo heredado.

El tamaño máximo de la clave depende del tamaño de página de la base de datos (JET_paramDatabasePageSize), como se indica a continuación:

  - Si JET_paramDatabasePageSize = 2048, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost2KBytePage (500)

  - Si JET_paramDatabasePageSize = 4096, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost4KBytePage (1000)

  - Si JET_paramDatabasePageSize = 8192, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost8KBytePage (2000)

El tamaño máximo de clave admitido para la instancia también se puede leer desde el parámetro del sistema JET_paramKeyMost.

**cbKeyMost** se presentó en Windows Vista.

**pSpacehints**

Puntero a una estructura de [JET_SPACEHINTS](./jet-spacehints-structure.md) .

**pSpacehints** se presentó en Windows 7.

### <a name="remarks"></a>Observaciones

ESE admite la indización de columnas de clave que contienen varios valores. Para usar esta característica, la columna debe ser un tipo de columna etiquetado (JET_bitColumnTagged) y se debe marcar para que sus múltiples valores se indexen con JET_bitColumnMultiValued. En las versiones de Windows anteriores a Windows Vista, solo se expandirá su valor en el índice de la primera columna de clave con varios valores del índice. Todas las demás columnas con varios valores y etiquetas solo tendrán sus primeros valores expandidos en el índice.

Suponiendo que las filas siguientes existen en una tabla (la columna alfa no tiene varios valores, mientras que las columnas beta, gamma y delta tienen varios valores) y se crea un índice como "+ alpha \\ 0 + beta \\ 0 + gamma \\ 0 + Delta \\ 0 \\ 0":

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Alpha</p></th>
<th><p>Beta</p></th>
<th><p>Gamma</p></th>
<th><p>Delta</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p>ABC<br />
GHI<br />
JKL</p></td>
<td><p>MNO<br />
PQR<br />
STU</p></td>
<td><p>VWX<br />
YZ</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>EL</p></td>
<td><p>LLUVIA<br />
España</p></td>
<td><p>IN<br />
PASÓ</p></td>
</tr>
</tbody>
</table>


Se almacenarán las siguientes tuplas de índice:

{1, ABC, MNO, VWX}  
{1, GHI, MNO, VWX}  
{1, JKL, MNO, VWX}  
{2,, RAIN, IN}

Tenga en cuenta que {2,, España, IN} no se almacena, aunque la columna alfa de la segunda fila tenga un solo multivalor.

En las versiones de Windows a partir de Windows Vista, todas las columnas con varios valores se pueden expandir en el índice especificando JET_bitIndexCrossProduct.

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Se implementa como <strong>JET_ INDEXCREATE2_W</strong> (Unicode) y <strong>JET_ INDEXCREATE2_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vea también

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
