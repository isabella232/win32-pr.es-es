---
title: CounterItem.Selected, propiedad
description: Recupera o establece un valor que indica si el contador está seleccionado.
ms.assetid: 293cc2ea-728c-4364-be2b-080bd188fe1c
keywords:
- Propiedad seleccionada SysMon
- Propiedad seleccionada SysMon , objeto CounterItem
- Objeto CounterItem SysMon , Propiedad seleccionada
topic_type:
- apiref
api_name:
- CounterItem.Selected
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac707dfaf2ed379884395a08128ddaeda771fa00
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068878"
---
# <a name="counteritemselected-property"></a>CounterItem.Selected, propiedad

Recupera o establece un valor que indica si el contador está seleccionado.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
Property Selected As Boolean
```



## <a name="property-value"></a>Valor de propiedad

True si el contador está seleccionado; de lo contrario, false.

## <a name="remarks"></a>Observaciones

Puede seleccionar uno o varios contadores de la colección de contadores. Al seleccionar un contador, selecciona el contador en leyenda, hace que el contador sea visible en la leyenda y genera un [**evento OnCounterSelected.**](-systemmonitor-oncounterselected.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> </dl>

 

 





