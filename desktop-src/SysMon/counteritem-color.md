---
title: CounterItem.Color, propiedad
description: Recupera o establece el color utilizado para representar el valor del contador.
ms.assetid: 73630efc-3128-4db5-b64c-ebb2f5e7611a
keywords:
- Propiedad de color SysMon
- Propiedad de color SysMon , clase CounterItem
- Clase CounterItem SysMon, propiedad Color
topic_type:
- apiref
api_name:
- CounterItem.Color
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcc51862c57312f9b923ea6a80f9814182bbc6aef707dab994b135ace9637754
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883886"
---
# <a name="counteritemcolor-property"></a>CounterItem.Color, propiedad

Recupera o establece el color utilizado para representar el valor del contador.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
Property Color As stdole.OLE_COLOR
```



## <a name="property-value"></a>Valor de propiedad

Color utilizado para representar el valor del contador.

## <a name="remarks"></a>Comentarios

Si no especifica el color que se va a usar, SYSMON selecciona los colores de los primeros dieciséis contadores. Si especifica más de 16 contadores, SYSMON reutilizará los mismos colores de los primeros dieciséis contadores. Para ayudar a distinguir los contadores entre [](counteritem-linestyle.md) sí, SYSMON cambia el estilo de línea usado para cada múltiplo de dieciséis contadores hasta los primeros 80 contadores. Por ejemplo, los primeros dieciséis contadores usan un estilo de línea sólido, los dieciséis siguientes usan un estilo de línea discontinua, y así sucesivamente. A continuación, [](counteritem-width.md) SYSMON establece el ancho de línea en 2 para los contadores 81 - 96 y en 3 para los contadores 96 - 112. Si la colección contiene más de 112 contadores, los contadores contendrán valores duplicados de color, estilo de línea y ancho.

**Antes de Windows Vista:** Si no especifica el color que se va a usar, SYSMON selecciona los colores de los primeros dieciséis contadores. Si especifica más de 16 contadores, SYSMON reutilizará los mismos colores de los primeros dieciséis contadores. Para ayudar a distinguir los contadores entre [](counteritem-width.md) sí, SYSMON aumenta el ancho de línea de los tres primeros contadores que reciben la misma asignación de color. Si más de tres contadores usan el mismo color, SYSMON elige aleatoriamente el ancho de línea que se usará para el contador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> </dl>

 

 





