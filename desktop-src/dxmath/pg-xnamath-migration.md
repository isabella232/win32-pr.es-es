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
# <a name="code-migration-from-the-xna-math-library"></a><span data-ttu-id="8951a-103">Migración de código desde la biblioteca matemática de XNA</span><span class="sxs-lookup"><span data-stu-id="8951a-103">Code Migration from the XNA Math Library</span></span>

<span data-ttu-id="8951a-104">En esta introducción se describen los cambios necesarios para migrar el código existente mediante la biblioteca matemática de XNA a la biblioteca DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="8951a-104">This overview describes the changes required to migrate existing code using the XNA Math library to the DirectXMath library.</span></span>

## <a name="header-changes"></a><span data-ttu-id="8951a-105">Cambios de encabezado</span><span class="sxs-lookup"><span data-stu-id="8951a-105">Header Changes</span></span>

<span data-ttu-id="8951a-106">La biblioteca DirectXMath usa un nuevo conjunto de encabezados.</span><span class="sxs-lookup"><span data-stu-id="8951a-106">The DirectXMath library uses a new set of headers.</span></span>

<span data-ttu-id="8951a-107">Reemplace el `xnamath.h` encabezado por y agregue para los tipos `DirectXMath.h` `DirectXPackedVector.h` *empaquetados de GPU.*</span><span class="sxs-lookup"><span data-stu-id="8951a-107">Replace the `xnamath.h` header with `DirectXMath.h`, and add `DirectXPackedVector.h` for the *GPU packed* types.</span></span>

<span data-ttu-id="8951a-108">Los tipos de límite del ejemplo de colisión del SDK de DirectX en ahora forman parte `xnacollision.h` de la biblioteca DirectXMath en `DirectXCollision.h` .</span><span class="sxs-lookup"><span data-stu-id="8951a-108">The bounding types from the DirectX SDK Collision sample in `xnacollision.h` is now part of the DirectXMath library in `DirectXCollision.h`.</span></span> <span data-ttu-id="8951a-109">Se han modificado para usar clases de C++ en lugar de una API de estilo C.</span><span class="sxs-lookup"><span data-stu-id="8951a-109">These have been modified to use C++ classes rather than a C-style API.</span></span>

## <a name="constant-changes"></a><span data-ttu-id="8951a-110">Cambios constantes</span><span class="sxs-lookup"><span data-stu-id="8951a-110">Constant Changes</span></span>

<span data-ttu-id="8951a-111">LA VERSIÓN XNXTTH \_ (200, 201, 202, 203, 204, y así sucesivamente) se ha reemplazado por DIRECXTMATH \_ VERSION (300, 301, 302, 303, y así sucesivamente).</span><span class="sxs-lookup"><span data-stu-id="8951a-111">XNAMATH\_VERSION (200, 201, 202, 203, 204, and so on) has been replaced with DIRECXTMATH\_VERSION (300, 301, 302, 303, and so on).</span></span>

> [!NOTE]  
> <span data-ttu-id="8951a-112">DirectXMath 3.00 y 3.02 se incluye con versiones preliminares del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="8951a-112">DirectXMath 3.00 and 3.02 shipped with preliminary versions of the Windows SDK.</span></span> <span data-ttu-id="8951a-113">DirectXMath 3.03 está en la versión final del SDK Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8951a-113">DirectXMath 3.03 is in the final version of the Windows 8 SDK.</span></span>

## <a name="namespaces"></a><span data-ttu-id="8951a-114">Espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="8951a-114">Namespaces</span></span>

<span data-ttu-id="8951a-115">La biblioteca DirectXMath usa espacios de nombres de C++ para organizar los tipos.</span><span class="sxs-lookup"><span data-stu-id="8951a-115">The DirectXMath library uses C++ namespaces to organize the types.</span></span> <span data-ttu-id="8951a-116">XNA Math solo usaba el espacio de nombres global.</span><span class="sxs-lookup"><span data-stu-id="8951a-116">XNA Math used only the global namespace.</span></span> <span data-ttu-id="8951a-117">Los tipos de DirectXMath en común con XNA Math se encuentran en el espacio de nombres **DirectX** o **DirectX::P ackedVector.**</span><span class="sxs-lookup"><span data-stu-id="8951a-117">The DirectXMath types in common with XNA Math are in the **DirectX** or the **DirectX::PackedVector** namespace.</span></span>

<span data-ttu-id="8951a-118">En los archivos de código fuente de C++, una solución sencilla es agregar `using` instrucciones.</span><span class="sxs-lookup"><span data-stu-id="8951a-118">In C++ source files, a simple solution is to add `using` statements.</span></span>

