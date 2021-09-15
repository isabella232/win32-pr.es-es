---
description: Actualiza el mensaje de renovación del sistema (SRM) para High-Bandwidth Digital Content Protection (HDCP).
ms.assetid: ea18baba-0e03-4471-af0e-a588773c98d2
title: OPM_SET_HDCP_SRM (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9283c493598f22a1715f687eccea985a27e0e6f0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467207"
---
# <a name="opm_set_hdcp_srm"></a>OPM \_ SET \_ HDCP \_ SRM

Actualiza el mensaje de renovación del sistema (SRM) para High-Bandwidth Digital Content Protection (HDCP).



| Requisito | Value |
|--------------|-------------------------------------------------------------------------------------|
| GUID del comando | OPM \_ SET \_ HDCP \_ SRM                                                                 |
| Datos de entrada   | Estructura [**OPM \_ SET \_ HDCP \_ SRM \_ PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters) |



 

El *parámetro pbAdditionalParameters* de [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) debe apuntar a un búfer que contenga el SRM. El formato de un SRM de HDCP se documenta en la especificación de HDCP. Establezca el *parámetro ulAdditionalParametersSize* igual al tamaño del búfer, en bytes.

## <a name="remarks"></a>Observaciones

Las SRE se usan para actualizar la lista de dispositivos HDCP revocados. Las SRE se entregan con el contenido del vídeo.

Este comando actualiza el SRM actual de la salida de vídeo. Si HDCP está habilitado en el momento del comando, la salida de vídeo usa el nuevo SRM para comprobar si se revoca cualquiera de los dispositivos HDCP conectados. Si la salida de vídeo detecta un dispositivo revocado, deja de mostrar el vídeo. Si envía este comando mientras HDCP está deshabilitado, la salida de vídeo valida el SRM y lo almacena. Más adelante, si la aplicación habilita HDCP, la salida de vídeo usa el nuevo SRM para comprobar el estado de revocación del dispositivo.

Este comando puede hacer que **el método Configure** devuelva cualquiera de los siguientes códigos de error.



| Código devuelto                                            | Descripción                             |
|--------------------------------------------------------|-----------------------------------------|
| ERROR \_ GRAPHICS \_ OPM \_ INVALID \_ SRM                     | El SRM no es válido.                   |
| LA \_ SALIDA \_ DE OPM DE \_ \_ GRÁFICOS DE ERROR NO ADMITE \_ \_ \_ HDCP | La salida de vídeo no admite HDCP. |



 

Este comando no se admite cuando la **interfaz IOPMVideoOutput** emula el Protocolo de protección de salida certificado (COPP). Cuando se usa la semántica de COPP, la aplicación es responsable de analizar las SRE y comprobar el estado de revocación del dispositivo HDCP. Use la [solicitud de estado OPM GET CONNECTED \_ \_ \_ HDCP DEVICE \_ \_ INFORMATION](opm-get-connected-hdcp-device-information.md) para obtener el vector de selección de claves (KSV) del dispositivo, que es necesario para comprobar el estado de revocación. Para más información sobre las SRE, consulte la especificación de HDCP.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[Comandos de OPM](opm-commands.md)
</dt> </dl>

 

 




