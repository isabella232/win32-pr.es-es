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
# <a name="code-migration-from-the-xna-math-library"></a><span data-ttu-id="eb88a-103">Migración de código desde la biblioteca matemática de XNA</span><span class="sxs-lookup"><span data-stu-id="eb88a-103">Code Migration from the XNA Math Library</span></span>

<span data-ttu-id="eb88a-104">En esta información general se describen los cambios necesarios para migrar el código existente mediante la biblioteca matemática de XNA a la biblioteca de DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="eb88a-104">This overview describes the changes required to migrate existing code using the XNA Math library to the DirectXMath library.</span></span>

-   [<span data-ttu-id="eb88a-105">Cambios de encabezado</span><span class="sxs-lookup"><span data-stu-id="eb88a-105">Header Changes</span></span>](#header-changes)
-   [<span data-ttu-id="eb88a-106">Cambios constantes</span><span class="sxs-lookup"><span data-stu-id="eb88a-106">Constant Changes</span></span>](#constant-changes)
-   [<span data-ttu-id="eb88a-107">Espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="eb88a-107">Namespaces</span></span>](#namespaces)
-   [<span data-ttu-id="eb88a-108">Cargas parciales</span><span class="sxs-lookup"><span data-stu-id="eb88a-108">Partial Loads</span></span>](#partial-loads)
-   [<span data-ttu-id="eb88a-109">Eliminación de tipos específicos de Xbox 360</span><span class="sxs-lookup"><span data-stu-id="eb88a-109">Removal of Xbox 360 Specific Types</span></span>](#removal-of-xbox-360-specific-types)
-   [<span data-ttu-id="eb88a-110">Intrínsecos ARM-neón</span><span class="sxs-lookup"><span data-stu-id="eb88a-110">ARM-NEON Intrinsics</span></span>](#arm-neon-intrinsics)
-   [<span data-ttu-id="eb88a-111">Permute (</span><span class="sxs-lookup"><span data-stu-id="eb88a-111">Permute</span></span>](#permute)
-   [<span data-ttu-id="eb88a-112">Formularios de plantilla</span><span class="sxs-lookup"><span data-stu-id="eb88a-112">Template Forms</span></span>](#template-forms)
-   [<span data-ttu-id="eb88a-113">Funciones eliminadas</span><span class="sxs-lookup"><span data-stu-id="eb88a-113">Eliminated Functions</span></span>](#eliminated-functions)
-   [<span data-ttu-id="eb88a-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eb88a-114">Related topics</span></span>](#related-topics)

## <a name="header-changes"></a><span data-ttu-id="eb88a-115">Cambios de encabezado</span><span class="sxs-lookup"><span data-stu-id="eb88a-115">Header Changes</span></span>

<span data-ttu-id="eb88a-116">La biblioteca de DirectXMath usa un nuevo conjunto de encabezados.</span><span class="sxs-lookup"><span data-stu-id="eb88a-116">The DirectXMath library uses a new set of headers.</span></span>

<span data-ttu-id="eb88a-117">Reemplace el encabezado xnamath. h por DirectXMath. h y agregue DirectXPackedVector. h para los tipos "comprimidos por GPU".</span><span class="sxs-lookup"><span data-stu-id="eb88a-117">Replace the xnamath.h header with DirectXMath.h and add DirectXPackedVector.h for the “GPU packed” types.</span></span>

<span data-ttu-id="eb88a-118">Los tipos de límite del ejemplo de colisión del SDK de DirectX en xnacollision. h ahora forman parte de la biblioteca de DirectXMath en DirectXCollision. h.</span><span class="sxs-lookup"><span data-stu-id="eb88a-118">The bounding types from the DirectX SDK Collision sample in xnacollision.h is now part of the DirectXMath library in DirectXCollision.h.</span></span> <span data-ttu-id="eb88a-119">Se han modificado para usar clases de C++ en lugar de una API de estilo C.</span><span class="sxs-lookup"><span data-stu-id="eb88a-119">These have been modified to use C++ classes rather than a C-style API.</span></span>

## <a name="constant-changes"></a><span data-ttu-id="eb88a-120">Cambios constantes</span><span class="sxs-lookup"><span data-stu-id="eb88a-120">Constant Changes</span></span>

<span data-ttu-id="eb88a-121">La \_ versión de XNAMATH (200, 201, 202, 203, 204, etc.) se ha reemplazado por la versión de DIRECXTMATH \_ (300, 301, 302, 303, etc.).</span><span class="sxs-lookup"><span data-stu-id="eb88a-121">XNAMATH\_VERSION (200, 201, 202, 203, 204, and so on) has been replaced with DIRECXTMATH\_VERSION (300, 301, 302, 303, and so on).</span></span>

> [!Note]  
> <span data-ttu-id="eb88a-122">DirectXMath 3,00 y 3,02 incluye versiones preliminares de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="eb88a-122">DirectXMath 3.00 and 3.02 shipped with preliminary versions of the Windows SDK.</span></span> <span data-ttu-id="eb88a-123">DirectXMath 3,03 está en la versión final del SDK de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="eb88a-123">DirectXMath 3.03 is in the final version of the Windows 8 SDK.</span></span>

 

## <a name="namespaces"></a><span data-ttu-id="eb88a-124">Espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="eb88a-124">Namespaces</span></span>

<span data-ttu-id="eb88a-125">La biblioteca de DirectXMath usa espacios de nombres de C++ para organizar los tipos.</span><span class="sxs-lookup"><span data-stu-id="eb88a-125">The DirectXMath library uses C++ namespaces to organize the types.</span></span> <span data-ttu-id="eb88a-126">XNA Math solo usa el espacio de nombres global.</span><span class="sxs-lookup"><span data-stu-id="eb88a-126">XNA Math used only the global namespace.</span></span> <span data-ttu-id="eb88a-127">Los tipos de DirectXMath en común con las matemáticas de XNA están en el espacio de nombres "DirectX" o "DirectX::P ackedVector".</span><span class="sxs-lookup"><span data-stu-id="eb88a-127">The DirectXMath types in common with XNA Math are in the “DirectX” or the “DirectX::PackedVector” namespace.</span></span>

<span data-ttu-id="eb88a-128">En los archivos de código fuente de C++, una solución sencilla es agregar instrucciones ' Using ':</span><span class="sxs-lookup"><span data-stu-id="eb88a-128">In C++ source files, a simple solution is to add ‘using’ statements:</span></span>


```
#include “DirectXMath.h”
#include “DirectXPackedVector.h”

using namespace DirectX; 
using namespace DirectX::PackedVector;
```



<span data-ttu-id="eb88a-129">En el caso de los encabezados, no se considera ' procedimiento recomendado ' Agregar instrucciones using.</span><span class="sxs-lookup"><span data-stu-id="eb88a-129">For headers, it is not considered ‘best practice’ to add using statements.</span></span> <span data-ttu-id="eb88a-130">En su lugar, agregue espacios de nombres completos:</span><span class="sxs-lookup"><span data-stu-id="eb88a-130">Instead, add fully qualified namespaces:</span></span>


```
struct mystruct
{
   DirectX::XMFLOAT3 position;
   DirectX::PackedVector::HALF packedValue;
};
```



## <a name="partial-loads"></a><span data-ttu-id="eb88a-131">Cargas parciales</span><span class="sxs-lookup"><span data-stu-id="eb88a-131">Partial Loads</span></span>

<span data-ttu-id="eb88a-132">En el caso de varias funciones que cargan menos de 4 elementos de un XMVECTOR, la biblioteca matemática de XNA dejó los elementos adicionales sin definir.</span><span class="sxs-lookup"><span data-stu-id="eb88a-132">For various functions that load less than 4 elements of an XMVECTOR, the XNA Math library left the additional elements undefined.</span></span> <span data-ttu-id="eb88a-133">DirectXMath siempre rellenará estos elementos adicionales con 0.</span><span class="sxs-lookup"><span data-stu-id="eb88a-133">DirectXMath will always fill these additional elements with 0.</span></span>

## <a name="removal-of-xbox-360-specific-types"></a><span data-ttu-id="eb88a-134">Eliminación de tipos específicos de Xbox 360</span><span class="sxs-lookup"><span data-stu-id="eb88a-134">Removal of Xbox 360 Specific Types</span></span>

<span data-ttu-id="eb88a-135">Los siguientes tipos, funciones y constantes de la biblioteca matemática de XNA no están disponibles en DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="eb88a-135">The following XNA Math library types, functions, and constants are not available in DirectXMath.</span></span>

-   <span data-ttu-id="eb88a-136">HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3</span><span class="sxs-lookup"><span data-stu-id="eb88a-136">HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3</span></span>
-   <span data-ttu-id="eb88a-137">XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()</span><span class="sxs-lookup"><span data-stu-id="eb88a-137">XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()</span></span>
-   <span data-ttu-id="eb88a-138">XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()</span><span class="sxs-lookup"><span data-stu-id="eb88a-138">XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()</span></span>
-   <span data-ttu-id="eb88a-139">g \_ XMMaskHenD3, g \_ XMMaskDHen3, g \_ XMAddUHenD3, g \_ XMAddHenD3, g \_ XMAddDHen, g \_ XMMulHenD3, g \_ XMMulDHen3, g \_ XMXorHenD3, g \_ XMXorDHen3</span><span class="sxs-lookup"><span data-stu-id="eb88a-139">g\_XMMaskHenD3, g\_XMMaskDHen3, g\_XMAddUHenD3, g\_XMAddHenD3, g\_XMAddDHen, g\_XMMulHenD3, g\_XMMulDHen3, g\_XMXorHenD3, g\_XMXorDHen3</span></span>
-   <span data-ttu-id="eb88a-140">XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4</span><span class="sxs-lookup"><span data-stu-id="eb88a-140">XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4</span></span>
-   <span data-ttu-id="eb88a-141">XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()</span><span class="sxs-lookup"><span data-stu-id="eb88a-141">XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()</span></span>
-   <span data-ttu-id="eb88a-142">XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()</span><span class="sxs-lookup"><span data-stu-id="eb88a-142">XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()</span></span>
-   <span data-ttu-id="eb88a-143">g \_ XMMaskIco4, g \_ XMXorXIco4, g \_ XMXorIco4, g \_ XMAddXIco4, g \_ XMAddUIco4, g \_ XMAddIco4, g \_ XMMulIco4</span><span class="sxs-lookup"><span data-stu-id="eb88a-143">g\_XMMaskIco4, g\_XMXorXIco4, g\_XMXorIco4, g\_XMAddXIco4, g\_XMAddUIco4, g\_XMAddIco4, g\_XMMulIco4</span></span>

<span data-ttu-id="eb88a-144">\_\_vector4i está en desuso.</span><span class="sxs-lookup"><span data-stu-id="eb88a-144">\_\_vector4i is deprecated.</span></span> <span data-ttu-id="eb88a-145">Use [**XMVECTORI32**](xmvectori32-data-type.md) o [**XMVECTORU32**](xmvectoru32-data-type.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="eb88a-145">Use [**XMVECTORI32**](xmvectori32-data-type.md) or [**XMVECTORU32**](xmvectoru32-data-type.md) instead.</span></span>

<span data-ttu-id="eb88a-146">Las siguientes funciones y tipos están en desuso, ya que solo Xbox 360: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.</span><span class="sxs-lookup"><span data-stu-id="eb88a-146">The following functions and types are deprecated as they are Xbox 360 only: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.</span></span>

## <a name="arm-neon-intrinsics"></a><span data-ttu-id="eb88a-147">Intrínsecos ARM-neón</span><span class="sxs-lookup"><span data-stu-id="eb88a-147">ARM-NEON Intrinsics</span></span>

<span data-ttu-id="eb88a-148">La declaración de una constante de vector con este código se compilará para las matemáticas de XNA para SSE y NO INTRÍNSECOs, pero se producirá un error en DirectXMath con ARM-neón.</span><span class="sxs-lookup"><span data-stu-id="eb88a-148">Declaring a vector constant with this code will compile for XNA Math for SSE and NO-INTRINSICS, but will fail for DirectXMath using ARM-NEON.</span></span>


```
XMVECTOR v = { 1.f, 2.f, 3.f, 4.f }
```



<span data-ttu-id="eb88a-149">En general, no se recomienda este método de inicialización de un [**XMVECTOR**](xmvector-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="eb88a-149">In general, we don't recommend this method of initialization of an [**XMVECTOR**](xmvector-data-type.md).</span></span> <span data-ttu-id="eb88a-150">Sin embargo, si desea una constante de Vector, la clase [**XMVECTORF32**](xmvectorf32-data-type.md) admite este estilo de inicialización y devuelve el tipo **XMVECTOR** automáticamente para que pueda usar **XMVECTORF32** en la mayoría de los contextos.</span><span class="sxs-lookup"><span data-stu-id="eb88a-150">However, if you want a vector constant, the [**XMVECTORF32**](xmvectorf32-data-type.md) class supports this style of initialization and returns the **XMVECTOR** type automatically so you can use **XMVECTORF32** in most of the same contexts.</span></span> <span data-ttu-id="eb88a-151">Cualquier operación de escritura en una clase **XMVECTORF32** requiere que se haga referencia explícitamente al miembro **XMVECTOR** . v.</span><span class="sxs-lookup"><span data-stu-id="eb88a-151">Any write operations to an **XMVECTORF32** class require explicitly referencing the .v **XMVECTOR** member.</span></span>

## <a name="permute"></a><span data-ttu-id="eb88a-152">Permute (</span><span class="sxs-lookup"><span data-stu-id="eb88a-152">Permute</span></span>

<span data-ttu-id="eb88a-153">La biblioteca matemática de XNA tenía el formato siguiente para el permute general de vectores:</span><span class="sxs-lookup"><span data-stu-id="eb88a-153">The XNA Math library had the following form for general vector permute:</span></span>


```
XMVECTOR XMVectorPermuteControl(UINT ElementIndex0, UINT ElementIndex1, UINT ElementIndex2, UINT ElementIndex3);
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, FXMVECTOR Control);
```



<span data-ttu-id="eb88a-154">En DirectXMath, se ha eliminado **XMVectorPermuteControl** y el de XM \_ permute \_ 0x.</span><span class="sxs-lookup"><span data-stu-id="eb88a-154">For DirectXMath, **XMVectorPermuteControl** has been eliminated and the XM\_PERMUTE\_0X ..</span></span> <span data-ttu-id="eb88a-155">Las \_ constantes de 1Z de XM PERmute se han \_ redefinido para ser índices simples de 0-7.</span><span class="sxs-lookup"><span data-stu-id="eb88a-155">XM\_PERMUTE\_1Z constants have been redefined to be simple 0-7 indices.</span></span> <span data-ttu-id="eb88a-156">Esta es la nueva firma de [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute):</span><span class="sxs-lookup"><span data-stu-id="eb88a-156">Here is the new signature for [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute):</span></span>


```
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW);
```



<span data-ttu-id="eb88a-157">En lugar de una palabra de control, esta función toma directamente los 4 índices como parámetros, lo que también lo hace análogo a la función [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) con el nuevo SWIZZLE de XM \_ \_ X.</span><span class="sxs-lookup"><span data-stu-id="eb88a-157">Instead of a control word, this function directly takes the 4 indices as parameters, which also makes it analogous to the [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) function using the new XM\_SWIZZLE\_X ..</span></span> <span data-ttu-id="eb88a-158">\_ \_ Constantes de XM SWIZZLE W definidas como índices simples de 0-3.</span><span class="sxs-lookup"><span data-stu-id="eb88a-158">XM\_SWIZZLE\_W constants defined as simple 0-3 indices.</span></span>


```
XMVECTOR XMVectorSwizzle(FXMVECTOR V, uint32_t E0, uint32_t E1, uint32_t E2, uint32_t E3);
```



> [!Note]  
> <span data-ttu-id="eb88a-159">En el caso de los valores constantes, existe una manera mucho más eficaz de implementar permute.</span><span class="sxs-lookup"><span data-stu-id="eb88a-159">For constant values, there is a much more efficient way to implement permute.</span></span> <span data-ttu-id="eb88a-160">En lugar de usar el formato de función de [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute), use el formulario de **plantilla** :</span><span class="sxs-lookup"><span data-stu-id="eb88a-160">Instead of using the function form of [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute), use the **template** form:</span></span>
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
> ## <a name="template-forms"></a><span data-ttu-id="eb88a-161">Formularios de plantilla</span><span class="sxs-lookup"><span data-stu-id="eb88a-161">Template Forms</span></span>
>
> <span data-ttu-id="eb88a-162">En general, el uso de un formulario de plantilla sobre un formulario de función de las funciones siguientes es mucho más eficaz y permite que la biblioteca realice optimizaciones específicas de la plataforma a través de la especialización de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="eb88a-162">In general, using a template form over a function form of the following functions is much more efficient and allows the library to do platform specific optimizations through template specialization.</span></span>
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
> ## <a name="eliminated-functions"></a><span data-ttu-id="eb88a-163">Funciones eliminadas</span><span class="sxs-lookup"><span data-stu-id="eb88a-163">Eliminated Functions</span></span>
>
> 
>
> | <span data-ttu-id="eb88a-164">Función eliminada</span><span class="sxs-lookup"><span data-stu-id="eb88a-164">Eliminated Function</span></span>        | <span data-ttu-id="eb88a-165">Replacement</span><span class="sxs-lookup"><span data-stu-id="eb88a-165">Replacement</span></span>                                                                                                       |
> |----------------------------|-------------------------------------------------------------------------------------------------------------------|
> | <span data-ttu-id="eb88a-166">XMStoreFloat3x3NC</span><span class="sxs-lookup"><span data-stu-id="eb88a-166">XMStoreFloat3x3NC</span></span>          | [<span data-ttu-id="eb88a-167">**XMStoreFloat3x3**</span><span class="sxs-lookup"><span data-stu-id="eb88a-167">**XMStoreFloat3x3**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat3x3)                                                                        |
> | <span data-ttu-id="eb88a-168">XMStoreFloat4NC</span><span class="sxs-lookup"><span data-stu-id="eb88a-168">XMStoreFloat4NC</span></span>            | [<span data-ttu-id="eb88a-169">**XMStoreFloat4**</span><span class="sxs-lookup"><span data-stu-id="eb88a-169">**XMStoreFloat4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4)                                                                            |
> | <span data-ttu-id="eb88a-170">XMStoreFloat4x3NC</span><span class="sxs-lookup"><span data-stu-id="eb88a-170">XMStoreFloat4x3NC</span></span>          | [<span data-ttu-id="eb88a-171">**XMStoreFloat4x3**</span><span class="sxs-lookup"><span data-stu-id="eb88a-171">**XMStoreFloat4x3**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x3)                                                                        |
> | <span data-ttu-id="eb88a-172">XMStoreFloat4x4NC</span><span class="sxs-lookup"><span data-stu-id="eb88a-172">XMStoreFloat4x4NC</span></span>          | [<span data-ttu-id="eb88a-173">**XMStoreFloat4x4**</span><span class="sxs-lookup"><span data-stu-id="eb88a-173">**XMStoreFloat4x4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x4)                                                                        |
> | <span data-ttu-id="eb88a-174">XMStoreInt4NC</span><span class="sxs-lookup"><span data-stu-id="eb88a-174">XMStoreInt4NC</span></span>              | [<span data-ttu-id="eb88a-175">**XMStoreInt4**</span><span class="sxs-lookup"><span data-stu-id="eb88a-175">**XMStoreInt4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstoreint4)                                                                                |
> | <span data-ttu-id="eb88a-176">XMVector2InBoundsR</span><span class="sxs-lookup"><span data-stu-id="eb88a-176">XMVector2InBoundsR</span></span>         | <span data-ttu-id="eb88a-177">[**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="eb88a-177">[**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ?</span></span> <span data-ttu-id="eb88a-178">[XM \_ CRMASK \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span><span class="sxs-lookup"><span data-stu-id="eb88a-178">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
> | <span data-ttu-id="eb88a-179">XMVector2TransformStreamNC</span><span class="sxs-lookup"><span data-stu-id="eb88a-179">XMVector2TransformStreamNC</span></span> | [<span data-ttu-id="eb88a-180">**XMVector2TransformStream**</span><span class="sxs-lookup"><span data-stu-id="eb88a-180">**XMVector2TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformstream)                                                      |
> | <span data-ttu-id="eb88a-181">XMVector3InBoundsR</span><span class="sxs-lookup"><span data-stu-id="eb88a-181">XMVector3InBoundsR</span></span>         | <span data-ttu-id="eb88a-182">[**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="eb88a-182">[**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ?</span></span> <span data-ttu-id="eb88a-183">[XM \_ CRMASK \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span><span class="sxs-lookup"><span data-stu-id="eb88a-183">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
> | <span data-ttu-id="eb88a-184">XMVector3TransformStreamNC</span><span class="sxs-lookup"><span data-stu-id="eb88a-184">XMVector3TransformStreamNC</span></span> | [<span data-ttu-id="eb88a-185">**XMVector3TransformStream**</span><span class="sxs-lookup"><span data-stu-id="eb88a-185">**XMVector3TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)                                                      |
> | <span data-ttu-id="eb88a-186">XMVector4InBoundsR</span><span class="sxs-lookup"><span data-stu-id="eb88a-186">XMVector4InBoundsR</span></span>         | <span data-ttu-id="eb88a-187">[**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="eb88a-187">[**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ?</span></span> <span data-ttu-id="eb88a-188">[XM \_ CRMASK \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span><span class="sxs-lookup"><span data-stu-id="eb88a-188">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
> | <span data-ttu-id="eb88a-189">XMVectorCosHEst</span><span class="sxs-lookup"><span data-stu-id="eb88a-189">XMVectorCosHEst</span></span>            | [<span data-ttu-id="eb88a-190">**XMVectorCosH**</span><span class="sxs-lookup"><span data-stu-id="eb88a-190">**XMVectorCosH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorcosh)                                                                              |
> | <span data-ttu-id="eb88a-191">XMVectorExpEst</span><span class="sxs-lookup"><span data-stu-id="eb88a-191">XMVectorExpEst</span></span>             | [<span data-ttu-id="eb88a-192">**XMVectorExp**</span><span class="sxs-lookup"><span data-stu-id="eb88a-192">**XMVectorExp**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorexp)                                                                                |
> | <span data-ttu-id="eb88a-193">XMVectorLogEst</span><span class="sxs-lookup"><span data-stu-id="eb88a-193">XMVectorLogEst</span></span>             | [<span data-ttu-id="eb88a-194">**XMVectorLog**</span><span class="sxs-lookup"><span data-stu-id="eb88a-194">**XMVectorLog**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorlog)                                                                                |
> | <span data-ttu-id="eb88a-195">XMVectorPowEst</span><span class="sxs-lookup"><span data-stu-id="eb88a-195">XMVectorPowEst</span></span>             | [<span data-ttu-id="eb88a-196">**XMVectorPow**</span><span class="sxs-lookup"><span data-stu-id="eb88a-196">**XMVectorPow**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)                                                                                |
> | <span data-ttu-id="eb88a-197">XMVectorSinHEst</span><span class="sxs-lookup"><span data-stu-id="eb88a-197">XMVectorSinHEst</span></span>            | [<span data-ttu-id="eb88a-198">**XMVectorSinH**</span><span class="sxs-lookup"><span data-stu-id="eb88a-198">**XMVectorSinH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorsinh)                                                                              |
> | <span data-ttu-id="eb88a-199">XMVectorTanHEst</span><span class="sxs-lookup"><span data-stu-id="eb88a-199">XMVectorTanHEst</span></span>            | [<span data-ttu-id="eb88a-200">**XMVectorTanH**</span><span class="sxs-lookup"><span data-stu-id="eb88a-200">**XMVectorTanH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectortanh)                                                                              |
>
> 
>
>  
>
> ## <a name="related-topics"></a><span data-ttu-id="eb88a-201">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eb88a-201">Related topics</span></span>
>
> <dl> <dt>

[<span data-ttu-id="eb88a-202">Guía de programación de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="eb88a-202">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)
</dt> </dl>
>
>  
>
>  
>
