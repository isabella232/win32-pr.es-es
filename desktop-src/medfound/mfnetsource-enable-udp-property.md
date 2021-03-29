---
description: Especifica si el transporte del Protocolo de datagramas de usuario (UDP) está habilitado en el origen de red.
ms.assetid: d46a59e6-8abc-484b-aecc-edf57ffff512
title: Propiedad MFNETSOURCE_ENABLE_UDP (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d326cbd375a7d7e22ea2afc121dd4af9086e60c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001260"
---
# <a name="mfnetsource_enable_udp-property"></a>MFNETSOURCE \_ habilitar \_ propiedad de UDP

Especifica si el transporte del Protocolo de datagramas de usuario (UDP) está habilitado en el origen de red.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

Booleano (**Long**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Observaciones

La constante **MFNETSOURCE \_ enable \_ UDP** define el GUID para esta clave de propiedad. El identificador de propiedad (PID) es cero.

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
</dt> <dt>

[Protocolos admitidos](supported-protocols.md)
</dt> </dl>

 

 




