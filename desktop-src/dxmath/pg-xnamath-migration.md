---
description: En esta información general se describen los cambios necesarios para migrar el código existente mediante la biblioteca matemática de XNA a la biblioteca de DirectXMath.
ms.assetid: ed8463f8-8a3d-e89e-89e2-8d72a7f45cd6
title: Migración de código desde la biblioteca matemática de XNA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c446165d3d0b6b7303424959f96ddf48bc75b5fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544078"
---
# <a name="code-migration-from-the-xna-math-library"></a>Migración de código desde la biblioteca matemática de XNA

En esta información general se describen los cambios necesarios para migrar el código existente mediante la biblioteca matemática de XNA a la biblioteca de DirectXMath.

-   [Cambios de encabezado](#header-changes)
-   [Cambios constantes](#constant-changes)
-   [Espacios de nombres](#namespaces)
-   [Cargas parciales](#partial-loads)
-   [Eliminación de tipos específicos de Xbox 360](#removal-of-xbox-360-specific-types)
-   [Intrínsecos ARM-neón](#arm-neon-intrinsics)
-   [Permute (](#permute)
-   [Formularios de plantilla](#template-forms)
-   [Funciones eliminadas](#eliminated-functions)
-   [Temas relacionados](#related-topics)

## <a name="header-changes"></a>Cambios de encabezado

La biblioteca de DirectXMath usa un nuevo conjunto de encabezados.

Reemplace el encabezado xnamath. h por DirectXMath. h y agregue DirectXPackedVector. h para los tipos "comprimidos por GPU".

Los tipos de límite del ejemplo de colisión del SDK de DirectX en xnacollision. h ahora forman parte de la biblioteca de DirectXMath en DirectXCollision. h. Se han modificado para usar clases de C++ en lugar de una API de estilo C.

## <a name="constant-changes"></a>Cambios constantes

La \_ versión de XNAMATH (200, 201, 202, 203, 204, etc.) se ha reemplazado por la versión de DIRECXTMATH \_ (300, 301, 302, 303, etc.).

> [!Note]  
> DirectXMath 3,00 y 3,02 incluye versiones preliminares de la Windows SDK. DirectXMath 3,03 está en la versión final del SDK de Windows 8.

 

## <a name="namespaces"></a>Espacios de nombres

La biblioteca de DirectXMath usa espacios de nombres de C++ para organizar los tipos. XNA Math solo usa el espacio de nombres global. Los tipos de DirectXMath en común con las matemáticas de XNA están en el espacio de nombres "DirectX" o "DirectX::P ackedVector".

En los archivos de código fuente de C++, una solución sencilla es agregar instrucciones ' Using ':


```
#include “DirectXMath.h”
#include “DirectXPackedVector.h”

using namespace DirectX; 
using namespace DirectX::PackedVector;
```



En el caso de los encabezados, no se considera ' procedimiento recomendado ' Agregar instrucciones using. En su lugar, agregue espacios de nombres completos:


```
struct mystruct
{
   DirectX::XMFLOAT3 position;
   DirectX::PackedVector::HALF packedValue;
};
```



## <a name="partial-loads"></a>Cargas parciales

En el caso de varias funciones que cargan menos de 4 elementos de un XMVECTOR, la biblioteca matemática de XNA dejó los elementos adicionales sin definir. DirectXMath siempre rellenará estos elementos adicionales con 0.

## <a name="removal-of-xbox-360-specific-types"></a>Eliminación de tipos específicos de Xbox 360

Los siguientes tipos, funciones y constantes de la biblioteca matemática de XNA no están disponibles en DirectXMath.

-   HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3
-   XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()
-   XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()
-   g \_ XMMaskHenD3, g \_ XMMaskDHen3, g \_ XMAddUHenD3, g \_ XMAddHenD3, g \_ XMAddDHen, g \_ XMMulHenD3, g \_ XMMulDHen3, g \_ XMXorHenD3, g \_ XMXorDHen3
-   XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4
-   XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()
-   XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()
-   g \_ XMMaskIco4, g \_ XMXorXIco4, g \_ XMXorIco4, g \_ XMAddXIco4, g \_ XMAddUIco4, g \_ XMAddIco4, g \_ XMMulIco4

\_\_vector4i está en desuso. Use [**XMVECTORI32**](xmvectori32-data-type.md) o [**XMVECTORU32**](xmvectoru32-data-type.md) en su lugar.

Las siguientes funciones y tipos están en desuso, ya que solo Xbox 360: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.

## <a name="arm-neon-intrinsics"></a>Intrínsecos ARM-neón

La declaración de una constante de vector con este código se compilará para las matemáticas de XNA para SSE y NO INTRÍNSECOs, pero se producirá un error en DirectXMath con ARM-neón.


```
XMVECTOR v = { 1.f, 2.f, 3.f, 4.f }
```



En general, no se recomienda este método de inicialización de un [**XMVECTOR**](xmvector-data-type.md). Sin embargo, si desea una constante de Vector, la clase [**XMVECTORF32**](xmvectorf32-data-type.md) admite este estilo de inicialización y devuelve el tipo **XMVECTOR** automáticamente para que pueda usar **XMVECTORF32** en la mayoría de los contextos. Cualquier operación de escritura en una clase **XMVECTORF32** requiere que se haga referencia explícitamente al miembro **XMVECTOR** . v.

## <a name="permute"></a>Permute (

La biblioteca matemática de XNA tenía el formato siguiente para el permute general de vectores:


```
XMVECTOR XMVectorPermuteControl(UINT ElementIndex0, UINT ElementIndex1, UINT ElementIndex2, UINT ElementIndex3);
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, FXMVECTOR Control);
```



En DirectXMath, se ha eliminado **XMVectorPermuteControl** y el de XM \_ permute \_ 0x. Las \_ constantes de 1Z de XM PERmute se han \_ redefinido para ser índices simples de 0-7. Esta es la nueva firma de [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute):


```
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW);
```



En lugar de una palabra de control, esta función toma directamente los 4 índices como parámetros, lo que también lo hace análogo a la función [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) con el nuevo SWIZZLE de XM \_ \_ X. \_ \_ Constantes de XM SWIZZLE W definidas como índices simples de 0-3.


```
XMVECTOR XMVectorSwizzle(FXMVECTOR V, uint32_t E0, uint32_t E1, uint32_t E2, uint32_t E3);
```



> [!Note]  
> En el caso de los valores constantes, existe una manera mucho más eficaz de implementar permute. En lugar de usar el formato de función de [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute), use el formulario de **plantilla** :
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
>     XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)</code></pre></td>
> </tr>
> </tbody>
> </table>
>  
>
> ## <a name="template-forms"></a>Formularios de plantilla
>
> En general, el uso de un formulario de plantilla sobre un formulario de función de las funciones siguientes es mucho más eficaz y permite que la biblioteca realice optimizaciones específicas de la plataforma a través de la especialización de la plantilla.
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
>     XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)
>
> template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW>
>     XMVECTOR XMVectorSwizzle(FXMVECTOR V)
>
> template<uint32_t Elements>
>     XMVECTOR XMVectorShiftLeft(FXMVECTOR V1, FXMVECTOR V2)
>
> template<uint32_t Elements>
>     XMVECTOR XMVectorRotateLeft(FXMVECTOR V)
>
> template<uint32_t Elements>
>     XMVECTOR XMVectorRotateRight(FXMVECTOR V)
>
> template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3>
>     XMVECTOR XMVectorInsert(FXMVECTOR VD, FXMVECTOR VS)</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> ## <a name="eliminated-functions"></a>Funciones eliminadas
>
> 
>
> | Función eliminada        | Replacement                                                                                                       |
> |----------------------------|-------------------------------------------------------------------------------------------------------------------|
> | XMStoreFloat3x3NC          | [**XMStoreFloat3x3**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat3x3)                                                                        |
> | XMStoreFloat4NC            | [**XMStoreFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4)                                                                            |
> | XMStoreFloat4x3NC          | [**XMStoreFloat4x3**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x3)                                                                        |
> | XMStoreFloat4x4NC          | [**XMStoreFloat4x4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x4)                                                                        |
> | XMStoreInt4NC              | [**XMStoreInt4**](/windows/win32/api/directxmath/nf-directxmath-xmstoreint4)                                                                                |
> | XMVector2InBoundsR         | [**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ? [XM \_ CRMASK \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0 |
> | XMVector2TransformStreamNC | [**XMVector2TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformstream)                                                      |
> | XMVector3InBoundsR         | [**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ? [XM \_ CRMASK \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0 |
> | XMVector3TransformStreamNC | [**XMVector3TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)                                                      |
> | XMVector4InBoundsR         | [**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ? [XM \_ CRMASK \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0 |
> | XMVectorCosHEst            | [**XMVectorCosH**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcosh)                                                                              |
> | XMVectorExpEst             | [**XMVectorExp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorexp)                                                                                |
> | XMVectorLogEst             | [**XMVectorLog**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlog)                                                                                |
> | XMVectorPowEst             | [**XMVectorPow**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)                                                                                |
> | XMVectorSinHEst            | [**XMVectorSinH**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsinh)                                                                              |
> | XMVectorTanHEst            | [**XMVectorTanH**](/windows/win32/api/directxmath/nf-directxmath-xmvectortanh)                                                                              |
>
> 
>
>  
>
> ## <a name="related-topics"></a>Temas relacionados
>
> <dl> <dt>

[Guía de programación de DirectXMath](ovw-xnamath-progguide.md)
</dt> </dl>
>
>  
>
>  
>
