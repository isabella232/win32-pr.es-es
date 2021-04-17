---
description: Habilita o deshabilita el modo de vista previa, que permite que la aplicación sobrescriba la lógica de almacenamiento en búfer inicial.
ms.assetid: 8aa8c6ac-8746-4bf6-9f57-b1426495a275
title: Propiedad MFNETSOURCE_PREVIEWMODEENABLED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1170135b0feb90a79bf5e26d36a02e262fdc1977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652875"
---
# <a name="mfnetsource_previewmodeenabled-property"></a>\_Propiedad PREVIEWMODEENABLED de MFNETSOURCE

Habilita o deshabilita el modo de vista previa, que permite que la aplicación sobrescriba la lógica de almacenamiento en búfer inicial.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

**BOOLEANO**

VT \_ bool

**lVal**



## <a name="remarks"></a>Observaciones

La constante **MFNETSOURCE \_ PREVIEWMODEENABLED** define el GUID de la clave de propiedad. El identificador de propiedad (PID) es cero. Esta propiedad se establece en el origen de red pasando un puntero **IPropertyStore** a la resolución de origen. Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Funciones de red en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




