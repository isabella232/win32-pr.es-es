---
description: 'Más información acerca de: OPM_GET_ACP_AND_CGMSA_SIGNALING'
ms.assetid: d477fe3e-4498-450b-93b7-ce74ae9ed005
title: OPM_GET_ACP_AND_CGMSA_SIGNALING (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bf6294c3f1d90ac8a2292c65b3c1b8558e69220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715531"
---
# <a name="opm_get_acp_and_cgmsa_signaling"></a>la \_ \_ \_ señalización de OPM y \_ CGMSA de \_ OPM

Devuelve la siguiente información sobre una salida de vídeo:

-   Una lista de los estándares de protección de televisión que admite el controlador.
-   Estándar que está activo actualmente.
-   La relación de aspecto actual u otros datos de señalización.



| Requisito | Value |
|--------------|-------------------------------------------------------------------------------------|
| GUID de solicitud | la \_ \_ \_ señalización de OPM y \_ CGMSA de \_ OPM                                                |
| Datos de entrada   | None                                                                                |
| Devolver datos  | Una [**estructura \_ \_ de \_ \_ señalización de CGMSA y ACP de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling) |



 

## <a name="remarks"></a>Observaciones

Esta consulta es equivalente a la \_ consulta COPPQuerySignaling de DXVA usada en el protocolo de protección de la salida certificada (COPP).

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

[**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Solicitudes de estado de OPM](opm-status-requests.md)
</dt> </dl>

 

 




