---
description: Establece el nivel de protección de HDCP para la reproducción de DVD, siguiendo las reglas del sistema de cifrado de contenido (CSS) de DVD.
ms.assetid: 8d9ecb9b-8528-4b23-ab2f-234ba2cb7ed0
title: OPM_SET_PROTECTION_LEVEL_ACCORDING_TO_CSS_DVD (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971d288367bdc5c59e11bdfd5b86fb233755c95e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155340"
---
# <a name="opm_set_protection_level_according_to_css_dvd"></a>\_configuración \_ \_ \_ de nivel de protección de OPM según el \_ \_ DVD de CSS \_

Establece el nivel de protección de HDCP para la reproducción de DVD, siguiendo las reglas del sistema de cifrado de contenido (CSS) de DVD.



| Requisito | Value |
|--------------|-----------------------------------------------------------------------------------------------------|
| GUID de comando | \_configuración \_ \_ \_ de nivel de protección de OPM según el \_ \_ DVD de CSS \_                                                |
| Datos de entrada   | Una estructura de [**parámetros de nivel de protección de \_ configuración \_ \_ \_ de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) |



 

## <a name="remarks"></a>Observaciones

Este comando se usa para establecer High-Bandwidth Content Protection digital (HDCP) al reproducir DVDs estándar. A diferencia del [**comando \_ set \_ PROTECTION \_ LEVEL de OPM**](opm-set-protection-level.md) , si no se puede establecer HDCP por alguna razón, este comando no detiene la reproducción. (Las reglas de CSS de DVD contienen un aprovisionamiento de "mejor esfuerzo" para los reproductores). De lo contrario, este comando es idéntico al comando de **nivel de protección de set de OPM \_ \_ \_** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IOPMVideoOutput:: configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[Comandos OPM](opm-commands.md)
</dt> </dl>

 

 




