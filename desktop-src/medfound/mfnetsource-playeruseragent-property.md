---
description: El valor de la segunda parte del campo &\# 0034; CS (User-Agent) &\# 0034; que usa el origen de red para el registro.
ms.assetid: c662a6d6-5e0b-4c28-841d-5774d4103d4b
title: Propiedad MFNETSOURCE_PLAYERUSERAGENT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f4d06eaea566e22e1239ed04594f2f592c7cd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720382"
---
# <a name="mfnetsource_playeruseragent-property"></a>\_Propiedad PLAYERUSERAGENT de MFNETSOURCE

El valor de la segunda parte del campo "CS (User-Agent)" que utiliza el origen de red para el registro. Las aplicaciones pueden establecer esta propiedad en cualquier valor de cadena.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

Cadena de caracteres anchos (**WCHAR** \* )

VT \_ LPWStr

**pwszVal**



## <a name="remarks"></a>Observaciones

La constante **MFNETSOURCE \_ PLAYERUSERAGENT** define el GUID para esta clave de propiedad. El identificador de propiedad (PID) es cero.

Las aplicaciones pueden utilizar esta propiedad para configurar el origen de red. Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen. Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Registro de cliente](client-logging.md)
</dt> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Funciones de red en Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[**MFNETSOURCE \_ BROWSERUSERAGENT**](mfnetsource-browseruseragent-property.md)
</dt> </dl>

 

 




