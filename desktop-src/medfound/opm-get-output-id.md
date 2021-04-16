---
description: Devuelve el identificador único del monitor asociado a esta salida de vídeo.
ms.assetid: d34d68ff-c513-483e-8619-4a9baa2a40ba
title: OPM_GET_OUTPUT_ID (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6146c07be3467e513b33f636bde78e699f3e0d6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705893"
---
# <a name="opm_get_output_id"></a>\_obtener \_ \_ ID. de salida de OPM

Devuelve el identificador único del monitor asociado a esta salida de vídeo.



| Requisito | Value |
|--------------|------------------------------------------------------------------|
| GUID de solicitud | \_obtener \_ \_ ID. de salida de OPM                                             |
| Datos de entrada   | None                                                             |
| Devolver datos  | Una estructura de [**\_ \_ \_ datos de ID. de salida OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data) |



 

## <a name="remarks"></a>Observaciones

El controlador de vídeo asigna un identificador único a cada monitor. Esta consulta devuelve el identificador del monitor que está asociado con el puntero de [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) actual.

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

 

 




