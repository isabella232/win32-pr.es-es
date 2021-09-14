---
title: WINBIO_EVENT constantes (Winbio \_ types.h)
description: Especifique los tipos de notificaciones de eventos del proveedor de servicios que se supervisarán.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071148"
---
# <a name="winbio_event-constants"></a>Constantes \_ DE EVENTOS WINBIO

Las siguientes constantes se pueden usar en la [**función WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) para especificar los tipos de notificaciones de eventos del proveedor de servicios que se deben supervisar.



| Constante                                                                                                                                                                                                                        | Descripción                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span><dl> <dt>**EVENTO DE WINBIO \_ \_ FP NO \_ RECLAMADO**</dt> </dl>                             | El sensor detectó un deslizamiento de dedo que no fue solicitado por la aplicación o por la ventana que actualmente tiene el foco. El Windows Biometric Framework llama a la función de devolución de llamada para indicar que se ha producido un deslizamiento de dedo, pero no intenta identificar la huella digital.<br/> |
| <span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span><dl> <dt>**IDENTIFICACIÓN NO \_ \_ RECLAMADA DEL EVENTO DE WINBIO FP \_ \_**</dt> </dl> | El sensor detectó un deslizamiento de dedo que no fue solicitado por la aplicación o por la ventana que actualmente tiene el foco. El Windows Biometric Framework intenta identificar la huella digital y pasa el resultado de ese proceso a la función de devolución de llamada.<br/>                        |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de aplicación cliente](client-application-constants.md)
</dt> </dl>

 

 





