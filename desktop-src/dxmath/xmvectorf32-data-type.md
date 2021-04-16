---
description: Un tipo opaco y portátil para admitir el uso de la sintaxis de inicializador de C/C++ para cargar valores de punto flotante en una instancia de tipo XMVECTOR.
ms.assetid: bafaa59f-fd1b-e252-cbbd-903df796fde0
title: Tipo de datos XMVECTORF32 (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e56e79ea678ede0afcac3523c09da725ede00d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649899"
---
# <a name="xmvectorf32-data-type"></a>XMVECTORF32, tipo de datos

Un tipo opaco y portátil para admitir el uso de la sintaxis de inicializador de C/C++ para cargar valores de punto flotante en una instancia de tipo [**XMVECTOR**](xmvector-data-type.md) .


```C++
typedef XMVECTORF32 vectorf32;
```



## <a name="remarks"></a>Observaciones

Para obtener una lista de funcionalidad adicional, como constructores y operadores, disponible `XMVECTORF32` al programar en C++, vea [extensiones de XMVECTORF32](ovw-xmvectorf32-extensions.md).

Las estructuras **XMVECTORF32**, [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md)y [**XMVECTORU8**](xmvectoru8-data-type.md) se proporcionan como un mecanismo para crear [**XMVECTOR**](xmvector-data-type.md) de diferentes tipos de datos constantes (punto flotante, entero sin signo, entero y byte) mediante inicializadores.

Esto es necesario para admitir [**XMVECTOR**](xmvector-data-type.md), ya que no admite inicializadores, por motivos de portabilidad y optimización.

Por ejemplo:


```
XMVECTOR data;
XMVECTORF32 floatingVector = { 0.f, 0.f, 0.1f, 1.f };
data = floatingVector;
```



**Espacio de nombres**: usar DirectX

### <a name="platform-requirements"></a>Requisitos de la plataforma

Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con el Windows SDK para Windows 8. Se admite para aplicaciones de escritorio de Win32, aplicaciones de la tienda Windows y Windows Phone 8 aplicaciones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DirectXMath. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos de biblioteca de DirectXMath](ovw-xnamath-reference-types.md)
</dt> <dt>

[**XMVECTORI32, tipo de datos**](xmvectori32-data-type.md)
</dt> <dt>

[**XMVECTOR, tipo de datos**](xmvector-data-type.md)
</dt> <dt>

[**XMVECTORU32, tipo de datos**](xmvectoru32-data-type.md)
</dt> <dt>

[**XMVECTORU8, tipo de datos**](xmvectoru8-data-type.md)
</dt> <dt>

[**XMVECTORF32, tipo de datos**](xmvectorf32-data-type.md)
</dt> </dl>

 

 




