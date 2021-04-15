---
description: Devuelve el número de versión del mensaje de renovación de sistema (SRM) que usa actualmente la salida de vídeo.
ms.assetid: 65d4b98b-369f-4863-a28c-f9e3b4c2b55d
title: OPM_GET_CURRENT_HDCP_SRM_VERSION (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e05ad53ae58e2141c63179c84a90f90cea86fb4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715527"
---
# <a name="opm_get_current_hdcp_srm_version"></a>\_obtener la \_ versión actual de \_ HDCP de HDCP \_ \_

Devuelve el número de versión del mensaje de renovación de sistema (SRM) que usa actualmente la salida de vídeo.



| Requisito | Value |
|--------------|-----------------------------------------------------------------------------|
| GUID de solicitud | \_obtener la \_ versión actual de \_ HDCP de HDCP \_ \_                                       |
| Datos de entrada   | None                                                                        |
| Devolver datos  | Una estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Observaciones

Si esta consulta se realiza correctamente, el miembro **ulInformation** de la estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) contiene el número de versión de SRM, en formato Little-Endian.

SRMs se usan para actualizar la lista de dispositivos revocados High-Bandwidth Digital Content Protection (HDCP). SRMs se entregan con el contenido del vídeo. Para establecer el SRM, envíe el comando [**OPM \_ set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) .

Esta consulta puede hacer que el método [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) devuelva cualquiera de los siguientes códigos de error.



| Código devuelto                                            | Descripción                             |
|--------------------------------------------------------|-----------------------------------------|
| gráficos de ERROR: no se ha \_ \_ \_ \_ \_ establecido nunca la SRM de HDCP \_            | La aplicación no estableció una SRM.     |
| el resultado de los gráficos de ERROR \_ \_ OPM \_ no es \_ \_ \_ compatible con \_ HDCP | La salida de vídeo no es compatible con HDCP. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Solicitudes de estado de OPM](opm-status-requests.md)
</dt> </dl>

 

 




