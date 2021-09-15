---
description: Especifica el ancho de banda del par de paquetes y el ancho de banda en tiempo de ejecución detectados por el origen de red.
ms.assetid: 430de7fc-fe62-4b89-b3fc-7cd956e40892
title: MFNETSOURCE_PPBANDWIDTH propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae0f23f289f68e46bba726a4391023ce9001e2ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579841"
---
# <a name="mfnetsource_ppbandwidth-property"></a>Propiedad MFNETSOURCE \_ PPBANDWIDTH

Especifica el ancho de banda del par de paquetes y el ancho de banda en tiempo de ejecución detectados por el origen de red. El valor de propiedad es una matriz de dos valores:

-   Ancho de banda de par de paquetes, en bits por segundo.
-   Ancho de banda en tiempo de ejecución, en bits por segundo.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

Matriz de **valores ULONG** (**CAUL**)

VT \_ VECTOR \| VT \_ UI4

**Caul**



## <a name="remarks"></a>Observaciones

La constante **MFNETSOURCE \_ PPBANDWIDTH** define el GUID de esta clave de propiedad. El identificador de propiedad (PID) es cero.

Esta propiedad es de solo lectura. Para recuperar esta propiedad, consulte el origen de red para la **interfaz IPropertyStore** y llame a **IPropertyStore::GetValue**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[Características de origen de red](network-source-features.md)
</dt> <dt>

[Redes en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




