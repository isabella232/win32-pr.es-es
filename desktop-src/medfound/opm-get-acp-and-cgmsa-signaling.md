---
description: 'Más información sobre: OPM_GET_ACP_AND_CGMSA_SIGNALING'
ms.assetid: d477fe3e-4498-450b-93b7-ce74ae9ed005
title: OPM_GET_ACP_AND_CGMSA_SIGNALING (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6c06da78ea9ae1a4f0ea58f0fb8770dffadff6a34d577fd2328816ffc100e4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102069"
---
# <a name="opm_get_acp_and_cgmsa_signaling"></a>OPM \_ GET \_ ACP \_ AND \_ CGMSA \_ SIGNALING

Devuelve la siguiente información sobre una salida de vídeo:

-   Lista de estándares de protección de televisión admitidos por el controlador.
-   Estándar que está activo actualmente.
-   La relación de aspecto actual u otros datos de señalización.



| Requisito | Valor |
|--------------|-------------------------------------------------------------------------------------|
| GUID de solicitud | OPM \_ GET \_ ACP \_ AND \_ CGMSA \_ SIGNALING                                                |
| Datos de entrada   | Ninguno                                                                                |
| Devolver datos  | Una [**estructura OPM \_ ACP Y \_ \_ CGMSA \_ SIGNALING**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling) |



 

## <a name="remarks"></a>Comentarios

Esta consulta es equivalente a la consulta COPPQuerySignaling de DXVA que se usa en el Protocolo de protección de salida \_ certificado (COPP).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Solicitudes de estado de OPM](opm-status-requests.md)
</dt> </dl>

 

 




