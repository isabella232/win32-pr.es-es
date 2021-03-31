---
description: Devuelve el nivel de protección global para un mecanismo de protección especificado.
ms.assetid: 3dd4f6f0-2305-4470-bbd4-7737fa2d8eae
title: OPM_GET_ACTUAL_PROTECTION_LEVEL (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 960d704fd44ca779f128795b26603698bb0ad622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082293"
---
# <a name="opm_get_actual_protection_level"></a>\_obtener \_ nivel de \_ protección \_ real de OPM

Devuelve el nivel de protección global para un mecanismo de protección especificado.



| Requisito | Value |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de solicitud | \_obtener \_ nivel de \_ protección \_ real de OPM                                                                                                                                       |
| Datos de entrada   | Mecanismo de protección que se va a consultar, especificado como un entero de 32 bits. El valor se interpreta como un miembro de las [marcas de tipo de protección OPM](opm-protection-type-flags.md). |
| Devolver datos  | Una estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)                                                                                               |



 

## <a name="remarks"></a>Observaciones

El nivel de protección global es el nivel de protección que se está aplicando actualmente en el conector, independientemente de cómo se haya indicado al controlador de gráficos que aplique la protección. Por ejemplo, una aplicación puede establecer el nivel de protección ACP llamando a la función **ChangeDisplaySettingsEx** . En ese caso, el nivel de protección global reflejaría esta configuración, aunque no se solicitó a través de Output Protection Manager (OPM).

El nivel de protección se devuelve en el miembro **ulInformation** de la estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . El significado de este valor depende del mecanismo de protección que se consulta. Para cada mecanismo de protección, el valor de **ulInformation** es una marca de una enumeración diferente, como se muestra en la tabla siguiente.



| Mecanismo de protección | Enumeración                                                       |
|----------------------|-------------------------------------------------------------------|
| ACP                  | [**nivel de protección de OPM \_ ACP \_ \_**](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| CGMS-A               | [Marcas de protección de CGMS-A](cgms-a-protection-flags.md)            |
| DPCP                 | [**\_nivel de \_ protección de DPCP de OPM \_**](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| HDCP                 | [**\_nivel de \_ protección de HDCP de OPM \_**](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

Esta consulta es equivalente a la \_ consulta COPPQueryGlobalProtectionLevel de DXVA usada en el protocolo de protección de la salida certificada (COPP).

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

 

 




