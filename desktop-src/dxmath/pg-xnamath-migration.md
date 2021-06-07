---
description: En esta introducción se describen los cambios necesarios para migrar el código existente mediante la biblioteca matemática de XNA a la biblioteca DirectXMath.
ms.assetid: ed8463f8-8a3d-e89e-89e2-8d72a7f45cd6
title: Migración de código desde la biblioteca matemática de XNA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dc7a48d30711a870c28b677e458a4f72c3b3c40
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/06/2021
ms.locfileid: "111549967"
---
# <a name="code-migration-from-the-xna-math-library"></a>Migración de código desde la biblioteca matemática de XNA

En esta introducción se describen los cambios necesarios para migrar el código existente mediante la biblioteca matemática de XNA a la biblioteca DirectXMath.

## <a name="header-changes"></a>Cambios de encabezado

La biblioteca DirectXMath usa un nuevo conjunto de encabezados.

Reemplace el `xnamath.h` encabezado por y agregue para los tipos `DirectXMath.h` `DirectXPackedVector.h` *empaquetados de GPU.*

Los tipos de límite del ejemplo de colisión del SDK de DirectX en ahora forman parte `xnacollision.h` de la biblioteca DirectXMath en `DirectXCollision.h` . Se han modificado para usar clases de C++ en lugar de una API de estilo C.

## <a name="constant-changes"></a>Cambios constantes

LA VERSIÓN XNXTTH \_ (200, 201, 202, 203, 204, y así sucesivamente) se ha reemplazado por DIRECXTMATH \_ VERSION (300, 301, 302, 303, y así sucesivamente).

> [!NOTE]  
> DirectXMath 3.00 y 3.02 se incluye con versiones preliminares del Windows SDK. DirectXMath 3.03 está en la versión final del SDK Windows 8.

## <a name="namespaces"></a>Espacios de nombres

La biblioteca DirectXMath usa espacios de nombres de C++ para organizar los tipos. XNA Math solo usaba el espacio de nombres global. Los tipos de DirectXMath en común con XNA Math se encuentran en el espacio de nombres **DirectX** o **DirectX::P ackedVector.**

En los archivos de código fuente de C++, una solución sencilla es agregar `using` instrucciones.

```cpp
#include "DirectXMath.h"
#include "DirectXPackedVector.h"

using namespace DirectX; 
using namespace DirectX::PackedVector;
```

En el caso de los encabezados, no se considera un procedimiento recomendado agregar instrucciones using. En su lugar, agregue espacios de nombres completos.

```
struct mystruct
{
   DirectX::XMFLOAT3 position;
   DirectX::PackedVector::HALF packedValue;
};
```

## <a name="partial-loads"></a>Cargas parciales

Para varias funciones que cargan menos de 4 elementos de un XMVECTOR, la biblioteca matemática de XNA dejó los elementos adicionales sin definir. DirectXMath siempre rellenará estos elementos adicionales con 0.

## <a name="removal-of-xbox-360-specific-types"></a>Eliminación de Xbox 360 tipos específicos

Los siguientes tipos, funciones y constantes de la biblioteca matemática de XNA no están disponibles en DirectXMath.

-   HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3
-   XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()
-   XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()
-   g \_ XMMaskHenD3, g \_ XMMaskDHen3, g \_ XMAddUHenD3, g \_ XMAddHenD3, g \_ XMAddDHen, g \_ XMMulHenD3, g \_ XMMulDHen3, g \_ XMXorHenD3, g \_ XMXorDHen3
-   XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4
-   XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()
-   XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()
-   g \_ XMMaskIco4, g \_ XMXorXIco4, g \_ XMXorIco4, g \_ XMAddXIco4, g \_ XMAddUIco4, g \_ XMAddIco4, g \_ XMMulIco4

\_\_vector4i está en desuso. Use [**XMVECVEC32**](xmvectori32-data-type.md) o [**XMVECTORU32 en**](xmvectoru32-data-type.md) su lugar.

Las siguientes funciones y tipos están en desuso porque solo están en Xbox 360: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.

## <a name="arm-neon-intrinsics"></a>Intrínsecos ARM-NEON

La declaración de una constante vectorial con este código se compilará para XNA Math para SSE y NO-INTRINSICS, pero se producirá un error para DirectXMath mediante ARM-NEON.

```
XMVECTOR v = { 1.f, 2.f, 3.f, 4.f }
```

