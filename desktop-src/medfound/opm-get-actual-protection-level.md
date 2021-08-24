---
description: Devuelve el nivel de protección global para un mecanismo de protección especificado.
ms.assetid: 3dd4f6f0-2305-4470-bbd4-7737fa2d8eae
title: OPM_GET_ACTUAL_PROTECTION_LEVEL (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ed5d895c037fedfa97bbafab8331d685af9a7f1ce81489b8d600bd903aa2a17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101924"
---
# <a name="opm_get_actual_protection_level"></a>OPM \_ GET REAL PROTECTION \_ \_ \_ LEVEL

Devuelve el nivel de protección global para un mecanismo de protección especificado.



| Requisito | Valor |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de solicitud | OPM \_ GET REAL PROTECTION \_ \_ \_ LEVEL                                                                                                                                       |
| Datos de entrada   | Mecanismo de protección que se consulta, especificado como un entero de 32 bits. El valor se interpreta como un miembro de las marcas de tipo de protección [de OPM](opm-protection-type-flags.md). |
| Devolver datos  | Una [**estructura OPM \_ STANDARD \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)                                                                                               |



 

## <a name="remarks"></a>Comentarios

El nivel de protección global es el nivel de protección que se está aplicando actualmente en el conector, independientemente de cómo se indicó al controlador de gráficos que aplicara la protección. Por ejemplo, una aplicación puede establecer el nivel de protección ACP llamando a la **función ChangeDisplaySettingsEx.** En ese caso, el nivel de protección global reflejaría esta configuración, aunque no se solicitó a través de Output Protection Manager (OPM).

El nivel de protección se devuelve en el **miembro ulInformation** de la [**estructura OPM STANDARD \_ \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) El significado de este valor depende del mecanismo de protección que se consulta. Para cada mecanismo de protección, el valor **de ulInformation** es una marca de una enumeración diferente, como se muestra en la tabla siguiente.



| Mecanismo de protección | Enumeración                                                       |
|----------------------|-------------------------------------------------------------------|
| ACP                  | [**NIVEL DE PROTECCIÓN \_ DE OPM ACP \_ \_**](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| CGMS-A               | [Marcas de protección CGMS-A](cgms-a-protection-flags.md)            |
| DPCP                 | [**NIVEL DE PROTECCIÓN \_ DE DPCP \_ de OPM \_**](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| Hdcp                 | [**NIVEL DE PROTECCIÓN \_ DE HDCP \_ DE OPM \_**](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

Esta consulta es equivalente a la consulta COPPQueryGlobalProtectionLevel de DXVA que se usa en el Protocolo de protección de salida \_ certificado (COPP).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Solicitudes de estado de OPM](opm-status-requests.md)
</dt> </dl>

 

 




