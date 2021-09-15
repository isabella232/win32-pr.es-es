---
description: Devuelve el número de versión del mensaje de renovación del sistema (SRM) utilizado actualmente por la salida de vídeo.
ms.assetid: 65d4b98b-369f-4863-a28c-f9e3b4c2b55d
title: OPM_GET_CURRENT_HDCP_SRM_VERSION (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e05ad53ae58e2141c63179c84a90f90cea86fb4a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574836"
---
# <a name="opm_get_current_hdcp_srm_version"></a>OPM \_ GET \_ CURRENT \_ HDCP \_ SRM \_ VERSION

Devuelve el número de versión del mensaje de renovación del sistema (SRM) utilizado actualmente por la salida de vídeo.



| Requisito | Value |
|--------------|-----------------------------------------------------------------------------|
| GUID de solicitud | OPM \_ GET \_ CURRENT \_ HDCP \_ SRM \_ VERSION                                       |
| Datos de entrada   | None                                                                        |
| Devolver datos  | Una [**estructura OPM \_ STANDARD \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Observaciones

Si esta consulta se realiza correctamente, el miembro **ulInformation** de la estructura [**OPM \_ STANDARD \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) contiene el número de versión de SRM, en formato little-endian.

Las SRE se usan para actualizar la lista de dispositivos High-Bandwidth Digital Content Protection (HDCP) revocados. Las SRE se entregan con el contenido del vídeo. Para establecer el SRM, envíe el comando [**OPM \_ SET \_ HDCP \_ SRM.**](opm-set-hdcp-srm.md)

Esta consulta puede hacer que [**el método IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) devuelva cualquiera de los siguientes códigos de error.



| Código devuelto                                            | Descripción                             |
|--------------------------------------------------------|-----------------------------------------|
| GRÁFICOS \_ DE \_ ERROR OPM \_ HDCP \_ SRM NEVER \_ \_ SET            | La aplicación no estableció un SRM.     |
| SALIDA \_ DE \_ OPM DE \_ \_ GRÁFICOS DE ERROR NO ADMITE \_ \_ \_ HDCP | La salida de vídeo no admite HDCP. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Solicitudes de estado de OPM](opm-status-requests.md)
</dt> </dl>

 

 