```cpp
#include "DirectXMath.h"
#include "DirectXPackedVector.h"

using namespace DirectX; 
using namespace DirectX::PackedVector;
```

<span data-ttu-id="8951a-119">En el caso de los encabezados, no se considera un procedimiento recomendado agregar instrucciones using.</span><span class="sxs-lookup"><span data-stu-id="8951a-119">For headers, it is not considered best practice to add using statements.</span></span> <span data-ttu-id="8951a-120">En su lugar, agregue espacios de nombres completos.</span><span class="sxs-lookup"><span data-stu-id="8951a-120">Instead, add fully-qualified namespaces.</span></span>

```
struct mystruct
{
   DirectX::XMFLOAT3 position;
   DirectX::PackedVector::HALF packedValue;
};
```

## <a name="partial-loads"></a><span data-ttu-id="8951a-121">Cargas parciales</span><span class="sxs-lookup"><span data-stu-id="8951a-121">Partial Loads</span></span>

<span data-ttu-id="8951a-122">Para varias funciones que cargan menos de 4 elementos de un XMVECTOR, la biblioteca matemática de XNA dejó los elementos adicionales sin definir.</span><span class="sxs-lookup"><span data-stu-id="8951a-122">For various functions that load less than 4 elements of an XMVECTOR, the XNA Math library left the additional elements undefined.</span></span> <span data-ttu-id="8951a-123">DirectXMath siempre rellenará estos elementos adicionales con 0.</span><span class="sxs-lookup"><span data-stu-id="8951a-123">DirectXMath will always fill these additional elements with 0.</span></span>

## <a name="removal-of-xbox-360-specific-types"></a><span data-ttu-id="8951a-124">Eliminación de Xbox 360 tipos específicos</span><span class="sxs-lookup"><span data-stu-id="8951a-124">Removal of Xbox 360 Specific Types</span></span>

<span data-ttu-id="8951a-125">Los siguientes tipos, funciones y constantes de la biblioteca matemática de XNA no están disponibles en DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="8951a-125">The following XNA Math library types, functions, and constants are not available in DirectXMath.</span></span>

-   <span data-ttu-id="8951a-126">HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3</span><span class="sxs-lookup"><span data-stu-id="8951a-126">HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3</span></span>
-   <span data-ttu-id="8951a-127">XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()</span><span class="sxs-lookup"><span data-stu-id="8951a-127">XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()</span></span>
-   <span data-ttu-id="8951a-128">XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()</span><span class="sxs-lookup"><span data-stu-id="8951a-128">XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()</span></span>
-   <span data-ttu-id="8951a-129">g \_ XMMaskHenD3, g \_ XMMaskDHen3, g \_ XMAddUHenD3, g \_ XMAddHenD3, g \_ XMAddDHen, g \_ XMMulHenD3, g \_ XMMulDHen3, g \_ XMXorHenD3, g \_ XMXorDHen3</span><span class="sxs-lookup"><span data-stu-id="8951a-129">g\_XMMaskHenD3, g\_XMMaskDHen3, g\_XMAddUHenD3, g\_XMAddHenD3, g\_XMAddDHen, g\_XMMulHenD3, g\_XMMulDHen3, g\_XMXorHenD3, g\_XMXorDHen3</span></span>
-   <span data-ttu-id="8951a-130">XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4</span><span class="sxs-lookup"><span data-stu-id="8951a-130">XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4</span></span>
-   <span data-ttu-id="8951a-131">XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()</span><span class="sxs-lookup"><span data-stu-id="8951a-131">XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()</span></span>
-   <span data-ttu-id="8951a-132">XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()</span><span class="sxs-lookup"><span data-stu-id="8951a-132">XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()</span></span>
-   <span data-ttu-id="8951a-133">g \_ XMMaskIco4, g \_ XMXorXIco4, g \_ XMXorIco4, g \_ XMAddXIco4, g \_ XMAddUIco4, g \_ XMAddIco4, g \_ XMMulIco4</span><span class="sxs-lookup"><span data-stu-id="8951a-133">g\_XMMaskIco4, g\_XMXorXIco4, g\_XMXorIco4, g\_XMAddXIco4, g\_XMAddUIco4, g\_XMAddIco4, g\_XMMulIco4</span></span>

