---
description: Almacena la cadena enviada en el Accept-Language encabezado.
ms.assetid: b6ac613c-099b-4415-84ad-c0f8ad5f667b
title: MFNETSOURCE_STREAM_LANGUAGE propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c44b6f55fd2f5652a41d9aa5eed76e60e73152343d2baf6c577be56bc462c94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119344545"
---
# <a name="mfnetsource_stream_language-property"></a>Propiedad MFNETSOURCE \_ STREAM \_ LANGUAGE

Almacena la cadena enviada en el Accept-Language encabezado.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**Wchar\***

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>Comentarios

La constante MFNETSOURCE \_ STREAM LANGUAGE define el GUID de la clave de \_ propiedad. El identificador de propiedad (PID) es cero. Para establecer esta propiedad en el origen de red, pase un **puntero IPropertyStore** al solucionador de origen. Para obtener más información, vea [Configuring a Media Source](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[Redes en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




