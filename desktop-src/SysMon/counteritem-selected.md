---
title: Propiedad de peritem. Selected
description: Recupera o establece un valor que indica si el contador está seleccionado.
ms.assetid: 293cc2ea-728c-4364-be2b-080bd188fe1c
keywords:
- Propiedad seleccionada SysMon
- Propiedad seleccionada SysMon, objeto de contraelemento
- Objeto de perelemento SysMon, propiedad seleccionada
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996495"
---
# <a name="counteritemselected-property"></a>Propiedad de peritem. Selected

Recupera o establece un valor que indica si el contador está seleccionado.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
Property Selected As Boolean
```



## <a name="property-value"></a>Valor de propiedad

True si el contador está seleccionado; en caso contrario, false.

## <a name="remarks"></a>Observaciones

Puede seleccionar uno o varios contadores de la colección de contadores. Seleccionar un contador, selecciona el contador en la leyenda, hace que el contador esté visible en la leyenda y genera un evento [**OnCounterSelected**](-systemmonitor-oncounterselected.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento de**](counteritem.md)
</dt> </dl>

 

 





