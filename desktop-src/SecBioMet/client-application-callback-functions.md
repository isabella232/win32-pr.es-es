---
title: Funciones de devolución de llamada de aplicación cliente
description: Dos tipos de firmas de devolución de llamada.
ms.assetid: 5569BFF3-9EEC-42E6-8F63-0C569C68FA74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371edd162c4cbd1332764c7b3e9e70bf114270e7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253586"
---
# <a name="client-application-callback-functions"></a>Funciones de devolución de llamada de aplicación cliente

El Windows Biometric Framework admite dos tipos de firmas de devolución de llamada. A partir Windows 8, se admite la devolución de llamada siguiente. Se recomienda implementar esta devolución de llamada para todas las aplicaciones nuevas. Sin embargo, esta devolución de llamada no se puede usar en Windows 7.



| Devolución de llamada                                                                                     | Descripción                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DEVOLUCIÓN DE LLAMADA \_ DE FINALIZACIÓN ASINCRÓNICA \_ \_ DE PWINBIO**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_async_completion_callback)<br/> | Notifica a la aplicación cliente que se ha completado una operación asincrónica iniciada mediante [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession) o [**WinBioAsyncOpenFramework.**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopenframework)<br/> |



 

Las siguientes funciones de devolución de llamada se introdujeron en Windows 7. Se recomienda no implementarlas para nuevas aplicaciones destinadas a Windows 8 sistemas operativos posteriores.



| Devolución de llamada                                                                                 | Descripción                                                                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**DEVOLUCIÓN DE LLAMADA \_ DE CAPTURA DE PWINBIO \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_capture_callback)<br/>                | Devuelve los resultados de la [**función asincrónica WinBioCaptureSampleWithCallback.**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesamplewithcallback)<br/> |
| [**DEVOLUCIÓN DE LLAMADA DE CAPTURA DE INSCRIPCIÓN DE PWINBIO \_ \_ \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_enroll_capture_callback)<br/> | Devuelve los resultados de la [**función asincrónica WinBioEnrollCaptureWithCallback.**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback)<br/> |
| [**DEVOLUCIÓN DE LLAMADA \_ DE EVENTOS \_ PWINBIO**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_event_callback)<br/>                    | Devuelve los resultados de la [**función asincrónica WinBioRegisterEventMonitor.**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor)<br/>           |
| [**DEVOLUCIÓN DE LLAMADA \_ DE IDENTIFICACIÓN DE PWINBIO \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_identify_callback)<br/>              | Devuelve los resultados de la [**función asincrónica WinBioIdentifyWithCallback.**](/windows/desktop/api/Winbio/nf-winbio-winbioidentifywithcallback)<br/>           |
| [**DEVOLUCIÓN DE LLAMADA DEL SENSOR DE PWINBIO \_ LOCATE \_ \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_locate_sensor_callback)<br/>   | Devuelve los resultados de la [**función asincrónica WinBioLocateSensorWithCallback.**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback)<br/>   |
| [**DEVOLUCIÓN DE LLAMADA \_ DE COMPROBACIÓN DE PWINBIO \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_verify_callback)<br/>                  | Devuelve los resultados de la [**función asincrónica WinBioVerifyWithCallback.**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback)<br/>               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de la aplicación cliente](client-application-reference.md)
</dt> </dl>

 

 





