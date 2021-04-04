---
title: Propiedad de contraelemento. color
description: Recupera o establece el color utilizado para representar el valor del contador en el gráfico.
ms.assetid: 73630efc-3128-4db5-b64c-ebb2f5e7611a
keywords:
- Propiedad de color SysMon
- Propiedad color SysMon, clase de contraelemento
- Clase de contraelemento SysMon, propiedad de color
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
ms.openlocfilehash: ada0a2266c4cf53e9706f1330e2336e6a38386b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802588"
---
# <a name="counteritemcolor-property"></a>Propiedad de contraelemento. color

Recupera o establece el color utilizado para representar el valor del contador en el gráfico.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
Property Color As stdole.OLE_COLOR
```



## <a name="property-value"></a>Valor de propiedad

Color que se usa para representar el valor del contador.

## <a name="remarks"></a>Observaciones

Si no especifica el color que se va a usar, SYSMON selecciona los colores de los primeros dieciséis contadores. Si especifica más de dieciséis contadores, SYSMON volverá a usar los mismos colores de los primeros dieciséis contadores. Para ayudar a distinguir los contadores entre sí, SYSMON cambia el [**estilo de línea**](counteritem-linestyle.md) usado para cada múltiplo de dieciséis contadores hasta los primeros 80 contadores. Por ejemplo, los primeros dieciséis contadores usan un estilo de línea continua, los siguientes dieciséis usan un estilo de línea de guiones, etc. SYSMON establece el [**ancho de línea**](counteritem-width.md) en 2 para los contadores 81-96 y en 3 para los contadores 96-112. Si la colección contiene más de 112 contadores, los contadores contendrán los valores de color, estilo de línea y ancho duplicados.

**Antes de Windows Vista:** Si no especifica el color que se va a usar, SYSMON selecciona los colores de los primeros dieciséis contadores. Si especifica más de dieciséis contadores, SYSMON volverá a usar los mismos colores de los primeros dieciséis contadores. Para ayudar a distinguir los contadores entre sí, SYSMON aumenta el [**ancho de línea**](counteritem-width.md) de los tres primeros contadores que reciben la misma asignación de color. Si más de tres contadores usan el mismo color, SYSMON elige aleatoriamente el ancho de línea que se va a usar para el contador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento de**](counteritem.md)
</dt> </dl>

 

 





