---
description: Especifica el &\# 0034; depósito de fugas&\# 0034; parámetros de una secuencia en un receptor de medios ASF.
ms.assetid: b01e59b6-0a7f-4125-867c-532385a27c15
title: Propiedad MFPKEY_ASFSTREAMSINK_CORRECTED_LEAKYBUCKET (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a4ebc2dc41a1f43906aff5d2fe8caea8d53057
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908143"
---
# <a name="mfpkey_asfstreamsink_corrected_leakybucket-property"></a>\_ \_ Propiedad LEAKYBUCKET corregida ASFSTREAMSINK MFPKEY \_

Especifica los parámetros de "depósito de fugas" (vea la sección comentarios) de una secuencia en un receptor de medios ASF.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

Matriz de valores **DWORD** (**caul**)

VT \_ Vector \| VT \_ UI4

**caul**



## <a name="remarks"></a>Observaciones

Una aplicación puede establecer esta propiedad en una secuencia del receptor de medios ASF una vez negociado el tipo de medio para la secuencia. Utilice esta propiedad para especificar la ventana de búfer real que utilizará el códec de Windows Media. Puede obtener esta información del códec mediante la interfaz **IWMCodecLeakyBucket** , que se documenta en el SDK de Windows Media Format.

El valor de esta propiedad es una matriz de tres valores **DWORD** en el orden siguiente:

-   Velocidad de bits, en bits por segundo.
-   Tamaño del búfer, en bytes.
-   Llenado inicial del búfer, en bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)
</dt> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




