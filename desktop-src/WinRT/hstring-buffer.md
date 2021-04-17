---
description: Identificador de un búfer de cadena mutable que se puede usar para crear un HSTRING.
ms.assetid: D173CE70-ABF3-4703-A229-0753F2AF6F70
title: HSTRING_BUFFER (hstring. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d70b961d442739e084e3b17d5666653c103cc35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696412"
---
# <a name="hstring_buffer"></a>\_búfer HSTRING

Identificador de un búfer de cadena mutable que se puede usar para crear un [**HSTRING**](hstring.md).


```C++
typedef HANDLE HSTRING_BUFFER;
```



## <a name="remarks"></a>Observaciones

**HSTRING \_ BUFFER** representa un búfer de cadena que se puede modificar antes de convertirlo en un [**HSTRING**](hstring.md)inmutable.

Llame a la función [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) para crear **un \_ búfer de HSTRING**. Llame a [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) para convertir un **\_ búfer de HSTRING** en un [**HSTRING**](hstring.md)inmutable.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Hstring. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>


</dt> <dt>

[**HSTRING**](hstring.md)
</dt> <dt>

[**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> <dt>

[**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer)
</dt> </dl>

 

 
