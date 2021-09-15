---
description: Especifica los parámetros &\# 0034;leaky bucket&0034; para una secuencia en un receptor \# de medios de ASF.
ms.assetid: b01e59b6-0a7f-4125-867c-532385a27c15
title: MFPKEY_ASFSTREAMSINK_CORRECTED_LEAKYBUCKET propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a4ebc2dc41a1f43906aff5d2fe8caea8d53057
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468653"
---
# <a name="mfpkey_asfstreamsink_corrected_leakybucket-property"></a>Propiedad \_ \_ LEAKYBUCKET CORREGIDA DE ASFSTREAMSINK \_ de MFPKEY

Especifica los parámetros de "cubo de pérdida" (consulte Comentarios) para una secuencia en un receptor de medios de ASF.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

Matriz de **valores DWORD** (**CAUL**)

VT \_ VECTOR \| VT \_ UI4

**Caul**



## <a name="remarks"></a>Observaciones

Una aplicación puede establecer esta propiedad en una secuencia del receptor de medios de ASF después de que se negocie el tipo de medio para la secuencia. Use esta propiedad para especificar la ventana de búfer real que usará Windows códec Multimedia. Puede obtener esta información del códec mediante la interfaz **IWMCodecLeakyBucket,** que se documenta en el SDK Windows Media Format.

El valor de esta propiedad es una matriz de tres **valores DWORD** en el orden siguiente:

-   Velocidad de bits, en bits por segundo.
-   Tamaño del búfer, en bytes.
-   Integridad inicial del búfer, en bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)
</dt> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




