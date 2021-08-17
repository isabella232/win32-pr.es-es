---
description: Devuelve una descripción de la señal de vídeo que se transmite a través del conector.
ms.assetid: 8464470f-49db-4559-80b2-02cfc473e30e
title: OPM_GET_ACTUAL_OUTPUT_FORMAT (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a37f35e9f3d64bd1a72bb6800011978ea1cf2f4c60f523a344594f949beb4f81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102079"
---
# <a name="opm_get_actual_output_format"></a>OPM \_ GET REAL OUTPUT \_ \_ \_ FORMAT

Devuelve una descripción de la señal de vídeo que se transmite a través del conector.



| Requisito | Valor |
|--------------|------------------------------------------------------------------------------|
| GUID de solicitud | OPM \_ GET REAL OUTPUT \_ \_ \_ FORMAT                                             |
| Datos de entrada   | Ninguno                                                                         |
| Devolver datos  | Estructura [**OPM \_ REAL OUTPUT \_ \_ FORMAT**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format) |



 

## <a name="remarks"></a>Comentarios

La señal de vídeo que se transmite a través del conector no tiene necesariamente el mismo formato que el modo de presentación de escritorio. Por ejemplo, el modo de visualización de escritorio podría ser de 1024 x 768 píxeles a 85 Hz, mientras que el conector podría ser un conector S-Video que transmite una señal de vídeo a 720 x 480 píxeles, 60/1,01 Hz entrelazada. En ese caso, el controlador devolvería la resolución de la señal S-Video, no la resolución de escritorio.

Esta consulta es equivalente a la consulta DXVA COPPQueryDisplayData que se usa en el Protocolo de protección de salida \_ certificado (COPP).

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

 

 




