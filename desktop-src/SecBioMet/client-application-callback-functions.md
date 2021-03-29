---
title: Funciones de devolución de llamada de aplicación cliente
description: Dos tipos de firmas de devolución de llamada.
ms.assetid: 5569BFF3-9EEC-42E6-8F63-0C569C68FA74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371edd162c4cbd1332764c7b3e9e70bf114270e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419003"
---
# <a name="client-application-callback-functions"></a>Funciones de devolución de llamada de aplicación cliente

El Plataforma de biometría de Windows admite dos tipos de firmas de devolución de llamada. A partir de Windows 8, se admite la siguiente devolución de llamada. Se recomienda implementar esta devolución de llamada para todas las aplicaciones nuevas. No obstante, esta devolución de llamada no se puede usar en Windows 7.



| Devolución de llamada                                                                                     | Descripción                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_devolución de \_ llamada de finalización ASINCRÓNICA de PWINBIO \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_async_completion_callback)<br/> | Notifica a la aplicación cliente que se ha completado una operación asincrónica iniciada mediante [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession) o [**WinBioAsyncOpenFramework**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopenframework) .<br/> |



 

Las siguientes funciones de devolución de llamada se introdujeron en Windows 7. Se recomienda no implementarlas para las nuevas aplicaciones destinadas a Windows 8 y sistemas operativos posteriores.



| Devolución de llamada                                                                                 | Descripción                                                                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**devolución de llamada de \_ captura PWINBIO \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_capture_callback)<br/>                | Devuelve los resultados de la función [**WinBioCaptureSampleWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesamplewithcallback) asincrónica.<br/> |
| [**\_devolución de \_ llamada de captura de inscripción de PWINBIO \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_enroll_capture_callback)<br/> | Devuelve los resultados de la función [**WinBioEnrollCaptureWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback) asincrónica.<br/> |
| [**devolución de llamada de \_ evento PWINBIO \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_event_callback)<br/>                    | Devuelve los resultados de la función [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) asincrónica.<br/>           |
| [**PWINBIO \_ identificar \_ devolución de llamada**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_identify_callback)<br/>              | Devuelve los resultados de la función [**WinBioIdentifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioidentifywithcallback) asincrónica.<br/>           |
| [**PWINBIO \_ Buscar \_ devolución de llamada del sensor \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_locate_sensor_callback)<br/>   | Devuelve los resultados de la función [**WinBioLocateSensorWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback) asincrónica.<br/>   |
| [**PWINBIO \_ comprobar \_ devolución de llamada**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_verify_callback)<br/>                  | Devuelve los resultados de la función [**WinBioVerifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback) asincrónica.<br/>               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de la aplicación cliente](client-application-reference.md)
</dt> </dl>

 

 





