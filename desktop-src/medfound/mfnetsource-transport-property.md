---
description: Especifica el protocolo de transporte utilizado por el origen de red.
ms.assetid: 7c8598ff-f408-42d0-9eee-3ef1e82f0466
title: MFNETSOURCE_TRANSPORT propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 933c4051cd3d008082c3b7811fcd88f8b118e51a9e864d947750813c11883b67
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663475"
---
# <a name="mfnetsource_transport-property"></a>Propiedad MFNETSOURCE \_ TRANSPORT

Especifica el protocolo de transporte utilizado por el origen de red. El valor de esta propiedad es un miembro de la [**enumeración MFNETSOURCE \_ TRANSPORT \_ TYPE.**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type)



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**LONG**

VT \_ I4

**lVal**



## <a name="remarks"></a>Comentarios

La constante **MFNETSOURCE \_ TRANSPORT** define el GUID de esta clave de propiedad. El identificador de propiedad (PID) es cero.

Esta propiedad es de solo lectura. Para recuperar esta propiedad, consulte el origen de red para la **interfaz IPropertyStore** y llame a **IPropertyStore::GetValue**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[Redes en Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Protocolos admitidos](supported-protocols.md)
</dt> </dl>

 

 




