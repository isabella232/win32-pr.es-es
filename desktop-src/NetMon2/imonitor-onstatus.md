---
description: El método MCSVC llama al método de estado para notificar al monitor que existe un evento de estado NPP. Este método debe ser implementado por el monitor.
ms.assetid: 771852b1-77d8-4d7d-b3fb-03eb3ea593b8
title: 'IMonitor:: alstatus (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStatus
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: fc2716a10673cc1178591b14a335b1d8559aa35a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155108"
---
# <a name="imonitoronstatus-method"></a>IMonitor:: alstatus (método)

El método MCSVC llama al método de **Estado** para notificar al monitor que existe un evento de estado NPP. Este método debe ser implementado por el monitor.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnStatus(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Evento* \[ de de\]
</dt> <dd>

Una estructura de [ \_ eventos de actualización](update-event.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es S \_ OK (que es igual que NoError) y MCSVC devuelve el valor devuelto a NPP para su procesamiento.

Si el método no se realiza correctamente, devuelve un código de error. En caso de error, MCSVC devuelve el valor devuelto a NPP para su procesamiento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




