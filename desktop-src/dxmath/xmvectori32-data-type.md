---
description: Tipo opaco y portátil que admite el uso de la sintaxis del inicializador de C/C++ para cargar valores enteros en una instancia de tipo XMVECTOR.
ms.assetid: 6564030e-b6e9-0c4f-4e2a-4132e4264c94
title: Tipo de datos XMVECVEC32 (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ac36caf97a62037223840e9220876f1c7a1f09a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170418"
---
# <a name="xmvectori32-data-type"></a>Tipo de datos XMVECVEC32

Tipo opaco y portátil que admite el uso de la sintaxis del inicializador de C/C++ para cargar valores enteros en una instancia de [**tipo XMVECTOR.**](xmvector-data-type.md)


```C++
typedef XMVECTORI32 vectori32;
```



## <a name="remarks"></a>Observaciones

Para obtener una lista de funcionalidades adicionales, como constructores y operadores, disponibles al programar en `XMVECTORI32` C++, vea [Extensiones XMVECGNI32](ovw-xmvectori32-extensions.md).

Las estructuras [**XMVECTORF32,**](xmvectorf32-data-type.md) [**XMVECTORU32,**](xmvectoru32-data-type.md) **XMVECVEC32** y [**XMVECTORU8**](xmvectoru8-data-type.md) se proporcionan como un mecanismo para crear [**XMVECTOR**](xmvector-data-type.md) a partir de diferentes tipos de datos constantes (punto flotante, entero sin signo, entero y byte) mediante inicializadores.

Esto es necesario para admitir [**XMVECTOR,**](xmvector-data-type.md)ya que no admite inicializadores por motivos de portabilidad y optimización.

Por ejemplo:


```
XMVECTOR data;
XMVECTORI32 intVector = { -1, 5, 33, 0 };
data = intVector;
```



**Espacio de** nombres: uso de DirectX

### <a name="platform-requirements"></a>Requisitos de la plataforma

Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con el SDK Windows para Windows 8. Compatible con aplicaciones de escritorio Win32, Windows store y Windows Phone 8 aplicaciones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DirectXMath.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos de biblioteca de DirectXMath](ovw-xnamath-reference-types.md)
</dt> <dt>

[**Tipo de datos XMVECTOR**](xmvector-data-type.md)
</dt> <dt>

[**Tipo de datos XMVECTORF32**](xmvectorf32-data-type.md)
</dt> <dt>

[**Tipo de datos XMVECTORU32**](xmvectoru32-data-type.md)
</dt> <dt>

[**Tipo de datos XMVECTORU8**](xmvectoru8-data-type.md)
</dt> <dt>

[**Tipo de datos XMVECVEC32**](xmvectori32-data-type.md)
</dt> </dl>

 

 




