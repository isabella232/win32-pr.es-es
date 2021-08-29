---
description: El método SendNMEvent envía eventos a Windows Management Instrumentation (WMI).
ms.assetid: 85c33a71-72aa-4b0a-8e8b-3a220a080bb2
title: Método IMonitorEventer::SendNMEvent (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.SendNMEvent
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: a922dbbd3e31fc344383016416f139424fd5782e9bf92268e3fb4ff1dc7f93b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037365"
---
# <a name="imonitoreventersendnmevent-method"></a>IMonitorEventer::SendNMEvent (método)

El **método SendNMEvent** envía eventos a Windows Management Instrumentation (WMI).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SendNMEvent(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pNMEventData* \[ En\]
</dt> <dd>

Puntero al evento enviado a WMI.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es S \_ OK.

Si el método no es correcto, el valor devuelto es NMERR \_ OUT \_ OF \_ MEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




