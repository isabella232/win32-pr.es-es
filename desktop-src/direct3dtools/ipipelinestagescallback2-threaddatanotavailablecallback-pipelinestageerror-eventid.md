---
description: Devolución de llamada que notifica al host que ThreadData no está disponible para una fase y un evento de canalización determinados.
MS-HAID: vspixengine.IPipeLineStagesCallback2\_ThreadDataNotAvailableCallback\_PipeLineStageError\_EventID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPipeLineStagesCallback2::ThreadDataNotAvailableCallback (método)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 231DC830-5F1A-4DDA-B5D0-C7FBCEDCB2A0
api_name:
- IPipeLineStagesCallback2.ThreadDataNotAvailableCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6e7f4f39a08e6370472fa54a41dbff41e21d38d3bbe994d124bdbf134cdd5dca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119484765"
---
# <a name="span-idvspixengineipipelinestagescallback2_threaddatanotavailablecallback_pipelinestageerror_eventidspanipipelinestagescallback2threaddatanotavailablecallback-method"></a><span id="vspixengine.ipipelinestagescallback2_threaddatanotavailablecallback_pipelinestageerror_eventid"></span>IPipeLineStagesCallback2::ThreadDataNotAvailableCallback (método)

Devolución de llamada que notifica al host que ThreadData no está disponible para una fase y un evento de canalización determinados.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ThreadDataNotAvailableCallback(
   PipeLineStageError error,
   EventID            eid
);
```

## <a name="parameters"></a>Parámetros

*Error*   
Error de la fase de canalización.

*Eid*   
Evento representado en los resultados.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IPipeLineStagesCallback2**](/windows/desktop/direct3dtools/ipipelinestagescallback2)

 

 
