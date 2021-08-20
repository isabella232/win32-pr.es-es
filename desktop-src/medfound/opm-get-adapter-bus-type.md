---
description: Devuelve el tipo de bus de E/S usado por la salida de vídeo.
ms.assetid: 1aff4c81-ffa0-4116-b7ea-60b1b83042df
title: OPM_GET_ADAPTER_BUS_TYPE (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78ce91a3f889775aa28f70640b850ab1790d55b33edb62a6cd11899436111dd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117871794"
---
# <a name="opm_get_adapter_bus_type"></a>OPM \_ GET \_ ADAPTER \_ BUS \_ TYPE

Devuelve el tipo de bus de E/S usado por la salida de vídeo.



| Requisito | Valor |
|--------------|-----------------------------------------------------------------------------|
| GUID de solicitud | OPM \_ GET \_ ADAPTER \_ BUS \_ TYPE                                                |
| Datos de entrada   | Ninguno                                                                        |
| Devolver datos  | Una [**estructura OPM \_ STANDARD \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Comentarios

El tipo de bus se devuelve en el **miembro ulInformation** de la [**estructura OPM STANDARD \_ \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) El valor es un OR bit a bit **de** marcas [**de tipo de bus OPM**](opm-bus-type-flags.md).

Esta consulta es equivalente a la consulta DXVA COPPQueryBusData que se usa en el Protocolo de protección de salida \_ certificado (COPP).

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

 

 




