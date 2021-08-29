---
title: Enumeración ControlCloseStatus
description: Indica si la aplicación que contiene el control puede cerrar el control inmediatamente.
ms.assetid: ac2e1c68-81b1-4b51-aa7e-0ff703e619a2
ms.tgt_platform: multiple
keywords:
- Enumeración ControlCloseStatus Servicios de Escritorio remoto
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
ms.openlocfilehash: e663ce5f6b8fd4536942bd9426c230255aa5132c04a3e2ed0133d6d32d4e6272
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119401625"
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

El contenedor puede continuar con el cierre inmediato. Esto puede ocurrir si el control no está conectado.

</dd> <dt>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents**
</dt> <dd>

El contenedor debe esperar los eventos [**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md) o [**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                      |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClient::RequestClose**](imsrdpclient-requestclose.md)
</dt> <dt>

[**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md)
</dt> <dt>

[**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

 





