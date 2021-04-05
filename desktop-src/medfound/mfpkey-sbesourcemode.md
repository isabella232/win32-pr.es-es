---
description: Establece la configuración de flujo para el origen de medios WTV.
ms.assetid: 2181723A-C6E8-42BD-979C-5C26FE3986C4
title: Propiedad MFPKEY_SBESourceMode (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b82835a4cfc363e3ae2d054cce68f95c655447dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001626"
---
# <a name="mfpkey_sbesourcemode-property"></a>\_Propiedad SBESourceMode de MFPKEY

Establece la configuración de flujo para el origen de medios WTV.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

**INT**

VT \_ int

**intVal**



## <a name="remarks"></a>Observaciones

Utilice esta propiedad para configurar el origen de medios WTV. Para establecer la propiedad, pase un puntero [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) a la resolución de origen. Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).

El origen de medios WTV lee archivos de programas de TV grabados de Windows (. WTV y. ms-drv).

Esta propiedad debe tener uno de los valores siguientes.

-   1: asigne secuencias de audio disponibles a una sola salida, según el sistema local. Este modo es adecuado para la reproducción. (Valor predeterminado).
-   2. Se seleccionan todas las secuencias de audio y subsecuencias (como el título y los flujos de datos). Este modo es adecuado para remuxing o la transcodificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
