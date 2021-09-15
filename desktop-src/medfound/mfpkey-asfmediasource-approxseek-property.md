---
description: Especifica si el origen de medios de ASF usa la búsqueda aproximada.
ms.assetid: 4877b67c-524c-4717-a90f-6de21918d3d8
title: MFPKEY_ASFMediaSource_ApproxSeek propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 253a18ebbdf78e3aa0ef0e79f41c4bf180a04b48
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474100"
---
# <a name="mfpkey_asfmediasource_approxseek-property"></a>Propiedad MFPKEY \_ ASFMediaSource \_ ApproxSeek

Especifica si el origen de medios de ASF usa la búsqueda aproximada.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**VARIANT \_ BOOL**

VT \_ BOOL

**boolVal**



## <a name="remarks"></a>Observaciones

Las aplicaciones pueden usar esta propiedad para configurar el origen multimedia de ASF. Para establecer la propiedad , pase un **puntero IPropertyStore** al solucionador de origen. Para obtener más información, vea [Configuring a Media Source](configuring-a-media-source.md).

El origen de medios de ASF controla las búsquedas de la manera siguiente:

-   Si el valor de esta propiedad es **VARIANT \_ TRUE,** el origen multimedia usa la búsqueda aproximada, que es menos precisa pero más rápida que la búsqueda exacta.
-   Si el valor es **VARIANT \_ FALSE y** el archivo ASF tiene un índice, el origen multimedia usa la búsqueda exacta.
-   Si el archivo ASF no contiene un índice, el origen multimedia usa la búsqueda de aproximación a menos que la propiedad [ \_ ASFMediaSource \_ IterativeSeekIfNoIndex de MFPKEY](mfpkey-asfmediasource-iterativeseekifnoindex.md) esté establecida en **VARIANT \_ TRUE.**
-   Si el archivo ASF no contiene un índice y la propiedad [ \_ \_ IterativeSeekIfNoIndex de ASFMediaSource de MFPKEY](mfpkey-asfmediasource-iterativeseekifnoindex.md) es **VARIANT \_ TRUE,** el origen del medio usa la búsqueda iterativa. La búsqueda iterativa es más precisa, pero más lenta que la búsqueda aproximada (pero generalmente menos precisa que la búsqueda exacta).
    > [!Note]  
    > Requiere Windows 7.

     

El valor predeterminado de esta propiedad es **VARIANT \_ FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