<span data-ttu-id="8951a-134">\_\_vector4i está en desuso.</span><span class="sxs-lookup"><span data-stu-id="8951a-134">\_\_vector4i is deprecated.</span></span> <span data-ttu-id="8951a-135">Use [**XMVECVEC32**](xmvectori32-data-type.md) o [**XMVECTORU32 en**](xmvectoru32-data-type.md) su lugar.</span><span class="sxs-lookup"><span data-stu-id="8951a-135">Use [**XMVECTORI32**](xmvectori32-data-type.md) or [**XMVECTORU32**](xmvectoru32-data-type.md) instead.</span></span>

<span data-ttu-id="8951a-136">Las siguientes funciones y tipos están en desuso porque solo están en Xbox 360: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.</span><span class="sxs-lookup"><span data-stu-id="8951a-136">The following functions and types are deprecated as they are Xbox 360 only: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.</span></span>

## <a name="arm-neon-intrinsics"></a><span data-ttu-id="8951a-137">Intrínsecos ARM-NEON</span><span class="sxs-lookup"><span data-stu-id="8951a-137">ARM-NEON Intrinsics</span></span>

<span data-ttu-id="8951a-138">La declaración de una constante vectorial con este código se compilará para XNA Math para SSE y NO-INTRINSICS, pero se producirá un error para DirectXMath mediante ARM-NEON.</span><span class="sxs-lookup"><span data-stu-id="8951a-138">Declaring a vector constant with this code will compile for XNA Math for SSE and NO-INTRINSICS, but will fail for DirectXMath using ARM-NEON.</span></span>

```
XMVECTOR v = { 1.f, 2.f, 3.f, 4.f }
```

