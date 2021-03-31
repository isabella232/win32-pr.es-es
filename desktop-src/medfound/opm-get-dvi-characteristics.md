---
description: Consulta si un conector de la interfaz de vídeo digital (DVI) admite DVI versión 1,1 o posterior.
ms.assetid: b6c450c0-e97f-472d-ae09-fa1e062aeb9e
title: OPM_GET_DVI_CHARACTERISTICS (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a6f996b0397db509a45af6e243359c581df333
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082291"
---
# <a name="opm_get_dvi_characteristics"></a>características de la \_ obtención de \_ DVI de OPM \_

Consulta si un conector de la interfaz de vídeo digital (DVI) admite DVI versión 1,1 o posterior.



| Requisito | Value |
|--------------|-----------------------------------------------------------------------------|
| GUID de solicitud | características de la \_ obtención de \_ DVI de OPM \_                                              |
| Datos de entrada   | None                                                                        |
| Devolver datos  | Una estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Observaciones

Si esta consulta se realiza correctamente, el miembro **ulInformation** de la estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) contiene uno de los valores siguientes.



| Value                                     | Descripción               |
|-------------------------------------------|---------------------------|
| Característica de DVI de OPM \_ \_ \_ 1 \_ 0            | DVI versión 1,0.          |
| \_ \_ Característica de DVI \_ de la versión 1 \_ 1 \_ o \_ superior de OPM | DVI versión 1,1 o posterior. |



 

Esta consulta solo se admite cuando el tipo de conector físico es el tipo de conector de OPM \_ \_ \_ DVI. Para obtener el tipo de conector, envíe la consulta de [**\_ tipo de \_ conector \_ OPM Get**](opm-get-connector-type.md) .

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

 

 




