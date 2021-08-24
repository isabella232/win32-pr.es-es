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
ms.openlocfilehash: 41e5cfcc65c54f882f10e87a0f2aaebad0e1a55c94b6581031b034799987bc6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117956964"
---
# <a name="counteritemselected-property"></a>CounterItem.Selected, propiedad

Recupera o establece un valor que indica si el contador está seleccionado.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
Property Selected As Boolean
```



## <a name="property-value"></a>Valor de propiedad

True si el contador está seleccionado; de lo contrario, false.

## <a name="remarks"></a>Comentarios

Puede seleccionar uno o varios contadores de la colección de contadores. Al seleccionar un contador, selecciona el contador en leyenda, hace que el contador sea visible en la leyenda y genera un [**evento OnCounterSelected.**](-systemmonitor-oncounterselected.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> </dl>

 

 





