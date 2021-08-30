---
description: Consulta si un conector de interfaz de vídeo digital (DVI) admite DVI versión 1.1 o posterior.
ms.assetid: b6c450c0-e97f-472d-ae09-fa1e062aeb9e
title: OPM_GET_DVI_CHARACTERISTICS (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f507d9d9c1f1df0efe1b3c5b0696c178ed6fdfe5d285fde2eb5d1def62e8d007
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887435"
---
# <a name="opm_get_dvi_characteristics"></a>OPM \_ GET \_ DVI \_ CHARACTERISTICS

Consulta si un conector de interfaz de vídeo digital (DVI) admite DVI versión 1.1 o posterior.



| Requisito | Value |
|--------------|-----------------------------------------------------------------------------|
| GUID de solicitud | OPM \_ GET \_ DVI \_ CHARACTERISTICS                                              |
| Datos de entrada   | Ninguno                                                                        |
| Devolver datos  | Una [**estructura OPM \_ STANDARD \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Comentarios

Si esta consulta se realiza correctamente, el **miembro ulInformation** de la [**estructura OPM STANDARD \_ \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) contiene uno de los valores siguientes.



| Value                                     | Descripción               |
|-------------------------------------------|---------------------------|
| OPM \_ DVI \_ CHARACTERISTIC \_ 1 \_ 0            | DVI versión 1.0.          |
| CARACTERÍSTICA DE \_ OPM DVI \_ \_ 1 \_ 1 \_ O \_ SUPERIOR | DVI versión 1.1 o posterior. |



 

Esta consulta solo se admite cuando el tipo de conector físico es OPM \_ CONNECTOR \_ TYPE \_ DVI. Para obtener el tipo de conector, envíe la consulta [**OPM \_ GET CONNECTOR \_ \_ TYPE.**](opm-get-connector-type.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Solicitudes de estado de OPM](opm-status-requests.md)
</dt> </dl>

 

 




