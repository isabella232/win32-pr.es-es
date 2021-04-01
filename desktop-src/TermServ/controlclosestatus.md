---
title: Enumeración ControlCloseStatus
description: Indica si la aplicación que contiene el control puede cerrar el control inmediatamente.
ms.assetid: ac2e1c68-81b1-4b51-aa7e-0ff703e619a2
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto enumeración ControlCloseStatus
topic_type:
- apiref
api_name:
- ControlCloseStatus
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b94e0ce5cd040a2ade970f566897d2eac339dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996025"
---
# <a name="controlclosestatus-enumeration"></a>Enumeración ControlCloseStatus

Indica si la aplicación que contiene el control puede cerrar el control inmediatamente.

## <a name="syntax"></a>Sintaxis


```C++
enum ControlCloseStatus {
  controlCloseCanProceed     = 0x0000, 
  controlCloseWaitForEvents  = 0x0001 

};
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed**
</dt> <dd>

El contenedor puede continuar con el cierre inmediatamente. Esto puede ocurrir si el control no está conectado.

</dd> <dt>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents**
</dt> <dd>

El contenedor debe esperar los eventos [**IMsTscAxEvents:: OnDisconnect**](imstscaxevents-ondisconnected.md) o [**IMsTscAxEvents:: OnConfirmClose**](imstscaxevents-onconfirmclose.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                      |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClient::RequestClose**](imsrdpclient-requestclose.md)
</dt> <dt>

[**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md)
</dt> <dt>

[**IMsTscAxEvents:: OnDisconnection**](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

 





