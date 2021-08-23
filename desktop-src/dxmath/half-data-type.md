---
description: Alias para uint16 t empaquetado con un número de punto flotante de 16 bits que consta de un bit de signo, un exponente sesgado de 5 bits y una \_ mantisa de 10 bits.
ms.assetid: E84E0EBA-5C34-41AA-84DB-7A65EBDCAD15
title: Tipo de datos HALF (DirectXPackedVector.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a59b7288324ae5935a23e67a35f402ab6041da55073915d812b39096cab30733
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985045"
---
# <a name="half-data-type"></a>HALF Data Type

Alias para **uint16 \_ t** empaquetado con un número de punto flotante de 16 bits que consta de un bit de signo, un exponente sesgado de 5 bits y una mantisa de 10 bits.


```C++
typedef uint16_t HALF;
```



## <a name="remarks"></a>Comentarios

El tipo de datos HALF es equivalente al formato binary16 IEEE 754.

HALF \_ MIN = 6,10352e-5f

HALF \_ MAX = 65504.f

Para obtener más información sobre el tipo de datos HALF, vea [Formato de punto flotante de precisión media.](https://en.wikipedia.org/wiki/Half_precision_floating-point_format)

**Espacio** de nombres: Use DirectX::P ackedVector

### <a name="platform-requirements"></a>Requisitos de la plataforma

Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con el SDK Windows para Windows 8. Compatible con aplicaciones de escritorio Win32, Windows store y Windows Phone 8 aplicaciones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DirectXPackedVector.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos de biblioteca de DirectXMath](ovw-xnamath-reference-types.md)
</dt> </dl>

 

 




