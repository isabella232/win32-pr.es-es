---
description: Especifica qué secuencias se conectaron correctamente a un receptor de medios.
ms.assetid: b5e45bfc-d91d-41b8-aaa4-72b3a23d869e
title: Propiedad MFP_PKEY_StreamRenderingResults (mfplay. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6acf04f751e8611f3add3a62fc7b4406d757999e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360384"
---
# <a name="mfp_pkey_streamrenderingresults-property"></a>MFP \_ PKEY \_ propiedad StreamRenderingResults

> [!IMPORTANT]
> En desuso. Esta API se puede quitar de las versiones futuras de Windows. Las aplicaciones deben usar la [sesión multimedia](media-session.md) para la reproducción.

 

Especifica qué secuencias se conectaron correctamente a un receptor de medios.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

Matriz de valores **DWORD** (**caul**)

VT \_ Vector \| VT \_ UI4

**caul**



## <a name="remarks"></a>Observaciones

Esta propiedad se puede enviar con el evento de **\_ tipo de evento MFP \_ \_ MEDIAITEM \_ set** .

El valor de la propiedad es una matriz de **HRESULT** s. Las entradas de la matriz corresponden a las secuencias del elemento multimedia actual. Cada entrada de la matriz indica si la secuencia correspondiente se conectó a un receptor de medios, como se indica a continuación:

-   Si la secuencia está conectada a un receptor de medios, el valor es **S \_ OK**.
-   Si la secuencia no está seleccionada, el valor es **S \_ false**.
-   Si se produjo un error al intentar conectar el flujo, el valor es un código de error.

Si al menos una secuencia se conectó correctamente, es posible la reproducción. Por ejemplo, el usuario podría tener el códec necesario para reproducir la secuencia de audio, pero no reproducir la secuencia de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Mfplay. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**\_MEDIAITEM el \_ \_ evento set de MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_set_event)
</dt> </dl>

 

 




