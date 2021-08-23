---
description: El método MCSVC llama al método OnStatus para notificar al monitor que existe un evento de estado NPP. El monitor debe implementar este método.
ms.assetid: 771852b1-77d8-4d7d-b3fb-03eb3ea593b8
title: Método IMonitor::OnStatus (Netmon.h)
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
ms.openlocfilehash: 2a82594400bebc8a529290e0e0e881603172aa45c111d2d4d83ebcbd5ebfbeb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779045"
---
# <a name="imonitoronstatus-method"></a>IMonitor::OnStatus (método)

El método MCSVC llama al **método OnStatus** para notificar al monitor que existe un evento de estado NPP. El monitor debe implementar este método.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnStatus(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Evento* \[ En\]
</dt> <dd>

Una [estructura UPDATE \_ EVENT.](update-event.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es S OK (que es igual que NOERROR) y MCSVC devuelve el valor devuelto al NPP para su \_ procesamiento.

Si el método no es correcto, devuelva un código de error. En caso de error, MCSVC devuelve el valor devuelto al NPP para su procesamiento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




