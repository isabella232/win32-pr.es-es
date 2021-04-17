---
description: Almacena el nombre de host y el puerto del servidor proxy que usa el origen de red.
ms.assetid: 164f8ac3-08ce-40a8-ac8d-4c2a267d9db5
title: Propiedad MFNETSOURCE_PROXYINFO (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f73ceedf71e567e026c5e9af67a67c5d84bebfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716345"
---
# <a name="mfnetsource_proxyinfo-property"></a>\_Propiedad PROXYINFO de MFNETSOURCE

Almacena el nombre de host y el puerto del servidor proxy que usa el origen de red.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

Cadena de caracteres anchos (**WCHAR** \* )

VT \_ LPWStr

**pwszVal**



## <a name="remarks"></a>Observaciones

La constante **MFNETSOURCE \_ PROXYINFO** define el GUID para esta clave de propiedad. El identificador de propiedad (PID) es cero.

Esta propiedad es de solo lectura. Para obtener el valor de propiedad del origen de red, llame a **IPropertyStore:: GetValue** y pase la estructura **PROPERTYKEY** en el parámetro *key* . El miembro **fmtid** de **PROPERTYKEY** debe establecerse en el GUID de la propiedad.

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

[Compatibilidad con proxy para orígenes de red](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




