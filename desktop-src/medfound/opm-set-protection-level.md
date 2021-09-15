---
description: Establece el nivel de protección para un mecanismo de protección de salida.
ms.assetid: f4e63bf5-0749-4054-9f86-7fd88f2881ad
title: OPM_SET_PROTECTION_LEVEL (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17a80fb674c9347dafc3bcf1a62dc4bc909f0471
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574817"
---
# <a name="opm_set_protection_level"></a>OPM \_ SET \_ PROTECTION \_ LEVEL

Establece el nivel de protección para un mecanismo de protección de salida.



| Requisito | Value |
|--------------|-----------------------------------------------------------------------------------------------------|
| GUID de comando | OPM \_ SET \_ PROTECTION \_ LEVEL                                                                         |
| Datos de entrada   | Estructura [**OPM \_ SET PROTECTION LEVEL \_ \_ \_ PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) |



 

## <a name="remarks"></a>Observaciones

Algunos conectores pueden admitir varios mecanismos de protección. Con ese tipo de conector, puede aplicar varios mecanismos de protección al mismo conector, con diferentes configuraciones para cada uno.

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

 

 




