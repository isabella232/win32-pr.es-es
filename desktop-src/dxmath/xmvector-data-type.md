---
description: Tipo portátil que se usa para representar un vector de cuatro componentes de punto flotante o entero de 32 bits, cada uno alineado de forma óptima y asignado a un registro de vector de hardware.
ms.assetid: 1a044094-444d-e787-fa6a-76e88531aef1
title: Tipo de datos XMVECTOR (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0a65c7da346163c3cbfaab7c68982f56eb6c424b7f74a3ec01c754eb4104a5e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094485"
---
# <a name="xmvector-data-type"></a>Tipo de datos XMVECTOR

Tipo portátil que se usa para representar un vector de cuatro componentes de punto flotante o entero de 32 bits, cada uno alineado de forma óptima y asignado a un registro de vector de hardware.

## <a name="remarks"></a>Comentarios

Para obtener una lista de funcionalidades adicionales, como constructores y operadores, disponibles mediante al programar `XMVECTOR` en C++, vea [Extensiones XMVECTOR](ovw-xmvector-extensions.md).

En la biblioteca DirectXMath, para admitir totalmente la portabilidad y la optimización, es, por `XMVECTOR` diseño, un tipo opaco. La implementación real de depende `XMVECTOR` de la plataforma.

En general, el código no debe basarse en los detalles de ninguna implementación específica de plataforma determinada de `XMVECTOR` . Las implementaciones específicas de la plataforma tienen estas características:

-   No son portátiles.
-   Pueden cambiar entre versiones.
-   El uso injudioso de los detalles de implementación puede ser inofóptico.

Los desarrolladores deben usar las funciones [](ovw-xnamath-reference-functions-load.md)de [accessor,](ovw-xnamath-reference-functions-accessors.md)load y store de la biblioteca DirectXMath para obtener y establecer los vectores, y las funciones [vectores 4D](ovw-xnamath-reference-functions-vector4.md) de la biblioteca DirectXMath para manipularlos. [](ovw-xnamath-reference-functions-storage.md)

Para los proyectos que necesitan información detallada sobre cómo implementar `XMVECTOR` en distintas [plataformas,](pg-xnamath-internals.md)vea Library Internals .

### <a name="compiler-aliases"></a>Alias del compilador

El archivo de encabezado DirectXMath.h usa alias para el objeto, en concreto `XMVECTOR` **CXMVECTOR** y **FXMVECTOR.** El encabezado usa estos alias para cumplir las convenciones de llamada en línea óptimas de diferentes compiladores. Para la mayoría de los proyectos que usan DirectXMath, es suficiente tratar estos tipos como un alias exacto para `XMVECTOR` .

Por ejemplo:


```
[CDATA[
typedef const XMVECTOR FXMVECTOR;
typedef const XMVECTOR CXMVECTOR;
]]
```



Para los proyectos que necesitan información detallada sobre cómo las distintas plataformas controlan sus convenciones de llamada, vea [Library Internals](pg-xnamath-internals.md).

Para XNAMATH 2.x, el tipo de datos tiene miembros de elementos `XMVECTOR` .x, .y, .z, .y .w, lo que suele provocar un rendimiento deficiente. El uso del tipo XM STRICT VECTOR4 proporciona una opción de la definición \_ \_ de DirectXMath de un tipo de datos opaco.

**Espacio de** nombres: uso de DirectX

### <a name="platform-requirements"></a>Requisitos de la plataforma

Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con el SDK Windows para Windows 8. Compatible con aplicaciones de escritorio Win32, Windows store y Windows Phone 8 aplicaciones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DirectXMath.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Tipos de biblioteca de DirectXMath](ovw-xnamath-reference-types.md)
</dt> <dt>

[**Tipo de datos XMVECVEC32**](xmvectori32-data-type.md)
</dt> <dt>

[**Tipo de datos XMVECTORF32**](xmvectorf32-data-type.md)
</dt> <dt>

[**Tipo de datos XMVECTORU32**](xmvectoru32-data-type.md)
</dt> <dt>

[**Tipo de datos XMVECTORU8**](xmvectoru8-data-type.md)
</dt> <dt>

[**Tipo de datos XMVECTOR**](xmvector-data-type.md)
</dt> </dl>

 

 