En general, no se recomienda este método de inicialización de [**un XMVECTOR**](xmvector-data-type.md). Sin embargo, si desea una constante de vector, la clase [**XMVECTORF32**](xmvectorf32-data-type.md) admite este estilo de inicialización y devuelve el tipo **XMVECTOR** automáticamente para que pueda usar **XMVECTORF32** en la mayoría de los mismos contextos. Cualquier operación de escritura en **una clase XMVECTORF32** requiere hacer referencia explícitamente al miembro **XMVECTOR .v.**

## <a name="permute"></a>Permute

La biblioteca matemática XNA tenía la forma siguiente para el vector general permute:

```
XMVECTOR XMVectorPermuteControl(UINT ElementIndex0, UINT ElementIndex1, UINT ElementIndex2, UINT ElementIndex3);
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, FXMVECTOR Control);
```

Para DirectXMath, **se ha eliminado XMVectorPermuteControl** y XM \_ PERMUTE \_ 0X . Las constantes PERMUTE 1Z de XM se han redefinido para que sean índices simples de \_ \_ 0 a 7. Esta es la nueva firma para [**XMVectorPermute:**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)

```
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW);
```

En lugar de una palabra de control, esta función toma directamente los 4 índices como parámetros, lo que también hace que sea análoga a la función [**XMVectorSwzzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) mediante el nuevo XM \_ SW STALE \_ X . Constantes SW STREETW de XM \_ \_ definidas como índices simples de 0-3.

```
XMVECTOR XMVectorSwizzle(FXMVECTOR V, uint32_t E0, uint32_t E1, uint32_t E2, uint32_t E3);
```

> [!NOTE]
> Para los valores constantes, hay una manera mucho más eficaz de implementar permute. En lugar de usar el formulario de función [**de XMVectorPermute,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)use el **formulario de** plantilla:

```
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
    XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)</code></pre></td>
```

## <a name="template-forms"></a>Formularios de plantilla

En general, el uso de un formulario de plantilla sobre un formulario de función de las funciones siguientes es mucho más eficaz y permite a la biblioteca realizar optimizaciones específicas de la plataforma a través de la especialización de plantilla.

```
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
    XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)

template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW>
    XMVECTOR XMVectorSwizzle(FXMVECTOR V)

template<uint32_t Elements>
    XMVECTOR XMVectorShiftLeft(FXMVECTOR V1, FXMVECTOR V2)

template<uint32_t Elements>
    XMVECTOR XMVectorRotateLeft(FXMVECTOR V)

template<uint32_t Elements>
    XMVECTOR XMVectorRotateRight(FXMVECTOR V)

template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3>
    XMVECTOR XMVectorInsert(FXMVECTOR VD, FXMVECTOR VS)</code></pre></td>
```

## <a name="eliminated-functions"></a>Funciones eliminadas

| Función eliminada        | Replacement                                                                                                       |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| XMStoreFloat3x3NC          | [**XMStoreFloat3x3**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat3x3)                                                                        |
| XMStoreFloat4NC            | [**XMStoreFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4)                                                                            |
| XMStoreFloat4x3NC          | [**XMStoreFloat4x3**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x3)                                                                        |
| XMStoreFloat4x4NC          | [**XMStoreFloat4x4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x4)                                                                        |
| XMStoreInt4NC              | [**XMStoreInt4**](/windows/win32/api/directxmath/nf-directxmath-xmstoreint4)                                                                                |
| XMVector2InBoundsR         | [**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ? [XM \_ CRMASK \_ CR6BOUNDS:](ovw-xnamath-reference-constants.md) 0 |
| XMVector2TransformStreamNC | [**XMVector2TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformstream)                                                      |
| XMVector3InBoundsR         | [**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ? [XM \_ CRMASK \_ CR6BOUNDS:](ovw-xnamath-reference-constants.md) 0 |
| XMVector3TransformStreamNC | [**XMVector3TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)                                                      |
| XMVector4InBoundsR         | [**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ? [XM \_ CRMASK \_ CR6BOUNDS:](ovw-xnamath-reference-constants.md) 0 |
| XMVectorCosHEst            | [**XMVectorCosH**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcosh)                                                                              |
| XMVectorExpEst             | [**XMVectorExp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorexp)                                                                                |
| XMVectorLogEst             | [**XMVectorLog**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlog)                                                                                |
| XMVectorPowEst             | [**XMVectorPow**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)                                                                                |
| XMVectorSinHEst            | [**XMVectorSinH**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsinh)                                                                              |
| XMVectorTanHEst            | [**XMVectorTanH**](/windows/win32/api/directxmath/nf-directxmath-xmvectortanh)                                                                              |

## <a name="related-topics"></a>Temas relacionados

[Guía de programación de DirectXMath](ovw-xnamath-progguide.md)
