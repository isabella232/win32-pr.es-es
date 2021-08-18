---
description: Establece la configuración del flujo para el origen de medios WTV.
ms.assetid: 2181723A-C6E8-42BD-979C-5C26FE3986C4
title: MFPKEY_SBESourceMode propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c6b4fc0b248000f0540fd47fd7bbf8bba907994d1351144521bf162d330340
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973374"
---
# <a name="mfpkey_sbesourcemode-property"></a>Propiedad SBESourceMode de MFPKEY \_

Establece la configuración del flujo para el origen de medios WTV.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**INT**

VT \_ INT

**intVal**



## <a name="remarks"></a>Comentarios

Use esta propiedad para configurar el origen de medios WTV. Para establecer la propiedad , pase un [**puntero IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) al solucionador de origen. Para obtener más información, vea [Configuring a Media Source](configuring-a-media-source.md).

El origen multimedia WTV lee Windows recorded TV Show (.wtv y .ms-drv).

Esta propiedad debe tener uno de los siguientes valores.

-   1: Asigne las secuencias de audio disponibles a una única salida, según la configuración local del sistema. Este modo es adecuado para la reproducción. (Valor predeterminado).
-   2. Se seleccionan todas las secuencias de audio y subproyecciones (por ejemplo, secuencias de subtítulos y de datos). Este modo es adecuado para la reuxing o transcodificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
