---
description: 'Más información acerca de: OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION'
ms.assetid: 71fa9a99-83e4-4b27-9fd1-5a9dc3070820
title: OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7561a348588b1244a6763eb447affa2b330e9c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543870"
---
# <a name="opm_get_connected_hdcp_device_information"></a>\_información de \_ \_ dispositivo HDCP \_ conectado \_ a OPM

Obtiene información acerca de un dispositivo High-Bandwidth Digital Content Protection (HDCP) conectado a la salida de vídeo. Se devuelve la siguiente información:

-   Vector de selección de clave de HDCP del dispositivo (KSV).
-   Si el dispositivo es un repetidor de HDCP.



| Requisito | Value |
|--------------|---------------------------------------------------------------------------------------------------------|
| GUID de solicitud | \_información de \_ \_ dispositivo HDCP \_ conectado \_ a OPM                                                          |
| Datos de entrada   | None                                                                                                    |
| Devolver datos  | Una estructura de [**\_ \_ \_ \_ información del dispositivo HDCP conectada a OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information) |



 

## <a name="remarks"></a>Observaciones

Esta consulta solo se puede usar con el *modo de emulación de COPP*. Si la interfaz [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) usa la semántica de administrador de protección de salida (OPM), esta solicitud de estado no se admite.

KSV es un identificador proporcionado al fabricante del dispositivo y se usa en el proceso de autenticación y configuración de HDCP. En el modo de emulación de COPP, la aplicación usa KSV para determinar si el dispositivo HDCP está revocado. Si es así, la aplicación no debería reproducir contenido protegido. Además, la aplicación no debe reproducir contenido protegido si el dispositivo es un repetidor de HDCP, porque COPP no admite repetidores de HDCP.

Esta consulta no es necesaria cuando se usan semánticas de OPM, porque OPM admite repetidores de devocación de dispositivos y de HDCP.

Esta consulta es equivalente a la \_ consulta COPPQueryHDCPKeyData de DXVA usada en el protocolo de protección de la salida certificada (COPP).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IOPMVideoOutput:: COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[Solicitudes de estado de OPM](opm-status-requests.md)
</dt> </dl>

 

 




