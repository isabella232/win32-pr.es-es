---
description: El número de veces que el origen de red ha intentado volver a conectarse a la red.
ms.assetid: e3410e68-6358-4f00-8039-833a4ccdf7fa
title: Propiedad MFNETSOURCE_AUTORECONNECTPROGRESS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05ade09bd425988cb0a64b258ff0887f8e79d4c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715367"
---
# <a name="mfnetsource_autoreconnectprogress-property"></a>\_Propiedad AUTORECONNECTPROGRESS de MFNETSOURCE

El número de veces que el origen de red ha intentado volver a conectarse a la red.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

**DWORD** (almacenado como **Long**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Observaciones

La constante **MFNETSOURCE \_ AUTORECONNECTPROGRESS** define el GUID para esta clave de propiedad. El identificador de propiedad (PID) es cero.

Esta propiedad es de solo lectura. Para recuperar esta propiedad, consulte el origen de red para la interfaz **IPropertyStore** y llame a **IPropertyStore:: GetValue**.

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

 

 




