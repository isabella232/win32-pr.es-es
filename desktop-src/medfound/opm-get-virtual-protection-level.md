---
description: Devuelve el nivel de protección virtual para un mecanismo de protección especificado.
ms.assetid: 635d54de-2735-4390-8bac-ba63b9503909
title: OPM_GET_VIRTUAL_PROTECTION_LEVEL (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09fb4130b4ad700de2328114dbf900ff7d122045b277c8a5ae812332c730a5d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972924"
---
# <a name="opm_get_virtual_protection_level"></a>OPM \_ GET \_ VIRTUAL \_ PROTECTION \_ LEVEL

Devuelve el nivel de protección virtual para un mecanismo de protección especificado.

El *nivel* de protección virtual es el nivel solicitado por la aplicación durante la sesión actual de Output Protection Manager (OPM). El controlador podría aplicar un nivel superior, debido a eventos fuera de esta sesión de OPM. Para buscar el nivel de protección real que está en vigor, envíe la consulta [**OPM \_ GET ACTUAL \_ PROTECTION \_ \_ LEVEL.**](opm-get-actual-protection-level.md)



| Requisito | Value |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de solicitud | OPM \_ GET \_ VIRTUAL \_ PROTECTION \_ LEVEL                                                                                                                                          |
| Datos de entrada   | Mecanismo de protección que se consulta, especificado como un entero de 32 bits. El valor se interpreta como un miembro de las marcas de tipo de [**protección de OPM**](opm-protection-type-flags.md). |
| Devolver datos  | Una [**estructura OPM \_ STANDARD \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)                                                                                                   |



 

## <a name="remarks"></a>Comentarios

El nivel de protección se devuelve en el **miembro ulInformation** de la [**estructura OPM STANDARD \_ \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) El significado de este valor depende del mecanismo de protección que se consulta. Para cada mecanismo de protección, el valor **de ulInformation** es una marca de una enumeración diferente, como se muestra en la tabla siguiente.



| Mecanismo de protección | Enumeración                                                       |
|----------------------|-------------------------------------------------------------------|
| ACP                  | [**NIVEL DE PROTECCIÓN DE OPM \_ ACP \_ \_**](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| CGMS-A               | [**Marcas de protección de CGMS-A**](cgms-a-protection-flags.md)        |
| DPCP                 | [**NIVEL DE PROTECCIÓN \_ DE DPCP \_ DE OPM \_**](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| Hdcp                 | [**NIVEL DE PROTECCIÓN \_ DE HDCP \_ DE OPM \_**](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

Esta consulta es equivalente a la consulta COPPQueryLocalProtectionLevel de DXVA que se usa en el Protocolo de protección de salida \_ certificado (COPP).

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

 

 




