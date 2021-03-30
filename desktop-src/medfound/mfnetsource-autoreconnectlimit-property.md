---
description: El número de veces que el origen de red intenta volver a conectarse al servidor y reanudar el streaming si se pierde la conexión.
ms.assetid: 185e15c6-910b-4e27-9087-cfe30a174194
title: Propiedad MFNETSOURCE_AUTORECONNECTLIMIT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dac2a81cb4d47d8113059924877670458ac22ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811000"
---
# <a name="mfnetsource_autoreconnectlimit-property"></a>\_Propiedad AUTORECONNECTLIMIT de MFNETSOURCE

El número de veces que el origen de red intenta volver a conectarse al servidor y reanudar el streaming si se pierde la conexión.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

**DWORD** (almacenado como **Long**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Observaciones

La constante **MFNETSOURCE \_ AUTORECONNECTLIMIT** define el GUID para esta clave de propiedad. El identificador de propiedad (PID) es cero.

Las aplicaciones pueden utilizar esta propiedad para configurar el origen de red. Para establecer la propiedad, pase un objeto **IPropertyStore** a la resolución de origen. Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Características de origen de red](network-source-features.md)
</dt> <dt>

[Funciones de red en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




