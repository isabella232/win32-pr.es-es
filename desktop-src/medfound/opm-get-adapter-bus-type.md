---
description: Devuelve el tipo de bus de e/s utilizado por la salida del vídeo.
ms.assetid: 1aff4c81-ffa0-4116-b7ea-60b1b83042df
title: OPM_GET_ADAPTER_BUS_TYPE (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acde3611eb00977670c59c4326f793c1cb9037fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715528"
---
# <a name="opm_get_adapter_bus_type"></a>\_tipo de \_ bus de adaptador OPM Get \_ \_

Devuelve el tipo de bus de e/s utilizado por la salida del vídeo.



| Requisito | Value |
|--------------|-----------------------------------------------------------------------------|
| GUID de solicitud | \_tipo de \_ bus de adaptador OPM Get \_ \_                                                |
| Datos de entrada   | None                                                                        |
| Devolver datos  | Una estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Observaciones

El tipo de bus se devuelve en el miembro **ulInformation** de la estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . El valor es **una operación OR bit a bit** de marcas de tipo de [**bus OPM**](opm-bus-type-flags.md).

Esta consulta es equivalente a la \_ consulta COPPQueryBusData de DXVA usada en el protocolo de protección de la salida certificada (COPP).

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

 

 




