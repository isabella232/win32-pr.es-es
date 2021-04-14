---
title: Constantes de WINBIO_EVENT (Winbio \_ Types. h)
description: Especifique los tipos de notificaciones de eventos del proveedor de servicios que se van a supervisar.
ms.assetid: 73805413-a8d9-4682-aa21-7032451d750a
topic_type:
- apiref
api_name:
- WINBIO_EVENT_FP_UNCLAIMED
- WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 182a4ffe254e946f1b8deca2c5034e665a58f7ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533861"
---
# <a name="winbio_event-constants"></a>\_Constantes de evento WINBIO

Se pueden usar las siguientes constantes en la función [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) para especificar los tipos de notificaciones de eventos del proveedor de servicios que se van a supervisar.



| Constante                                                                                                                                                                                                                        | Descripción                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span><dl> <dt>**\_evento WINBIO \_ FP no \_ reclamado**</dt> </dl>                             | El sensor ha detectado un dedo deslizante que no ha solicitado la aplicación o que la ventana tiene el foco actualmente. El Plataforma de biometría de Windows llama a la función de devolución de llamada para indicar que se ha producido un deslizamiento de dedo pero no intenta identificar la huella digital.<br/> |
| <span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span><dl> <dt>**\_identificación no \_ \_ reclamada del evento WINBIO FP \_**</dt> </dl> | El sensor ha detectado un dedo deslizante que no ha solicitado la aplicación o que la ventana tiene el foco actualmente. El Plataforma de biometría de Windows intenta identificar la huella digital y pasa el resultado de ese proceso a la función de devolución de llamada.<br/>                        |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Types. h (incluye Winbio. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de aplicación cliente](client-application-constants.md)
</dt> </dl>

 

 





