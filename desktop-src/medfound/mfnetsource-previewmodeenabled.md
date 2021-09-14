---
description: Habilita o deshabilita el modo de vista previa, lo que permite a la aplicación sobrescribir la lógica de almacenamiento en búfer inicial.
ms.assetid: 8aa8c6ac-8746-4bf6-9f57-b1426495a275
title: MFNETSOURCE_PREVIEWMODEENABLED propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1170135b0feb90a79bf5e26d36a02e262fdc1977
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127269036"
---
# <a name="mfnetsource_previewmodeenabled-property"></a>Propiedad MFNETSOURCE \_ PREVIEWMODEENABLED

Habilita o deshabilita el modo de vista previa, lo que permite a la aplicación sobrescribir la lógica de almacenamiento en búfer inicial.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**BOOL**

VT \_ BOOL

**lVal**



## <a name="remarks"></a>Observaciones

La constante **MFNETSOURCE \_ PREVIEWMODEENABLED** define el GUID de la clave de propiedad. El identificador de propiedad (PID) es cero. Esta propiedad se establece en el origen de red pasando un **puntero IPropertyStore** al solucionador de origen. Para obtener más información, vea [Configuring a Media Source](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 \[ aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[Redes en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




