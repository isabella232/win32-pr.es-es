---
description: Establece el nivel de protección de HDCP para la reproducción de DVD, siguiendo las reglas del Sistema de codificación de contenido de DVD (CSS).
ms.assetid: 8d9ecb9b-8528-4b23-ab2f-234ba2cb7ed0
title: OPM_SET_PROTECTION_LEVEL_ACCORDING_TO_CSS_DVD (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971d288367bdc5c59e11bdfd5b86fb233755c95e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574820"
---
# <a name="opm_set_protection_level_according_to_css_dvd"></a>OPM \_ ESTABLECE EL NIVEL DE PROTECCIÓN SEGÚN EL DVD DE \_ \_ \_ \_ \_ \_ CSS

Establece el nivel de protección de HDCP para la reproducción de DVD, siguiendo las reglas del Sistema de codificación de contenido de DVD (CSS).



| Requisito | Value |
|--------------|-----------------------------------------------------------------------------------------------------|
| GUID de comando | OPM \_ ESTABLECE EL NIVEL DE PROTECCIÓN SEGÚN EL DVD DE \_ \_ \_ \_ \_ \_ CSS                                                |
| Datos de entrada   | Estructura [**OPM \_ SET PROTECTION LEVEL \_ \_ \_ PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) |



 

## <a name="remarks"></a>Observaciones

Este comando se usa para establecer High-Bandwidth Digital Content Protection (HDCP) al reproducir DVD estándar. A diferencia [**del comando OPM \_ SET PROTECTION \_ \_ LEVEL,**](opm-set-protection-level.md) si HDCP no se puede establecer por algún motivo, este comando no detiene la reproducción. (Las reglas CSS de DVD contienen una disposición de "mejor esfuerzo" para los reproductores). De lo contrario, este comando es idéntico al **comando OPM \_ SET PROTECTION \_ \_ LEVEL.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[Comandos de OPM](opm-commands.md)
</dt> </dl>

 

 




