---
description: Especifica qué secuencias se conectaron correctamente a un receptor multimedia.
ms.assetid: b5e45bfc-d91d-41b8-aaa4-72b3a23d869e
title: MFP_PKEY_StreamRenderingResults propiedad (Mfplay.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d63272662d71e261374f51c0463c0bbbb6d515dfeea8dd1ec5ab424609c386d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954715"
---
# <a name="mfp_pkey_streamrenderingresults-property"></a>Propiedad \_ StreamRenderingResults de PKEY de MFP \_

> [!IMPORTANT]
> En desuso. Esta API puede quitarse de futuras versiones de Windows. Las aplicaciones deben usar la [sesión multimedia para](media-session.md) la reproducción.

 

Especifica qué secuencias se conectaron correctamente a un receptor multimedia.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

Matriz de **valores DWORD** (**CAUL**)

VT \_ VECTOR \| VT \_ UI4

**Caul**



## <a name="remarks"></a>Comentarios

Esta propiedad se puede enviar con el evento **\_ MFP EVENT \_ TYPE \_ MEDIAITEM \_ SET.**

El valor de la propiedad es una matriz **de HRESULT** s. Las entradas de la matriz corresponden a secuencias en el elemento multimedia actual. Cada entrada de la matriz indica si la secuencia correspondiente se conectó a un receptor de medios, como se indica a continuación:

-   Si la secuencia está conectada a un receptor multimedia, el valor es **S \_ OK**.
-   Si la secuencia no está seleccionada, el valor es **S \_ FALSE.**
-   Si se produjo un error al intentar conectar la secuencia, el valor es un código de error.

Si al menos una secuencia se conectó correctamente, es posible la reproducción. Por ejemplo, el usuario podría tener el códec necesario para reproducir la secuencia de audio, pero no para reproducir la secuencia de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                             |
| Header<br/>                   | <dl> <dt>Mfplay.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[**EVENTO MFP \_ MEDIAITEM \_ SET \_**](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_set_event)
</dt> </dl>

 

 




