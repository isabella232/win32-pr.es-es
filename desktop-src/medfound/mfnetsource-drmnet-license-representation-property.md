---
description: Almacena una matriz de bytes que representa la licencia DRM asociada a la secuencia de bytes.
ms.assetid: 866a9706-0b0a-4675-af61-5f55a5a69014
title: MFNETSOURCE_DRMNET_LICENSE_REPRESENTATION propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2718ba8a13d8d0c00114449f1141be77db0d3f83930d3b3de2171719c3bdf2d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113555"
---
# <a name="mfnetsource_drmnet_license_representation-property"></a>Propiedad MFNETSOURCE \_ DRMNET \_ LICENSE \_ REPRESENTATION

Almacena una matriz de bytes que representa la licencia DRM asociada a la secuencia de bytes.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

Matriz de bytes (**BLOB**)

VT \_ BLOB

**blob**



## <a name="remarks"></a>Comentarios

La constante **MFNETSOURCE \_ DRMNET \_ LICENSE \_ REPRESENTATION** define el GUID de esta clave de propiedad. El identificador de propiedad (PID) es cero.

Esta propiedad es de solo lectura. Para obtener el valor de propiedad de la secuencia de bytes de red, llame a **IPropertyStore::GetValue** y pase la **estructura PROPERTYKEY** en el *parámetro key.* El **miembro fmtid** de **PROPERTYKEY** debe establecerse en el GUID de la propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[Redes en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




