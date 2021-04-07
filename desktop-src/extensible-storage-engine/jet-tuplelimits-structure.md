---
description: 'Más información acerca de: estructura de JET_TUPLELIMITS'
title: Estructura de JET_TUPLELIMITS
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
ms.openlocfilehash: 491f9248db607836b34f1fc0fcacc504b3c1d3f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003077"
---
# <a name="jet_tuplelimits-structure"></a>Estructura de JET_TUPLELIMITS


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_tuplelimits-structure"></a>Estructura de JET_TUPLELIMITS

La estructura de **JET_TUPLELIMITS** permite la personalización de las características del índice de tupla por índice, en lugar de por instancia, mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md).

**Windows Server 2003:** La estructura de **JET_TUPLELIMITS** se introduce en Windows Server 2003.

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

Longitud máxima de una cadena que se va a indizar. Por ejemplo, si una columna tiene una longitud de 100 caracteres y **chToIndexMax** está establecido en 60, solo se indexarán los primeros 60 caracteres de la columna. El valor predeterminado es 32767.

**cchIncrement**

Esto permite configurar el intervalo por índice.

**Windows Vista:** El miembro **cchIncrement** se introduce en Windows Vista. Antes de Windows Vista, la cantidad de desplazamiento de la ventana (el "intervalo") era siempre 1, como se muestra en el ejemplo de la sección Comentarios.

**ichStart**

Desplazamiento en el valor que se va a comenzar a recuperar las tuplas del valor.

**Windows Vista:** El miembro **ichStart** se introduce en Windows Vista.

### <a name="remarks"></a>Observaciones

Un índice de tupla recorre una cadena y indexa todas sus subcadenas posibles de **chLengthMax**. Al final de la cadena (o en la posición **chToIndexMax**, lo que ocurra primero), se indizarán las subcadenas de al menos **chLengthMin** .

Un índice de tupla se puede usar para buscar cadenas con caracteres comodín iniciales y finales.

Suponiendo que una fila tiene un campo de texto de "RAIN IN España \! ", si se crea un índice de tupla con los parámetros **chLengthMin**= 2 y **chLengthMax**= 3, se crean las siguientes entradas en el índice:

Rai  
UN valoren  
DE  
"N I"  
DE  
DE  
"N S"  
DAÑADO  
Spa  
"PAI"  
UN valoren  
"IN \! "  
"N \! "

Tenga en cuenta que "IN" se produce dos veces y que la última entrada ("N \! ") es más corta que 3 (**chLengthMax**). Tenga en cuenta también que el algoritmo de división no es compatible con espacios ni palabras, y trata todos los caracteres de forma idéntica.

**Windows XP:** Windows XP admite índices de tupla, pero no tiene **JET_TUPLELIMITS**. El motor de base de datos usará los valores predeterminados (**chLengthMin**= 3, **chLengthMax**= 10, **chToIndexMax**= 32767). Todavía es posible cambiar estos valores, pero se establecen en función de cada instancia mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md) con [JET_paramIndexTuplesLengthMin](./index-parameters.md), [JET_paramIndexTuplesLengthMax](./index-parameters.md)y [JET_paramIndexTuplesToIndexMax](./index-parameters.md).

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
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JET_COLTYP](./jet-coltyp.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TUPLELIMITS]()  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
