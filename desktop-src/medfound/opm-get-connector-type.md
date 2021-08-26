---
description: Devuelve el tipo de conector físico de la salida de vídeo.
ms.assetid: c5862758-0125-4dbe-af72-5ed4a85bd702
title: OPM_GET_CONNECTOR_TYPE (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3099da66193048b52011e58eb5ce3f925d451fc1ad26b193f2955f6012f0e607
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887505"
---
# <a name="opm_get_connector_type"></a>OPM \_ GET \_ CONNECTOR \_ TYPE

Devuelve el tipo de conector físico de la salida de vídeo.



| Requisito | Value |
|--------------|-----------------------------------------------------------------------------|
| GUID de solicitud | OPM \_ GET \_ CONNECTOR \_ TYPE                                                   |
| Datos de entrada   | Ninguno                                                                        |
| Devolver datos  | Una [**estructura OPM \_ STANDARD \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Comentarios

El tipo de conector se devuelve en el **miembro ulInformation** de la [**estructura OPM STANDARD \_ \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) El valor de **ulInformation** es igual a uno de los tipos de conector enumerados en Marcas de tipo de conector [**de OPM.**](opm-connector-type-flags.md)

En el modo de emulación de COPP, el tipo de conector puede combinarse con la marca **OPM \_ COPP \_ COMPATIBLE CONNECTOR \_ TYPE \_ \_ INTERNAL.** Use and bit a **bit** para extraer el tipo de conector:

`ulInformation & ~OPM_COPP_COMPATIBLE_CONNECTOR_TYPE_INTERNAL`

Las aplicaciones deben omitir la marca **\_ OPM COPP \_ COMPATIBLE CONNECTOR TYPE \_ \_ \_ INTERNAL.** Para obtener más información, vea la sección Comentarios de las marcas [**de tipo de conector de OPM**](opm-connector-type-flags.md).

Esta consulta es equivalente a la consulta COPPQueryConnectorType de DXVA que se usa en el Protocolo de protección de salida \_ certificado (COPP).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Solicitudes de estado de OPM](opm-status-requests.md)
</dt> </dl>

 

 




