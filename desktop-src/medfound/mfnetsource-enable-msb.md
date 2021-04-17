---
description: Especifica si está habilitado el protocolo de multidifusión de difusión de transmisión multimedia (MSB) en el origen de red.
ms.assetid: a46e3b4c-60be-4470-b9dc-041902c2563c
title: Propiedad MFNETSOURCE_ENABLE_MSB (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e6b2a49876cf504bfc4e086ab1e064e6835283a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687054"
---
# <a name="mfnetsource_enable_msb-property"></a>MFNETSOURCE \_ Habilitar la \_ propiedad MSB

Especifica si está habilitado el protocolo de multidifusión de difusión de transmisión multimedia (MSB) en el origen de red.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

**LONG**

VT \_ I4

**lVal**



## <a name="remarks"></a>Observaciones

La constante **MFNETSOURCE \_ enable \_ MSB** define el GUID para esta clave de propiedad. El identificador de propiedad (PID) es cero.

Las aplicaciones pueden utilizar esta propiedad para configurar el origen de red. Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen. Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).

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
</dt> <dt>

[Protocolos admitidos](supported-protocols.md)
</dt> </dl>

 

 




