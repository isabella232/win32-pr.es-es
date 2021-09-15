---
description: 'Más información sobre: OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION'
ms.assetid: 71fa9a99-83e4-4b27-9fd1-5a9dc3070820
title: OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7561a348588b1244a6763eb447affa2b330e9c51
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574840"
---
# <a name="opm_get_connected_hdcp_device_information"></a>OPM \_ GET \_ CONNECTED \_ HDCP \_ DEVICE \_ INFORMATION

Obtiene información sobre un High-Bandwidth digital Content Protection (HDCP) conectado a la salida de vídeo. Se devuelve la siguiente información:

-   Vector de selección de claves HDCP (KSV) del dispositivo.
-   Si el dispositivo es un repetidor HDCP.



| Requisito | Value |
|--------------|---------------------------------------------------------------------------------------------------------|
| GUID de solicitud | OPM \_ GET \_ CONNECTED \_ HDCP \_ DEVICE \_ INFORMATION                                                          |
| Datos de entrada   | None                                                                                                    |
| Devolver datos  | Estructura [**OPM \_ CONNECTED \_ HDCP DEVICE \_ \_ INFORMATION**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information) |



 

## <a name="remarks"></a>Observaciones

Esta consulta solo se puede usar con el *modo de emulación copp*. Si la [**interfaz IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) usa la semántica del Administrador de protección de salida (OPM), no se admite esta solicitud de estado.

KSV es un identificador proporcionado al fabricante del dispositivo y se usa en el proceso de autenticación y configuración de HDCP. En el modo de emulación copp, la aplicación usa KSV para determinar si se revoca el dispositivo HDCP. Si es así, la aplicación no debe reproducir contenido protegido. Además, la aplicación no debe reproducir contenido protegido si el dispositivo es un repetidor HDCP, ya que COPP no admite repetidores HDCP.

Esta consulta no es necesaria cuando se usa la semántica de OPM, porque OPM admite la revocación de dispositivos y los repetidores HDCP.

Esta consulta es equivalente a la consulta COPPQueryHDCPKeyData de DXVA que se usa en el Protocolo de protección de salida \_ certificado (COPP).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[Solicitudes de estado de OPM](opm-status-requests.md)
</dt> </dl>

 

 




