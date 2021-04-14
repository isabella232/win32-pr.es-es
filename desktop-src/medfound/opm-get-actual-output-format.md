---
description: Devuelve una descripción de la señal de vídeo que se transmite a través del conector.
ms.assetid: 8464470f-49db-4559-80b2-02cfc473e30e
title: OPM_GET_ACTUAL_OUTPUT_FORMAT (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12eeca9bcf8fde670447afe4268a86ffa31b6a94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360483"
---
# <a name="opm_get_actual_output_format"></a>\_formato de \_ \_ salida real \_ de OPM

Devuelve una descripción de la señal de vídeo que se transmite a través del conector.



| Requisito | Value |
|--------------|------------------------------------------------------------------------------|
| GUID de solicitud | \_formato de \_ \_ salida real \_ de OPM                                             |
| Datos de entrada   | None                                                                         |
| Devolver datos  | Una estructura de [**\_ \_ \_ formato de salida real de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format) |



 

## <a name="remarks"></a>Observaciones

La señal de vídeo que se transmite a través del conector no tiene necesariamente el mismo formato que el modo de presentación del escritorio. Por ejemplo, el modo de presentación del escritorio podría ser de 1024 x 768 píxeles a 85 Hz, mientras que el conector podría ser un conector de S-vídeo que transmite una señal de vídeo a 720 x 480 píxeles, 60/1.01 Hz entrelazada. En ese caso, el controlador devolvería la resolución de la señal S-video, no la resolución del escritorio.

Esta consulta es equivalente a la \_ consulta COPPQueryDisplayData de DXVA usada en el protocolo de protección de la salida certificada (COPP).

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

 

 




