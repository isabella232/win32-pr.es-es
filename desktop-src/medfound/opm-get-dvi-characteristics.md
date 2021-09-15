---
description: Consulta si un conector de interfaz de vídeo digital (DVI) admite DVI versión 1.1 o posterior.
ms.assetid: b6c450c0-e97f-472d-ae09-fa1e062aeb9e
title: OPM_GET_DVI_CHARACTERISTICS (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a6f996b0397db509a45af6e243359c581df333
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574833"
---
# <a name="opm_get_dvi_characteristics"></a>CARACTERÍSTICAS DE OPM \_ GET \_ \_ DVI

Consulta si un conector de interfaz de vídeo digital (DVI) admite DVI versión 1.1 o posterior.



| Requisito | Value |
|--------------|-----------------------------------------------------------------------------|
| GUID de solicitud | CARACTERÍSTICAS DE OPM \_ GET \_ \_ DVI                                              |
| Datos de entrada   | None                                                                        |
| Devolver datos  | Una [**estructura OPM \_ STANDARD \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Observaciones

Si esta consulta se realiza correctamente, el **miembro ulInformation** de la estructura [**OPM \_ STANDARD \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) contiene uno de los valores siguientes.



| Value                                     | Descripción               |
|-------------------------------------------|---------------------------|
| OPM \_ DVI \_ CHARACTERISTIC \_ 1 \_ 0            | DVI versión 1.0.          |
| CARACTERÍSTICA \_ DE OPM DVI \_ \_ 1 \_ 1 \_ O \_ SUPERIOR | DVI versión 1.1 o posterior. |



 

Esta consulta solo se admite cuando el tipo de conector físico es OPM \_ CONNECTOR \_ TYPE \_ DVI. Para obtener el tipo de conector, envíe la consulta [**OPM \_ GET CONNECTOR \_ \_ TYPE.**](opm-get-connector-type.md)

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

 

 




