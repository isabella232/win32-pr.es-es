---
description: Devuelve el identificador único del monitor asociado a esta salida de vídeo.
ms.assetid: d34d68ff-c513-483e-8619-4a9baa2a40ba
title: OPM_GET_OUTPUT_ID (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6146c07be3467e513b33f636bde78e699f3e0d6d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361132"
---
# <a name="opm_get_output_id"></a>OPM \_ GET \_ OUTPUT \_ ID

Devuelve el identificador único del monitor asociado a esta salida de vídeo.



| Requisito | Value |
|--------------|------------------------------------------------------------------|
| GUID de solicitud | OPM \_ GET \_ OUTPUT \_ ID                                             |
| Datos de entrada   | None                                                             |
| Devolver datos  | Estructura [**de datos de un identificador de salida \_ \_ \_ de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data) |



 

## <a name="remarks"></a>Observaciones

El controlador de vídeo asigna un identificador único a cada monitor. Esta consulta devuelve el identificador del monitor asociado al puntero [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Solicitudes de estado de OPM](opm-status-requests.md)
</dt> </dl>

 

 




