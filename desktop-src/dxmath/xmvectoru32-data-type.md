---
description: Tipo opaco y portátil para admitir el uso de la sintaxis del inicializador de C/C++ para cargar valores uint32 t en una instancia de \_ tipo XMVECTOR.
ms.assetid: 1ac1f48a-cd7f-7741-933f-c341fc42a21c
title: Tipo de datos XMVECTORU32 (Directxmath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f13d37a5630df37021637bed978943a48a665db16301f2067c82f050a8231bbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891685"
---
# <a name="xmvectoru32-data-type"></a>Tipo de datos XMVECTORU32

Tipo opaco y portátil para admitir el uso de la sintaxis del inicializador de C/C++ para cargar valores uint32 t en una instancia de \_ [**tipo XMVECTOR.**](xmvector-data-type.md)


```C++
typedef XMVECTOR32 vectoru32;
```



## <a name="remarks"></a>Comentarios

Para obtener una lista de funcionalidades adicionales, como constructores y operadores, disponibles mediante XMVECTORU32 al programar en C++, vea [Extensiones XMVECTORU32](ovw-xmvectoru32-extensions.md).

Las estructuras [**XMVECTORF32,**](xmvectorf32-data-type.md) **XMVECTORU32,** [**XMVECVEC32**](xmvectori32-data-type.md)y [**XMVECTORU8**](xmvectoru8-data-type.md) se proporcionan como mecanismo para crear [**XMVECTOR**](xmvector-data-type.md) a partir de diferentes tipos de datos constantes (punto flotante, entero sin signo, entero y byte) mediante inicializadores.

Esto es necesario para admitir [**XMVECTOR,**](xmvector-data-type.md)ya que no admite inicializadores por motivos de portabilidad y optimización.

Por ejemplo:

``` syntax
XMVECTOR data;
XMVECTORU32 uintVector = { 0xf7000000, 0x8310000, 0x1000000, 0 };
data = uintVector;
```

**Espacio de** nombres: uso de DirectX

### <a name="platform-requirements"></a>Requisitos de la plataforma

Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con el SDK Windows para Windows 8. Compatible con aplicaciones de escritorio Win32, Windows store y Windows Phone 8 aplicaciones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Directxmath.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos de biblioteca de DirectXMath](ovw-xnamath-reference-types.md)
</dt> <dt>

[**Tipo de datos XMVECVEC32**](xmvectori32-data-type.md)
</dt> <dt>

[**Tipo de datos XMVECTORF32**](xmvectorf32-data-type.md)
</dt> <dt>

[**Tipo de datos XMVECTOR**](xmvector-data-type.md)
</dt> <dt>

[**Tipo de datos XMVECTORU8**](xmvectoru8-data-type.md)
</dt> <dt>

[Extensiones XMVECTORU32](ovw-xmvectoru32-extensions.md)
</dt> </dl>

 

 




