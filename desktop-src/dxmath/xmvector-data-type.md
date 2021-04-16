---
description: Tipo portable que se usa para representar un vector de componentes de punto flotante de 4 32 bits o enteros, cada uno alineado de manera óptima y asignado a un registro de vector de hardware.
ms.assetid: 1a044094-444d-e787-fa6a-76e88531aef1
title: Tipo de datos XMVECTOR (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c62cab01098cd95f904ac2e2ee33d420309e8e99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708200"
---
# <a name="xmvector-data-type"></a>XMVECTOR, tipo de datos

Tipo portable que se usa para representar un vector de componentes de punto flotante de 4 32 bits o enteros, cada uno alineado de manera óptima y asignado a un registro de vector de hardware.

## <a name="remarks"></a>Observaciones

Para obtener una lista de funcionalidad adicional, como constructores y operadores, disponible `XMVECTOR` al programar en C++, vea [extensiones de XMVECTOR](ovw-xmvector-extensions.md).

En la biblioteca de DirectXMath, para admitir totalmente la portabilidad y la optimización, `XMVECTOR` es, por diseño, un tipo opaco. La implementación real de `XMVECTOR` depende de la plataforma.

En general, el código no debe basarse en los detalles de una implementación específica de la plataforma determinada de `XMVECTOR` . Las implementaciones específicas de la plataforma tienen estas características:

-   No son portátiles.
-   Pueden cambiar entre versiones.
-   El uso inprudente de los detalles de implementación puede ser poco óptimo.

Los desarrolladores deben usar las funciones de [descriptor de acceso](ovw-xnamath-reference-functions-accessors.md), [carga](ovw-xnamath-reference-functions-load.md)y [almacenamiento](ovw-xnamath-reference-functions-storage.md) de la biblioteca de directxmath para obtener y establecer los vectores, y las funciones de vector 4D de la [biblioteca directxmath](ovw-xnamath-reference-functions-vector4.md) para manipularlos.

En el caso de los proyectos que necesitan información detallada acerca de cómo implementar `XMVECTOR` en distintas plataformas, vea [Internals Library](pg-xnamath-internals.md).

### <a name="compiler-aliases"></a>Alias del compilador

El archivo de encabezado DirectXMath. h usa alias para el `XMVECTOR` objeto, específicamente **CXMVECTOR** y **FXMVECTOR**. El encabezado utiliza estos alias para cumplir con las convenciones de llamada en línea óptimas de compiladores diferentes. Para la mayoría de los proyectos que usan DirectXMath, es suficiente tratar estos tipos como un alias exacto para `XMVECTOR` .

Por ejemplo:


```
[CDATA[
typedef const XMVECTOR FXMVECTOR;
typedef const XMVECTOR CXMVECTOR;
]]
```



En el caso de los proyectos que necesitan información detallada sobre cómo las diferentes plataformas controlan sus convenciones de llamada, consulte [Internals Library](pg-xnamath-internals.md).

En el caso de XNAMATH 2. x, el `XMVECTOR` tipo de datos tiene los miembros de elemento. x,. y,. z, y. w, que generalmente causan un rendimiento deficiente. El uso del tipo de \_ VECTOR4 estricto de XM \_ proporciona una participación en la definición de DirectXMath de un tipo de datos opaco.

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

[**XMVECTORF32, tipo de datos**](xmvectorf32-data-type.md)
</dt> <dt>

[**XMVECTORU32, tipo de datos**](xmvectoru32-data-type.md)
</dt> <dt>

[**XMVECTORU8, tipo de datos**](xmvectoru8-data-type.md)
</dt> <dt>

[**XMVECTOR, tipo de datos**](xmvector-data-type.md)
</dt> </dl>

 

 




