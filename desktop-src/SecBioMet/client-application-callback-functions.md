---
title: Funciones de devolución de llamada de aplicación cliente
description: Dos tipos de firmas de devolución de llamada.
ms.assetid: 5569BFF3-9EEC-42E6-8F63-0C569C68FA74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f3e052df1821a5fd85bbba4ebbea3e6672d9e625b7d4258110fb19a5c234f4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977105"
---
# <a name="client-application-callback-functions"></a>Funciones de devolución de llamada de aplicación cliente

El Windows Biometric Framework admite dos tipos de firmas de devolución de llamada. A partir Windows 8, se admite la devolución de llamada siguiente. Se recomienda implementar esta devolución de llamada para todas las aplicaciones nuevas. Sin embargo, esta devolución de llamada no se puede usar en Windows 7.



| Devolución de llamada                                                                                     | Descripción                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DEVOLUCIÓN DE LLAMADA \_ DE FINALIZACIÓN \_ ASINCRÓNICA \_ DE PWINBIO**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_async_completion_callback)<br/> | Notifica a la aplicación cliente que se ha completado una operación asincrónica iniciada mediante [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession) o [**WinBioAsyncOpenFramework.**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopenframework)<br/> |



 

Las siguientes funciones de devolución de llamada se introdujeron en Windows 7. Se recomienda no implementarlas para nuevas aplicaciones que tienen como destino Windows 8 sistemas operativos posteriores.



| Devolución de llamada                                                                                 | Descripción                                                                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**DEVOLUCIÓN DE LLAMADA \_ DE CAPTURA DE PWINBIO \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_capture_callback)<br/>                | Devuelve los resultados de la [**función asincrónica WinBioCaptureSampleWithCallback.**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesamplewithcallback)<br/> |
| [**DEVOLUCIÓN DE LLAMADA DE CAPTURA DE INSCRIPCIÓN \_ \_ DE PWINBIO \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_enroll_capture_callback)<br/> | Devuelve los resultados de la [**función asincrónica WinBioEnrollCaptureWithCallback.**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback)<br/> |
| [**DEVOLUCIÓN DE LLAMADA \_ DE EVENTOS \_ PWINBIO**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_event_callback)<br/>                    | Devuelve los resultados de la [**función asincrónica WinBioRegisterEventMonitor.**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor)<br/>           |
| [**PWINBIO \_ IDENTIFY \_ CALLBACK**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_identify_callback)<br/>              | Devuelve los resultados de la [**función asincrónica WinBioIdentifyWithCallback.**](/windows/desktop/api/Winbio/nf-winbio-winbioidentifywithcallback)<br/>           |
| [**DEVOLUCIÓN DE LLAMADA DEL SENSOR DE PWINBIO \_ \_ \_ LOCATE**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_locate_sensor_callback)<br/>   | Devuelve los resultados de la [**función asincrónica WinBioLocateSensorWithCallback.**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback)<br/>   |
| [**DEVOLUCIÓN DE LLAMADA \_ DE COMPROBACIÓN DE PWINBIO \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_verify_callback)<br/>                  | Devuelve los resultados de la [**función asincrónica WinBioVerifyWithCallback.**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback)<br/>               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de la aplicación cliente](client-application-reference.md)
</dt> </dl>

 

 





