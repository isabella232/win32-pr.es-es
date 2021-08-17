---
description: Especifica si el origen de medios de ASF usa búsquedas aproximadas.
ms.assetid: 4877b67c-524c-4717-a90f-6de21918d3d8
title: MFPKEY_ASFMediaSource_ApproxSeek propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f68dedbf2b008870021e620029a039c21465d4bb45a23428225d7c88fae6583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874339"
---
# <a name="mfpkey_asfmediasource_approxseek-property"></a>Propiedad MFPKEY \_ ASFMediaSource \_ ApproxSeek

Especifica si el origen de medios de ASF usa búsquedas aproximadas.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**VARIANT \_ BOOL**

VT \_ BOOL

**boolVal**



## <a name="remarks"></a>Comentarios

Las aplicaciones pueden usar esta propiedad para configurar el origen de medios de ASF. Para establecer la propiedad , pase un **puntero IPropertyStore** al solucionador de origen. Para obtener más información, vea [Configuring a Media Source](configuring-a-media-source.md).

El origen de medios de ASF controla las búsquedas de la manera siguiente:

-   Si el valor de esta propiedad es **VARIANT \_ TRUE,** el origen multimedia usa la búsqueda aproximada, que es menos precisa pero más rápida que la búsqueda exacta.
-   Si el valor es **VARIANT \_ FALSE y** el archivo ASF tiene un índice, el origen del medio usa búsquedas exactas.
-   Si el archivo ASF no contiene un índice, el origen multimedia usa la búsqueda de aproximación a menos que la propiedad [ \_ ASFMediaSource \_ IterativeSeekIfNoIndex de MFPKEY](mfpkey-asfmediasource-iterativeseekifnoindex.md) esté establecida en **VARIANT \_ TRUE.**
-   Si el archivo ASF no contiene un índice y la propiedad [ \_ ASFMediaSource \_ IterativeSeekIfNoIndex de MFPKEY](mfpkey-asfmediasource-iterativeseekifnoindex.md) es **VARIANT \_ TRUE,** el origen del medio usa la búsqueda iterativa. La búsqueda iterativa es más precisa, pero más lenta que la búsqueda aproximada (pero generalmente menos precisa que la búsqueda exacta).
    > [!Note]  
    > Requiere Windows 7.

     

El valor predeterminado de esta propiedad es **VARIANT \_ FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




