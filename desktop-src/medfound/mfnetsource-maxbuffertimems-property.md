---
description: Cantidad máxima de datos que los búferes de origen de red, en milisegundos.
ms.assetid: bd776dc2-341a-4d87-8a06-8063daf53ede
title: MFNETSOURCE_MAXBUFFERTIMEMS propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99d0bf07da8b931ee5487715a4b4430e5ed4384142fc69678a075275d9c7757b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243437"
---
# <a name="mfnetsource_maxbuffertimems-property"></a>Propiedad MFNETSOURCE \_ MAXBUFFERTIMEMS

Cantidad máxima de datos que los búferes de origen de red, en milisegundos.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**DWORD** (almacenado como **LONG)**

VT \_ I4

**lVal**



## <a name="remarks"></a>Comentarios

La constante **MFNETSOURCE \_ MAXBUFFERTIMEMS** define el GUID de esta clave de propiedad. El identificador de propiedad (PID) es cero.

Las aplicaciones pueden usar esta propiedad para configurar el origen de red. Para establecer la propiedad , pase un **puntero IPropertyStore** al solucionador de origen. Para obtener más información, vea [Configuring a Media Source](configuring-a-media-source.md).

El valor predeterminado de esta propiedad es 40 000 milisegundos.

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

 

 




