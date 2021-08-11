---
description: Especifica si el protocolo de multidifusión de difusión de secuencias multimedia (MSB) está habilitado en el origen de red.
ms.assetid: a46e3b4c-60be-4470-b9dc-041902c2563c
title: MFNETSOURCE_ENABLE_MSB propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1054b4a94bf966457ddeccc606fbd2fd2c8a1d5b3978b830b5e3c48f0f93b5ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243822"
---
# <a name="mfnetsource_enable_msb-property"></a>MFNETSOURCE \_ ENABLE \_ MSB, propiedad

Especifica si el protocolo de multidifusión de difusión de secuencias multimedia (MSB) está habilitado en el origen de red.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**LONG**

VT \_ I4

**lVal**



## <a name="remarks"></a>Comentarios

La constante **MFNETSOURCE \_ ENABLE \_ MSB** define el GUID de esta clave de propiedad. El identificador de propiedad (PID) es cero.

Las aplicaciones pueden usar esta propiedad para configurar el origen de red. Para establecer la propiedad , pase un **puntero IPropertyStore** al solucionador de origen. Para obtener más información, vea [Configuring a Media Source](configuring-a-media-source.md).

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
</dt> <dt>

[Protocolos admitidos](supported-protocols.md)
</dt> </dl>

 

 