<span data-ttu-id="8951a-139">En general, no se recomienda este método de inicialización de [**un XMVECTOR**](xmvector-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="8951a-139">In general, we don't recommend this method of initialization of an [**XMVECTOR**](xmvector-data-type.md).</span></span> <span data-ttu-id="8951a-140">Sin embargo, si desea una constante de vector, la clase [**XMVECTORF32**](xmvectorf32-data-type.md) admite este estilo de inicialización y devuelve el tipo **XMVECTOR** automáticamente para que pueda usar **XMVECTORF32** en la mayoría de los mismos contextos.</span><span class="sxs-lookup"><span data-stu-id="8951a-140">However, if you want a vector constant, the [**XMVECTORF32**](xmvectorf32-data-type.md) class supports this style of initialization and returns the **XMVECTOR** type automatically so you can use **XMVECTORF32** in most of the same contexts.</span></span> <span data-ttu-id="8951a-141">Cualquier operación de escritura en **una clase XMVECTORF32** requiere hacer referencia explícitamente al miembro **XMVECTOR .v.**</span><span class="sxs-lookup"><span data-stu-id="8951a-141">Any write operations to an **XMVECTORF32** class require explicitly referencing the .v **XMVECTOR** member.</span></span>

## <a name="permute"></a><span data-ttu-id="8951a-142">Permute</span><span class="sxs-lookup"><span data-stu-id="8951a-142">Permute</span></span>

<span data-ttu-id="8951a-143">La biblioteca matemática XNA tenía la forma siguiente para el vector general permute:</span><span class="sxs-lookup"><span data-stu-id="8951a-143">The XNA Math library had the following form for general vector permute:</span></span>

```
XMVECTOR XMVectorPermuteControl(UINT ElementIndex0, UINT ElementIndex1, UINT ElementIndex2, UINT ElementIndex3);
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, FXMVECTOR Control);
```

<span data-ttu-id="8951a-144">Para DirectXMath, **se ha eliminado XMVectorPermuteControl** y XM \_ PERMUTE \_ 0X .</span><span class="sxs-lookup"><span data-stu-id="8951a-144">For DirectXMath, **XMVectorPermuteControl** has been eliminated and the XM\_PERMUTE\_0X ..</span></span> <span data-ttu-id="8951a-145">Las constantes PERMUTE 1Z de XM se han redefinido para que sean índices simples de \_ \_ 0 a 7.</span><span class="sxs-lookup"><span data-stu-id="8951a-145">XM\_PERMUTE\_1Z constants have been redefined to be simple 0-7 indices.</span></span> <span data-ttu-id="8951a-146">Esta es la nueva firma para [**XMVectorPermute:**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)</span><span class="sxs-lookup"><span data-stu-id="8951a-146">Here is the new signature for [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute):</span></span>

```
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW);
```

<span data-ttu-id="8951a-147">En lugar de una palabra de control, esta función toma directamente los 4 índices como parámetros, lo que también hace que sea análoga a la función [**XMVectorSwzzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) mediante el nuevo XM \_ SW STALE \_ X .</span><span class="sxs-lookup"><span data-stu-id="8951a-147">Instead of a control word, this function directly takes the 4 indices as parameters, which also makes it analogous to the [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) function using the new XM\_SWIZZLE\_X ..</span></span> <span data-ttu-id="8951a-148">Constantes SW STREETW de XM \_ \_ definidas como índices simples de 0-3.</span><span class="sxs-lookup"><span data-stu-id="8951a-148">XM\_SWIZZLE\_W constants defined as simple 0-3 indices.</span></span>

```
XMVECTOR XMVectorSwizzle(FXMVECTOR V, uint32_t E0, uint32_t E1, uint32_t E2, uint32_t E3);
```

> [!NOTE]
> <span data-ttu-id="8951a-149">Para los valores constantes, hay una manera mucho más eficaz de implementar permute.</span><span class="sxs-lookup"><span data-stu-id="8951a-149">For constant values, there is a much more efficient way to implement permute.</span></span> <span data-ttu-id="8951a-150">En lugar de usar el formulario de función [**de XMVectorPermute,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)use el **formulario de** plantilla:</span><span class="sxs-lookup"><span data-stu-id="8951a-150">Instead of using the function form of [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute), use the **template** form:</span></span>

```
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
    XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)</code></pre></td>
```

## <a name="template-forms"></a><span data-ttu-id="8951a-151">Formularios de plantilla</span><span class="sxs-lookup"><span data-stu-id="8951a-151">Template Forms</span></span>

<span data-ttu-id="8951a-152">En general, el uso de un formulario de plantilla sobre un formulario de función de las funciones siguientes es mucho más eficaz y permite a la biblioteca realizar optimizaciones específicas de la plataforma a través de la especialización de plantilla.</span><span class="sxs-lookup"><span data-stu-id="8951a-152">In general, using a template form over a function form of the following functions is much more efficient and allows the library to do platform specific optimizations through template specialization.</span></span>

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

## <a name="eliminated-functions"></a><span data-ttu-id="8951a-153">Funciones eliminadas</span><span class="sxs-lookup"><span data-stu-id="8951a-153">Eliminated Functions</span></span>

| <span data-ttu-id="8951a-154">Función eliminada</span><span class="sxs-lookup"><span data-stu-id="8951a-154">Eliminated Function</span></span>        | <span data-ttu-id="8951a-155">Replacement</span><span class="sxs-lookup"><span data-stu-id="8951a-155">Replacement</span></span>                                                                                                       |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8951a-156">XMStoreFloat3x3NC</span><span class="sxs-lookup"><span data-stu-id="8951a-156">XMStoreFloat3x3NC</span></span>          | [<span data-ttu-id="8951a-157">**XMStoreFloat3x3**</span><span class="sxs-lookup"><span data-stu-id="8951a-157">**XMStoreFloat3x3**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat3x3)                                                                        |
| <span data-ttu-id="8951a-158">XMStoreFloat4NC</span><span class="sxs-lookup"><span data-stu-id="8951a-158">XMStoreFloat4NC</span></span>            | [<span data-ttu-id="8951a-159">**XMStoreFloat4**</span><span class="sxs-lookup"><span data-stu-id="8951a-159">**XMStoreFloat4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4)                                                                            |
| <span data-ttu-id="8951a-160">XMStoreFloat4x3NC</span><span class="sxs-lookup"><span data-stu-id="8951a-160">XMStoreFloat4x3NC</span></span>          | [<span data-ttu-id="8951a-161">**XMStoreFloat4x3**</span><span class="sxs-lookup"><span data-stu-id="8951a-161">**XMStoreFloat4x3**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x3)                                                                        |
| <span data-ttu-id="8951a-162">XMStoreFloat4x4NC</span><span class="sxs-lookup"><span data-stu-id="8951a-162">XMStoreFloat4x4NC</span></span>          | [<span data-ttu-id="8951a-163">**XMStoreFloat4x4**</span><span class="sxs-lookup"><span data-stu-id="8951a-163">**XMStoreFloat4x4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x4)                                                                        |
| <span data-ttu-id="8951a-164">XMStoreInt4NC</span><span class="sxs-lookup"><span data-stu-id="8951a-164">XMStoreInt4NC</span></span>              | [<span data-ttu-id="8951a-165">**XMStoreInt4**</span><span class="sxs-lookup"><span data-stu-id="8951a-165">**XMStoreInt4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstoreint4)                                                                                |
| <span data-ttu-id="8951a-166">XMVector2InBoundsR</span><span class="sxs-lookup"><span data-stu-id="8951a-166">XMVector2InBoundsR</span></span>         | <span data-ttu-id="8951a-167">[**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="8951a-167">[**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ?</span></span> <span data-ttu-id="8951a-168">[XM \_ CRMASK \_ CR6BOUNDS:](ovw-xnamath-reference-constants.md) 0</span><span class="sxs-lookup"><span data-stu-id="8951a-168">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
| <span data-ttu-id="8951a-169">XMVector2TransformStreamNC</span><span class="sxs-lookup"><span data-stu-id="8951a-169">XMVector2TransformStreamNC</span></span> | [<span data-ttu-id="8951a-170">**XMVector2TransformStream**</span><span class="sxs-lookup"><span data-stu-id="8951a-170">**XMVector2TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformstream)                                                      |
| <span data-ttu-id="8951a-171">XMVector3InBoundsR</span><span class="sxs-lookup"><span data-stu-id="8951a-171">XMVector3InBoundsR</span></span>         | <span data-ttu-id="8951a-172">[**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="8951a-172">[**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ?</span></span> <span data-ttu-id="8951a-173">[XM \_ CRMASK \_ CR6BOUNDS:](ovw-xnamath-reference-constants.md) 0</span><span class="sxs-lookup"><span data-stu-id="8951a-173">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
| <span data-ttu-id="8951a-174">XMVector3TransformStreamNC</span><span class="sxs-lookup"><span data-stu-id="8951a-174">XMVector3TransformStreamNC</span></span> | [<span data-ttu-id="8951a-175">**XMVector3TransformStream**</span><span class="sxs-lookup"><span data-stu-id="8951a-175">**XMVector3TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)                                                      |
| <span data-ttu-id="8951a-176">XMVector4InBoundsR</span><span class="sxs-lookup"><span data-stu-id="8951a-176">XMVector4InBoundsR</span></span>         | <span data-ttu-id="8951a-177">[**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="8951a-177">[**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ?</span></span> <span data-ttu-id="8951a-178">[XM \_ CRMASK \_ CR6BOUNDS:](ovw-xnamath-reference-constants.md) 0</span><span class="sxs-lookup"><span data-stu-id="8951a-178">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
| <span data-ttu-id="8951a-179">XMVectorCosHEst</span><span class="sxs-lookup"><span data-stu-id="8951a-179">XMVectorCosHEst</span></span>            | [<span data-ttu-id="8951a-180">**XMVectorCosH**</span><span class="sxs-lookup"><span data-stu-id="8951a-180">**XMVectorCosH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorcosh)                                                                              |
| <span data-ttu-id="8951a-181">XMVectorExpEst</span><span class="sxs-lookup"><span data-stu-id="8951a-181">XMVectorExpEst</span></span>             | [<span data-ttu-id="8951a-182">**XMVectorExp**</span><span class="sxs-lookup"><span data-stu-id="8951a-182">**XMVectorExp**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorexp)                                                                                |
| <span data-ttu-id="8951a-183">XMVectorLogEst</span><span class="sxs-lookup"><span data-stu-id="8951a-183">XMVectorLogEst</span></span>             | [<span data-ttu-id="8951a-184">**XMVectorLog**</span><span class="sxs-lookup"><span data-stu-id="8951a-184">**XMVectorLog**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorlog)                                                                                |
| <span data-ttu-id="8951a-185">XMVectorPowEst</span><span class="sxs-lookup"><span data-stu-id="8951a-185">XMVectorPowEst</span></span>             | [<span data-ttu-id="8951a-186">**XMVectorPow**</span><span class="sxs-lookup"><span data-stu-id="8951a-186">**XMVectorPow**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)                                                                                |
| <span data-ttu-id="8951a-187">XMVectorSinHEst</span><span class="sxs-lookup"><span data-stu-id="8951a-187">XMVectorSinHEst</span></span>            | [<span data-ttu-id="8951a-188">**XMVectorSinH**</span><span class="sxs-lookup"><span data-stu-id="8951a-188">**XMVectorSinH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorsinh)                                                                              |
| <span data-ttu-id="8951a-189">XMVectorTanHEst</span><span class="sxs-lookup"><span data-stu-id="8951a-189">XMVectorTanHEst</span></span>            | [<span data-ttu-id="8951a-190">**XMVectorTanH**</span><span class="sxs-lookup"><span data-stu-id="8951a-190">**XMVectorTanH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectortanh)                                                                              |

## <a name="related-topics"></a><span data-ttu-id="8951a-191">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8951a-191">Related topics</span></span>

[<span data-ttu-id="8951a-192">Guía de programación de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="8951a-192">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)
