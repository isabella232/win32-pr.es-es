---
description: Número de veces que el origen de red ha intentado volver a conectarse a la red.
ms.assetid: e3410e68-6358-4f00-8039-833a4ccdf7fa
title: MFNETSOURCE_AUTORECONNECTPROGRESS propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cfbf0bac147b3608145d3ef38eb328a44de1c064899a5e7800acbadfadcf709
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243879"
---
# <a name="mfnetsource_autoreconnectprogress-property"></a>Propiedad MFNETSOURCE \_ AUTORECONNECTPROGRESS

Número de veces que el origen de red ha intentado volver a conectarse a la red.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**DWORD** (almacenado como **LONG)**

VT \_ I4

**lVal**



## <a name="remarks"></a>Comentarios

La constante **MFNETSOURCE \_ AUTORECONNECTPROGRESS** define el GUID de esta clave de propiedad. El identificador de propiedad (PID) es cero.

Esta propiedad es de solo lectura. Para recuperar esta propiedad, consulte el origen de red para la **interfaz IPropertyStore** y llame a **IPropertyStore::GetValue**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[Características de origen de red](network-source-features.md)
</dt> <dt>

[Redes en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




