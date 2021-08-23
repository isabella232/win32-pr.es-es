---
description: Identificador de un búfer de cadena mutable que puede usar para crear un HSTRING.
ms.assetid: D173CE70-ABF3-4703-A229-0753F2AF6F70
title: HSTRING_BUFFER (Hstring.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f115ca18b4bf5b81bbd7004259aa525517c05a3adc0f6376f7d16df3e3ce679
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733825"
---
# <a name="hstring_buffer"></a>HSTRING \_ BUFFER

Identificador de un búfer de cadena mutable que puede usar para crear una [**cadena HSTRING.**](hstring.md)


```C++
typedef HANDLE HSTRING_BUFFER;
```



## <a name="remarks"></a>Comentarios

**HSTRING \_ BUFFER** representa un búfer de cadena que se puede modificar antes de convertirlo en un [**HSTRING inmutable.**](hstring.md)

Llame a [**la función WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) para crear un **búfer de HSTRING. \_** Llame a [**WindowsPromoteStringBuffer para**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) convertir un búfer **de HSTRING \_** en un [**HSTRING inmutable.**](hstring.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                       |
| Header<br/>                   | <dl> <dt>Hstring.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>


</dt> <dt>

[**HSTRING**](hstring.md)
</dt> <dt>

[**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> <dt>

[**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer)
</dt> </dl>

 

 
