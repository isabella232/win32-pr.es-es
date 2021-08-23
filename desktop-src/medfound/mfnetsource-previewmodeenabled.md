---
description: Habilita o deshabilita el modo de vista previa, lo que permite a la aplicación sobrescribir la lógica de almacenamiento en búfer inicial.
ms.assetid: 8aa8c6ac-8746-4bf6-9f57-b1426495a275
title: MFNETSOURCE_PREVIEWMODEENABLED propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e03940828c6fa32b9e0367a03f960d4d64d88edf691100817ed31883013ce1b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663865"
---
# <a name="mfnetsource_previewmodeenabled-property"></a>Propiedad MFNETSOURCE \_ PREVIEWMODEENABLED

Habilita o deshabilita el modo de vista previa, lo que permite a la aplicación sobrescribir la lógica de almacenamiento en búfer inicial.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**Bool**

VT \_ BOOL

**lVal**



## <a name="remarks"></a>Comentarios

La constante **MFNETSOURCE \_ PREVIEWMODEENABLED** define el GUID de la clave de propiedad. El identificador de propiedad (PID) es cero. Esta propiedad se establece en el origen de red pasando un **puntero IPropertyStore** al solucionador de origen. Para obtener más información, vea [Configuring a Media Source](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[Redes en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




