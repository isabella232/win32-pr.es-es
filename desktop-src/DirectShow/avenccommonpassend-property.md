---
description: Detiene el paso de codificación actual o consulta si el paso de codificación actual es el último.
ms.assetid: 847f638f-9ab9-42ca-8e39-82c113cee92f
title: Propiedad AVEncCommonPassEnd (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02faeb9d78f10b962b7134fd316bda348b0f03e1a82ace210956c2243231df19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873375"
---
# <a name="avenccommonpassend-property"></a>Propiedad AVEncCommonPassEnd

Detiene el paso de codificación actual o consulta si el paso de codificación actual es el último.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncCommonPassEnd**

## <a name="remarks"></a>Comentarios

Si se establece esta propiedad **en VARIANT \_ TRUE,** se finaliza el paso de codificación actual. Si se establece esta propiedad **en VARIANT \_ FALSE,** se finaliza la codificación multipass.

Al leer esta propiedad se consulta si el paso de codificación actual es el último.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional \[ aplicaciones de escritorio para \| UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




