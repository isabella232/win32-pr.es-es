---
description: Devuelve el nivel de protección virtual para un mecanismo de protección especificado.
ms.assetid: 635d54de-2735-4390-8bac-ba63b9503909
title: OPM_GET_VIRTUAL_PROTECTION_LEVEL (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7ac36abd0a043a74a18401205bbb5e661ac17d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696682"
---
# <a name="opm_get_virtual_protection_level"></a>\_nivel de \_ \_ protección virtual \_ de OPM

Devuelve el nivel de protección virtual para un mecanismo de protección especificado.

El nivel de protección *virtual* es el nivel solicitado por la aplicación durante la sesión actual de Output Protection Manager (OPM). El controlador puede aplicar un nivel superior, debido a eventos fuera de esta sesión OPM. Para buscar el nivel de protección real que está en vigor, envíe la consulta de [**\_ nivel de \_ \_ protección \_ OPM real**](opm-get-actual-protection-level.md) .



| Requisito | Value |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de solicitud | \_nivel de \_ \_ protección virtual \_ de OPM                                                                                                                                          |
| Datos de entrada   | Mecanismo de protección que se va a consultar, especificado como un entero de 32 bits. El valor se interpreta como un miembro de las [**marcas de tipo de protección OPM**](opm-protection-type-flags.md). |
| Devolver datos  | Una estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)                                                                                                   |



 

## <a name="remarks"></a>Observaciones

El nivel de protección se devuelve en el miembro **ulInformation** de la estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . El significado de este valor depende del mecanismo de protección que se consulta. Para cada mecanismo de protección, el valor de **ulInformation** es una marca de una enumeración diferente, como se muestra en la tabla siguiente.



| Mecanismo de protección | Enumeración                                                       |
|----------------------|-------------------------------------------------------------------|
| ACP                  | [**nivel de protección de OPM \_ ACP \_ \_**](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| CGMS-A               | [**Marcas de protección de CGMS-A**](cgms-a-protection-flags.md)        |
| DPCP                 | [**\_nivel de \_ protección de DPCP de OPM \_**](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| HDCP                 | [**\_nivel de \_ protección de HDCP de OPM \_**](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

Esta consulta es equivalente a la \_ consulta COPPQueryLocalProtectionLevel de DXVA usada en el protocolo de protección de la salida certificada (COPP).

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

 

 




