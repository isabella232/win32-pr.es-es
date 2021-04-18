---
description: El intervalo de puertos UDP válidos que puede usar el origen de red para recibir contenido de streaming.
ms.assetid: 97fe2d11-70f7-4baa-b49f-513d90146591
title: Propiedad MFNETSOURCE_UDP_PORT_RANGE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04db8c450bd20adc8c03ec3b964b543f1500aa51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715302"
---
# <a name="mfnetsource_udp_port_range-property"></a>\_Propiedad de \_ intervalo de puertos UDP de MFNETSOURCE \_

El intervalo de puertos UDP válidos que puede usar el origen de red para recibir contenido de streaming. El valor de esta propiedad es una cadena con el formato " *m*–*n* ", donde *m* y *n* son números de puerto.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

Cadena de caracteres anchos (**WCHAR** \* )

VT \_ LPWStr

**pwszVal**



## <a name="remarks"></a>Observaciones

El **intervalo de \_ \_ puertos UDP \_ constante MFNETSOURCE** define el GUID de esta clave de propiedad. El identificador de propiedad (PID) es cero.

Las aplicaciones pueden utilizar esta propiedad para configurar el origen de red. Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen. Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).

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

[Funciones de red en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




