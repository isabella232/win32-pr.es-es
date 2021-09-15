---
description: Establece la configuración de secuencia para el origen de medios WTV.
ms.assetid: 2181723A-C6E8-42BD-979C-5C26FE3986C4
title: MFPKEY_SBESourceMode propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b82835a4cfc363e3ae2d054cce68f95c655447dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468620"
---
# <a name="mfpkey_sbesourcemode-property"></a>Propiedad \_ SBESourceMode de MFPKEY

Establece la configuración de secuencia para el origen de medios WTV.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**INT**

VT \_ INT

**intVal**



## <a name="remarks"></a>Observaciones

Use esta propiedad para configurar el origen multimedia de WTV. Para establecer la propiedad , pase un [**puntero IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) al solucionador de origen. Para obtener más información, vea [Configuring a Media Source](configuring-a-media-source.md).

El origen multimedia de WTV lee Windows recorded TV Show (.wtv y .ms-drv).

Esta propiedad debe tener uno de los siguientes valores.

-   1: Asigne las secuencias de audio disponibles a una única salida, en función del sistema local. Este modo es adecuado para la reproducción. (Valor predeterminado).
-   2. Se seleccionan todas las secuencias de audio y las secuencias posteriores (como los títulos y los flujos de datos). Este modo es adecuado para volver a experienciar o transcodificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
