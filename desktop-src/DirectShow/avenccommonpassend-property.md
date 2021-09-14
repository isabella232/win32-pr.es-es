---
description: Detiene el paso de codificación actual o consulta si el paso de codificación actual es el último.
ms.assetid: 847f638f-9ab9-42ca-8e39-82c113cee92f
title: Propiedad AVEncCommonPassEnd (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 026b20cf0c13536403e7ccf32b160e8c6fc08141
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162001"
---
# <a name="avenccommonpassend-property"></a>Propiedad AVEncCommonPassEnd

Detiene el paso de codificación actual o consulta si el paso de codificación actual es el último.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncCommonPassEnd**

## <a name="remarks"></a>Observaciones

Al establecer esta propiedad en **VARIANT \_ TRUE,** finaliza el paso de codificación actual. Si se establece esta propiedad **en VARIANT \_ FALSE,** se finaliza la codificación multipass.

Al leer esta propiedad se consulta si el paso de codificación actual es el último.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional \[ aplicaciones de escritorio aplicaciones para \| UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




