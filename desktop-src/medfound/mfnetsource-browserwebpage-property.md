---
description: El valor del &\# 0034; CS (referer) &\# 0034; campo que utiliza el origen de red para el registro.
ms.assetid: 328544b3-0d5f-4d1a-9ad1-ac38402d5898
title: Propiedad MFNETSOURCE_BROWSERWEBPAGE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5e8222761299cad229b692ef400f69d0968ebd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001354"
---
# <a name="mfnetsource_browserwebpage-property"></a>\_Propiedad BROWSERWEBPAGE de MFNETSOURCE

El valor del campo "CS (referer)" que usa el origen de red para el registro. Las aplicaciones pueden establecer esta propiedad en la dirección URL de la página web en la que se incrustó la aplicación.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

Cadena de caracteres anchos (**WCHAR** \* )

VT \_ LPWStr

**pwszVal**



## <a name="remarks"></a>Observaciones

La constante **MFNETSOURCE \_ BROWSERWEBPAGE** define el GUID para esta clave de propiedad. El identificador de propiedad (PID) es cero.

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
</dt> </dl>

 

 




