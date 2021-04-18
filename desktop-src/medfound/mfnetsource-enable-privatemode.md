---
description: Habilita el modo de descarga privada en el origen de red.
ms.assetid: 679661A7-1D31-43F3-A64E-16ADCB5414B0
title: Propiedad MFNETSOURCE_ENABLE_PRIVATEMODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53aa0bde3bf76ded278e0e3ee37465adb717972a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715363"
---
# <a name="mfnetsource_enable_privatemode-property"></a>MFNETSOURCE \_ habilitar \_ propiedad PRIVATEMODE

Habilita el modo de descarga privada en el origen de red.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

**BOOLEANO**

VT \_ I4

**lVal**



## <a name="remarks"></a>Observaciones

Si esta propiedad es **true**, la memoria caché se borra cuando finaliza la sesión.

La constante **MFNETSOURCE \_ CLIENTGUID** define el GUID de la clave de propiedad. El identificador de propiedad (PID) es cero. Para establecer esta propiedad en el origen de red, pase un puntero **IPropertyStore** a la resolución de origen. Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Funciones de red en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




