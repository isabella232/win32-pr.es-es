---
description: Actualiza el mensaje de renovación de sistema (SRM) para High-Bandwidth Digital Content Protection (HDCP).
ms.assetid: ea18baba-0e03-4471-af0e-a588773c98d2
title: OPM_SET_HDCP_SRM (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9283c493598f22a1715f687eccea985a27e0e6f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275828"
---
# <a name="opm_set_hdcp_srm"></a>OPM \_ set \_ HDCP \_ SRM

Actualiza el mensaje de renovación de sistema (SRM) para High-Bandwidth Digital Content Protection (HDCP).



| Requisito | Value |
|--------------|-------------------------------------------------------------------------------------|
| GUID de comando | OPM \_ set \_ HDCP \_ SRM                                                                 |
| Datos de entrada   | Una estructura de [**\_ parámetros de SRM de set \_ HDCP \_ \_ de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters) |



 

El parámetro *pbAdditionalParameters* de [**IOPMVideoOutput:: configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) debe apuntar a un búfer que contenga la SRM. El formato de una SRM de HDCP se documenta en la especificación de HDCP. Establezca el parámetro *ulAdditionalParametersSize* en el tamaño del búfer, en bytes.

## <a name="remarks"></a>Observaciones

SRMs se usan para actualizar la lista de dispositivos HDCP revocados. SRMs se entregan con el contenido del vídeo.

Este comando actualiza el SRM actual de la salida de vídeo. Si se habilita HDCP en el momento del comando, la salida de vídeo usa el nuevo SRM para comprobar si alguno de los dispositivos HDCP conectados está revocado. Si la salida de vídeo detecta un dispositivo revocado, deja de mostrar vídeo. Si envía este comando mientras HDCP está deshabilitado, la salida de vídeo valida el SRM y lo almacena. Más adelante, si la aplicación habilita HDCP, la salida de vídeo usa el nuevo SRM para comprobar el estado de revocación del dispositivo.

Este comando puede hacer que el método **Configure** devuelva alguno de los siguientes códigos de error.



| Código devuelto                                            | Descripción                             |
|--------------------------------------------------------|-----------------------------------------|
| ERROR en el \_ \_ \_ SRM no válido de los gráficos OPM \_                     | El SRM no es válido.                   |
| el resultado de los gráficos de ERROR \_ \_ OPM \_ no es \_ \_ \_ compatible con \_ HDCP | La salida de vídeo no es compatible con HDCP. |



 

Este comando no se admite cuando la interfaz **IOPMVideoOutput** emula el protocolo de protección de la salida (COPP). Cuando se usan semánticas de COPP, la aplicación es responsable de analizar SRMs y comprobar el estado de revocación del dispositivo HDCP. Use la solicitud de estado de [ \_ \_ \_ \_ \_ información del dispositivo HDCP Get Connected HDCP](opm-get-connected-hdcp-device-information.md) para obtener el vector de selección de clave (KSV) del dispositivo, que es necesario para comprobar el estado de revocación. Para obtener más información sobre SRMs, consulte la especificación de HDCP.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IOPMVideoOutput:: configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[Comandos OPM](opm-commands.md)
</dt> </dl>

 

 




