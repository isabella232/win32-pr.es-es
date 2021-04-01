---
description: Devuelve el tipo de conector físico de la salida de vídeo.
ms.assetid: c5862758-0125-4dbe-af72-5ed4a85bd702
title: OPM_GET_CONNECTOR_TYPE (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a95ca88b079aa93b4c2665fe7aa954eb58cfc1a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275833"
---
# <a name="opm_get_connector_type"></a>\_tipo de \_ conector de obtención de OPM \_

Devuelve el tipo de conector físico de la salida de vídeo.



| Requisito | Value |
|--------------|-----------------------------------------------------------------------------|
| GUID de solicitud | \_tipo de \_ conector de obtención de OPM \_                                                   |
| Datos de entrada   | None                                                                        |
| Devolver datos  | Una estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Observaciones

El tipo de conector se devuelve en el miembro **ulInformation** de la estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . El valor de **ulInformation** es igual a uno de los tipos de conectores que aparecen en las [**marcas de tipo de conector de OPM**](opm-connector-type-flags.md).

En el modo de emulación de COPP, el tipo de conector podría combinarse con la marca **\_ interna del \_ \_ \_ tipo \_ de conector compatible de COPP de OPM** . Use una operación and bit a bit para extraer el **tipo de conector** :

`ulInformation & ~OPM_COPP_COMPATIBLE_CONNECTOR_TYPE_INTERNAL`

Las aplicaciones deben omitir la marca **\_ interna del \_ \_ \_ tipo \_ de conector compatible de COPP de OPM** . Para obtener más información, consulte la sección Comentarios de las [**marcas de tipo de conector de OPM**](opm-connector-type-flags.md).

Esta consulta es equivalente a la \_ consulta COPPQueryConnectorType de DXVA usada en el protocolo de protección de la salida certificada (COPP).

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

 

 




