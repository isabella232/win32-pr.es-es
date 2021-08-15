---
description: Especifica los parámetros \# &0034;leaky bucket&0034; para una secuencia en un receptor \# de medios de ASF.
ms.assetid: b01e59b6-0a7f-4125-867c-532385a27c15
title: MFPKEY_ASFSTREAMSINK_CORRECTED_LEAKYBUCKET propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bcb41de92f160e3d73c7d15721dae3015efc0ad1bc1a982d1a22c542d311b60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874097"
---
# <a name="mfpkey_asfstreamsink_corrected_leakybucket-property"></a>Propiedad DE MFPKEY \_ ASFSTREAMSINK \_ \_ CORREGIDA LEAKYBUCKET

Especifica los parámetros del "cubo de fugas" (consulte Comentarios) para una secuencia en un receptor de medios de ASF.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

Matriz de **valores DWORD** (**CAUL**)

VT \_ VECTOR \| VT \_ UI4

**Caul**



## <a name="remarks"></a>Comentarios

Una aplicación puede establecer esta propiedad en una secuencia del receptor de medios de ASF una vez negociado el tipo de medio para la secuencia. Use esta propiedad para especificar la ventana de búfer real que usará Windows códec Multimedia. Puede obtener esta información del códec mediante la interfaz **IWMCodecLeakyBucket,** que se documenta en el SDK Windows Media Format.

El valor de esta propiedad es una matriz de tres **valores DWORD** en el orden siguiente:

-   Velocidad de bits, en bits por segundo.
-   Tamaño del búfer, en bytes.
-   Integridad inicial del búfer, en bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)
</dt> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




