---
description: Un tipo opaco y portátil para admitir el uso de la sintaxis de inicializador de C/C++ para cargar \_ valores UInt32 t en una instancia de tipo XMVECTOR.
ms.assetid: 1ac1f48a-cd7f-7741-933f-c341fc42a21c
title: Tipo de datos XMVECTORU32 (Directxmath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90c7a64d42bc4638573b987642c0cd77c37cc12d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708958"
---
# <a name="xmvectoru32-data-type"></a>XMVECTORU32, tipo de datos

Un tipo opaco y portátil para admitir el uso de la sintaxis de inicializador de C/C++ para cargar \_ valores UInt32 t en una instancia de tipo [**XMVECTOR**](xmvector-data-type.md) .


```C++
typedef XMVECTOR32 vectoru32;
```



## <a name="remarks"></a>Observaciones

Para obtener una lista de funcionalidad adicional, como constructores y operadores, disponible mediante XMVECTORU32 al programar en C++, vea [extensiones de XMVECTORU32](ovw-xmvectoru32-extensions.md).

Las estructuras [**XMVECTORF32**](xmvectorf32-data-type.md), **XMVECTORU32**, [**XMVECTORI32**](xmvectori32-data-type.md)y [**XMVECTORU8**](xmvectoru8-data-type.md) se proporcionan como un mecanismo para crear [**XMVECTOR**](xmvector-data-type.md) de diferentes tipos de datos constantes (punto flotante, entero sin signo, entero y byte) mediante inicializadores.

Esto es necesario para admitir [**XMVECTOR**](xmvector-data-type.md), ya que no admite inicializadores, por motivos de portabilidad y optimización.

Por ejemplo:

``` syntax
XMVECTOR data;
XMVECTORU32 uintVector = { 0xf7000000, 0x8310000, 0x1000000, 0 };
data = uintVector;
```

**Espacio de nombres**: usar DirectX

### <a name="platform-requirements"></a>Requisitos de la plataforma

Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con el Windows SDK para Windows 8. Se admite para aplicaciones de escritorio de Win32, aplicaciones de la tienda Windows y Windows Phone 8 aplicaciones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Directxmath. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos de biblioteca de DirectXMath](ovw-xnamath-reference-types.md)
</dt> <dt>

[**XMVECTORI32, tipo de datos**](xmvectori32-data-type.md)
</dt> <dt>

[**XMVECTORF32, tipo de datos**](xmvectorf32-data-type.md)
</dt> <dt>

[**XMVECTOR, tipo de datos**](xmvector-data-type.md)
</dt> <dt>

[**XMVECTORU8, tipo de datos**](xmvectoru8-data-type.md)
</dt> <dt>

[Extensiones de XMVECTORU32](ovw-xmvectoru32-extensions.md)
</dt> </dl>

 

 




