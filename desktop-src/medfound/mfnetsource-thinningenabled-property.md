---
description: Especifica si la conmutación de secuencias está habilitada en el origen de red.
ms.assetid: 691a3549-eaf8-4e3d-ad0e-e5b013658f78
title: MFNETSOURCE_THINNINGENABLED propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cfe92e09e9f772d7506cf944a8b2de793048d71e3ed8d893f534e919d4877ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940214"
---
# <a name="mfnetsource_thinningenabled-property"></a>MfNETSOURCE \_ PERSONALIZACIÓNENABLED, propiedad

Especifica si la conmutación de secuencias está habilitada en el origen de red. La conmutación de secuencias permite al servidor multimedia cambiar secuencias en un archivo de velocidad de bits múltiple (MBR), en función del ancho de banda disponible.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

Booleano (**LONG**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Comentarios

La constante **MFNETSOURCE \_ CTRLNNINGENABLED** define el GUID de esta clave de propiedad. El identificador de propiedad (PID) es cero.

Las aplicaciones pueden usar esta propiedad para configurar el origen de red. Para establecer la propiedad , pase un **puntero IPropertyStore** al solucionador de origen. Para obtener más información, vea [Configuring a Media Source](configuring-a-media-source.md).

El valor predeterminado de esta propiedad es **TRUE.**

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

 

 




