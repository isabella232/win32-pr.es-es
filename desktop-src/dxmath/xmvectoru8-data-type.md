---
description: Tipo opaco y portátil para admitir el uso de la sintaxis del inicializador de C/C++ para cargar valores uint8 t en una instancia \_ de tipo XMVECTOR.
ms.assetid: ab73ac2c-f178-1bb9-910d-9eef5fc6f5df
title: Tipo de datos XMVECTORU8 (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4428cdd78206bfa17c295a9578653bb0a66f0c6b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359088"
---
# <a name="xmvectoru8-data-type"></a>Tipo de datos XMVECTORU8

Tipo opaco y portátil para admitir el uso de la sintaxis del inicializador de C/C++ para cargar valores uint8 t en una instancia \_ de [**tipo XMVECTOR.**](xmvector-data-type.md)


```C++
typedef XMVECTORU8 vectoru8;
```



## <a name="remarks"></a>Observaciones

Para obtener una lista de funcionalidades adicionales, como constructores y operadores, disponibles mediante XMVECTORU8 al programar en C++, vea [Extensiones XMVECTORU8](ovw-xmvectoru8-extensions.md).

Las estructuras [**XMVECTORF32,**](xmvectorf32-data-type.md) [**XMVECTORU32,**](xmvectoru32-data-type.md) [**XMVECVEC32**](xmvectori32-data-type.md)y **XMVECTORU8** se proporcionan como mecanismo para crear [**XMVECTOR**](xmvector-data-type.md) a partir de diferentes tipos de datos constantes (punto flotante, entero sin signo, entero y byte) mediante inicializadores.

Esto es necesario para admitir [**XMVECTOR,**](xmvector-data-type.md)ya que no admite inicializadores por motivos de portabilidad y optimización.

Por ejemplo:

``` syntax
XMVECTOR data;
XMVECTORU8  byteVector = { (uint8_t)  1,(uint8_t) 16,(uint8_t)101,(uint8_t) 62,
                           (uint8_t)  4,(uint8_t)  0,(uint8_t)  2,(uint8_t) 99,
                           (uint8_t)  9,(uint8_t) 18,(uint8_t)  0,(uint8_t)  0,
                           (uint8_t)100,(uint8_t) 51,(uint8_t) 23,(uint8_t)117};

data = floatingVector;
```

**Espacio de** nombres: uso de DirectX

### <a name="platform-requirements"></a>Requisitos de la plataforma

Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con el SDK de Windows para Windows 8. Compatible con aplicaciones de escritorio Win32, Windows store y Windows Phone 8 aplicaciones.

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

[**Tipo de datos XMVECVEC32**](xmvectori32-data-type.md)
</dt> <dt>

[**Tipo de datos XMVECTORU32**](xmvectoru32-data-type.md)
</dt> <dt>

[Extensiones XMVECTORU8](ovw-xmvectoru8-extensions.md)
</dt> </dl>

 

 




