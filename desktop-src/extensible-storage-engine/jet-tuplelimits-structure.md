---
description: 'Más información sobre: JET_TUPLELIMITS estructura'
title: JET_TUPLELIMITS estructura
TOCTitle: JET_TUPLELIMITS Structure
ms:assetid: 2610e2e5-5883-4aec-bc66-e6160b76c264
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269207(v=EXCHG.10)
ms:contentKeyID: 32765510
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c4e2c118b7b42dce82ec0a95c53853ec501a7152c08ad088bbddde251edadf3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119472695"
---
# <a name="jet_tuplelimits-structure"></a>JET_TUPLELIMITS estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_tuplelimits-structure"></a>JET_TUPLELIMITS estructura

La **JET_TUPLELIMITS** estructura permite la personalización de las características del índice de tupla por índice, en lugar de por instancia, mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md).

**Windows Server 2003:** La **JET_TUPLELIMITS** se introduce en Windows Server 2003.

```cpp
    typedef struct tagJET_TUPLELIMITS {
      unsigned long chLengthMin;
      unsigned long chLengthMax;
      unsigned long chToIndexMax;
      unsigned long cchIncrement;
      unsigned long ichStart;
    } JET_TUPLELIMITS;
```

### <a name="members"></a>Miembros

**chLengthMin**

Longitud mínima de una tupla. El valor predeterminado es 3.

**chLengthMax**

Longitud máxima de una tupla. El valor predeterminado es 10.

**chToIndexMax**

Longitud máxima de una cadena que se indexa. Por ejemplo, si una columna tiene 100 caracteres y **chToIndexMax** se establece en 60, solo se indexarán los primeros 60 caracteres de la columna. El valor predeterminado es 32767.

**cchIncrement**

Esto permite configurar el paso por índice.

**Windows Vista:** El **miembro cchIncrement** se introdujo en Windows Vista. Antes de Windows Vista, la cantidad para desplazar la ventana (el "paso") siempre era 1, como se muestra en el ejemplo en la sección de comentarios.

**ichStart**

Desplazamiento en el valor para empezar a recuperar tuplas del valor.

**Windows Vista:** El **miembro ichStart** se introdujo en Windows Vista.

### <a name="remarks"></a>Comentarios

Un índice de tupla recorre una cadena e indexa todas sus subcadenas posibles de **chLengthMax.** Al final de la cadena (o en la posición **chToIndexMax,** lo que ocurra primero), se indexarán las subcadenas de al menos **chLengthMin.**

Se puede usar un índice de tupla para buscar cadenas con caracteres comodín iniciales y finales.

Suponiendo una fila con un campo de texto de "RAIN IN SPAIN", si se crea un índice de tupla con los parámetros \! **chLengthMin**=2 y **chLengthMax**=3, se crean las siguientes entradas en el índice:

"RAI"  
"SUDA"  
"IN"  
"N I"  
"IN"  
"IN"  
"N S"  
"SP"  
"SPA"  
"HAN"  
"SUDA"  
\!"IN"  
\!"N"

Tenga en cuenta que "IN" se produce dos veces y que la última entrada ("N ") es menor \! que 3 (**chLengthMax**). Tenga en cuenta también que el algoritmo de división no es consciente de los espacios o palabras y trata todos los caracteres de forma idéntica.

**Windows XP:** Windows XP admite índices de tupla, pero no **tiene JET_TUPLELIMITS**. El motor de base de datos usará los valores predeterminados (**chLengthMin**=3, **chLengthMax**=10, **chToIndexMax**=32767). Todavía es posible cambiar estos valores, pero se establecen por instancia mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md) con [JET_paramIndexTuplesLengthMin](./index-parameters.md), [JET_paramIndexTuplesLengthMax](./index-parameters.md)y [JET_paramIndexTuplesToIndexMax](./index-parameters.md).

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en Esent.h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JET_COLTYP](./jet-coltyp.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TUPLELIMITS]()  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
