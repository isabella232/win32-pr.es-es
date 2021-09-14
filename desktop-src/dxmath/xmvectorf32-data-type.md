---
description: Tipo opaco y portátil que admite el uso de la sintaxis del inicializador de C/C++ para cargar valores de punto flotante en una instancia de tipo XMVECTOR.
ms.assetid: bafaa59f-fd1b-e252-cbbd-903df796fde0
title: Tipo de datos XMVECTORF32 (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e56e79ea678ede0afcac3523c09da725ede00d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170422"
---
# <a name="xmvectorf32-data-type"></a>Tipo de datos XMVECTORF32

Tipo opaco y portátil que admite el uso de la sintaxis del inicializador de C/C++ para cargar valores de punto flotante en una instancia de [**tipo XMVECTOR.**](xmvector-data-type.md)


```C++
typedef XMVECTORF32 vectorf32;
```



## <a name="remarks"></a>Observaciones

Para obtener una lista de funcionalidades adicionales, como constructores y operadores, disponibles al programar en `XMVECTORF32` C++, vea [Extensiones XMVECTORF32](ovw-xmvectorf32-extensions.md).

Las estructuras **XMVECTORF32,** [**XMVECTORU32,**](xmvectoru32-data-type.md) [**XMVECVEC32**](xmvectori32-data-type.md)y [**XMVECTORU8**](xmvectoru8-data-type.md) se proporcionan como un mecanismo para crear [**XMVECTOR**](xmvector-data-type.md) a partir de diferentes tipos de datos constantes (punto flotante, entero sin signo, entero y byte) mediante inicializadores.

Esto es necesario para admitir [**XMVECTOR,**](xmvector-data-type.md)ya que no admite inicializadores por motivos de portabilidad y optimización.

Por ejemplo:


```
XMVECTOR data;
XMVECTORF32 floatingVector = { 0.f, 0.f, 0.1f, 1.f };
data = floatingVector;
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

[**Tipo de datos XMVECVEC32**](xmvectori32-data-type.md)
</dt> <dt>

[**Tipo de datos XMVECTOR**](xmvector-data-type.md)
</dt> <dt>

[**Tipo de datos XMVECTORU32**](xmvectoru32-data-type.md)
</dt> <dt>

[**Tipo de datos XMVECTORU8**](xmvectoru8-data-type.md)
</dt> <dt>

[**Tipo de datos XMVECTORF32**](xmvectorf32-data-type.md)
</dt> </dl>

 

 




