---
description: Devuelve el tipo de conector físico de la salida de vídeo.
ms.assetid: c5862758-0125-4dbe-af72-5ed4a85bd702
title: OPM_GET_CONNECTOR_TYPE (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a95ca88b079aa93b4c2665fe7aa954eb58cfc1a9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574837"
---
# <a name="opm_get_connector_type"></a>OPM \_ GET \_ CONNECTOR \_ TYPE

Devuelve el tipo de conector físico de la salida de vídeo.



| Requisito | Value |
|--------------|-----------------------------------------------------------------------------|
| GUID de solicitud | OPM \_ GET \_ CONNECTOR \_ TYPE                                                   |
| Datos de entrada   | None                                                                        |
| Devolver datos  | Una [**estructura OPM \_ STANDARD \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Observaciones

El tipo de conector se devuelve en el **miembro ulInformation** de la [**estructura OPM STANDARD \_ \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) El valor de **ulInformation** es igual a uno de los tipos de conector enumerados en [**OPM Connector Type Flags**](opm-connector-type-flags.md).

En el modo de emulación copp, el tipo de conector se puede combinar con la marca **OPM \_ COPP \_ COMPATIBLE CONNECTOR \_ TYPE \_ \_ INTERNAL.** Use and bit a bit **para** extraer el tipo de conector:

`ulInformation & ~OPM_COPP_COMPATIBLE_CONNECTOR_TYPE_INTERNAL`

Las aplicaciones deben omitir la marca **\_ OPM COPP \_ COMPATIBLE CONNECTOR TYPE \_ \_ \_ INTERNAL.** Para obtener más información, vea la sección Comentarios de las marcas de tipo de conector [**de OPM**](opm-connector-type-flags.md).

Esta consulta es equivalente a la consulta COPPQueryConnectorType de DXVA que se usa en el Protocolo de protección de salida \_ certificado (COPP).

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

[**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Solicitudes de estado de OPM](opm-status-requests.md)
</dt> </dl>

 

 




