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
# <a name="xmvector-data-type"></a><span data-ttu-id="2a1b6-103">XMVECTOR, tipo de datos</span><span class="sxs-lookup"><span data-stu-id="2a1b6-103">XMVECTOR Data Type</span></span>

<span data-ttu-id="2a1b6-104">Tipo portable que se usa para representar un vector de componentes de punto flotante de 4 32 bits o enteros, cada uno alineado de manera óptima y asignado a un registro de vector de hardware.</span><span class="sxs-lookup"><span data-stu-id="2a1b6-104">A portable type used to represent a vector of four 32-bit floating-point or integer components, each aligned optimally and mapped to a hardware vector register.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a1b6-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a1b6-105">Remarks</span></span>

<span data-ttu-id="2a1b6-106">Para obtener una lista de funcionalidad adicional, como constructores y operadores, disponible `XMVECTOR` al programar en C++, vea [extensiones de XMVECTOR](ovw-xmvector-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="2a1b6-106">For a list of additional functionality, such as constructors and operators, available using `XMVECTOR` when programming in C++, see [XMVECTOR Extensions](ovw-xmvector-extensions.md).</span></span>

<span data-ttu-id="2a1b6-107">En la biblioteca de DirectXMath, para admitir totalmente la portabilidad y la optimización, `XMVECTOR` es, por diseño, un tipo opaco.</span><span class="sxs-lookup"><span data-stu-id="2a1b6-107">In the DirectXMath Library, to fully support portability and optimization, `XMVECTOR` is, by design, an opaque type.</span></span> <span data-ttu-id="2a1b6-108">La implementación real de `XMVECTOR` depende de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="2a1b6-108">The actual implementation of `XMVECTOR` is platform dependent.</span></span>

<span data-ttu-id="2a1b6-109">En general, el código no debe basarse en los detalles de una implementación específica de la plataforma determinada de `XMVECTOR` .</span><span class="sxs-lookup"><span data-stu-id="2a1b6-109">In general, code should not rely on the specifics of any given platform specific implementation of `XMVECTOR`.</span></span> <span data-ttu-id="2a1b6-110">Las implementaciones específicas de la plataforma tienen estas características:</span><span class="sxs-lookup"><span data-stu-id="2a1b6-110">Platform-specific implementations have these characteristics:</span></span>

-   <span data-ttu-id="2a1b6-111">No son portátiles.</span><span class="sxs-lookup"><span data-stu-id="2a1b6-111">They are not portable.</span></span>
-   <span data-ttu-id="2a1b6-112">Pueden cambiar entre versiones.</span><span class="sxs-lookup"><span data-stu-id="2a1b6-112">They may change between releases.</span></span>
-   <span data-ttu-id="2a1b6-113">El uso inprudente de los detalles de implementación puede ser poco óptimo.</span><span class="sxs-lookup"><span data-stu-id="2a1b6-113">Injudicious use of implementation details may be suboptimal.</span></span>

<span data-ttu-id="2a1b6-114">Los desarrolladores deben usar las funciones de [descriptor de acceso](ovw-xnamath-reference-functions-accessors.md), [carga](ovw-xnamath-reference-functions-load.md)y [almacenamiento](ovw-xnamath-reference-functions-storage.md) de la biblioteca de directxmath para obtener y establecer los vectores, y las funciones de vector 4D de la [biblioteca directxmath](ovw-xnamath-reference-functions-vector4.md) para manipularlos.</span><span class="sxs-lookup"><span data-stu-id="2a1b6-114">Developers should use DirectXMath Library's [accessor](ovw-xnamath-reference-functions-accessors.md), [load](ovw-xnamath-reference-functions-load.md), and [store](ovw-xnamath-reference-functions-storage.md) functions to get and set the vectors, and the [DirectXMath Library 4D Vector Functions](ovw-xnamath-reference-functions-vector4.md) to manipulate them.</span></span>

<span data-ttu-id="2a1b6-115">En el caso de los proyectos que necesitan información detallada acerca de cómo implementar `XMVECTOR` en distintas plataformas, vea [Internals Library](pg-xnamath-internals.md).</span><span class="sxs-lookup"><span data-stu-id="2a1b6-115">For projects that need detailed information about how to implement `XMVECTOR` on different platforms, see [Library Internals](pg-xnamath-internals.md).</span></span>

### <a name="compiler-aliases"></a><span data-ttu-id="2a1b6-116">Alias del compilador</span><span class="sxs-lookup"><span data-stu-id="2a1b6-116">Compiler Aliases</span></span>

<span data-ttu-id="2a1b6-117">El archivo de encabezado DirectXMath. h usa alias para el `XMVECTOR` objeto, específicamente **CXMVECTOR** y **FXMVECTOR**.</span><span class="sxs-lookup"><span data-stu-id="2a1b6-117">The DirectXMath.h header file uses aliases to the `XMVECTOR` object, specifically **CXMVECTOR** and **FXMVECTOR**.</span></span> <span data-ttu-id="2a1b6-118">El encabezado utiliza estos alias para cumplir con las convenciones de llamada en línea óptimas de compiladores diferentes.</span><span class="sxs-lookup"><span data-stu-id="2a1b6-118">The header uses these aliases to comply with the optimal in-line calling conventions of different compilers.</span></span> <span data-ttu-id="2a1b6-119">Para la mayoría de los proyectos que usan DirectXMath, es suficiente tratar estos tipos como un alias exacto para `XMVECTOR` .</span><span class="sxs-lookup"><span data-stu-id="2a1b6-119">For most projects that use DirectXMath it is sufficient to treat these types as an exact alias to `XMVECTOR`.</span></span>

<span data-ttu-id="2a1b6-120">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2a1b6-120">For example:</span></span>


```
[CDATA[
typedef const XMVECTOR FXMVECTOR;
typedef const XMVECTOR CXMVECTOR;
]]
```



<span data-ttu-id="2a1b6-121">En el caso de los proyectos que necesitan información detallada sobre cómo las diferentes plataformas controlan sus convenciones de llamada, consulte [Internals Library](pg-xnamath-internals.md).</span><span class="sxs-lookup"><span data-stu-id="2a1b6-121">For projects that need detailed information about how different platforms handle their calling conventions, see [Library Internals](pg-xnamath-internals.md).</span></span>

<span data-ttu-id="2a1b6-122">En el caso de XNAMATH 2. x, el `XMVECTOR` tipo de datos tiene los miembros de elemento. x,. y,. z, y. w, que generalmente causan un rendimiento deficiente.</span><span class="sxs-lookup"><span data-stu-id="2a1b6-122">For XNAMATH 2.x, the `XMVECTOR` data type has .x, .y, .z, .and .w element members, which generally cause poor performance.</span></span> <span data-ttu-id="2a1b6-123">El uso del tipo de \_ VECTOR4 estricto de XM \_ proporciona una participación en la definición de DirectXMath de un tipo de datos opaco.</span><span class="sxs-lookup"><span data-stu-id="2a1b6-123">The use of the XM\_STRICT\_VECTOR4 type provides an opt-in of the DirectXMath definition of an opaque data type.</span></span>

<span data-ttu-id="2a1b6-124">**Espacio de nombres**: usar DirectX</span><span class="sxs-lookup"><span data-stu-id="2a1b6-124">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="2a1b6-125">Requisitos de la plataforma</span><span class="sxs-lookup"><span data-stu-id="2a1b6-125">Platform Requirements</span></span>

<span data-ttu-id="2a1b6-126">Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con el Windows SDK para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2a1b6-126">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="2a1b6-127">Se admite para aplicaciones de escritorio de Win32, aplicaciones de la tienda Windows y Windows Phone 8 aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="2a1b6-127">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a1b6-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a1b6-128">Requirements</span></span>



| <span data-ttu-id="2a1b6-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a1b6-129">Requirement</span></span> | <span data-ttu-id="2a1b6-130">Value</span><span class="sxs-lookup"><span data-stu-id="2a1b6-130">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a1b6-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2a1b6-131">Header</span></span><br/> | <dl> <span data-ttu-id="2a1b6-132"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a1b6-132"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a1b6-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a1b6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a1b6-134">Tipos de biblioteca de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="2a1b6-134">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="2a1b6-135">**XMVECTORI32, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="2a1b6-135">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> <dt>

[<span data-ttu-id="2a1b6-136">**XMVECTORF32, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="2a1b6-136">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> <dt>

[<span data-ttu-id="2a1b6-137">**XMVECTORU32, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="2a1b6-137">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)
</dt> <dt>

[<span data-ttu-id="2a1b6-138">**XMVECTORU8, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="2a1b6-138">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)
</dt> <dt>

[<span data-ttu-id="2a1b6-139">**XMVECTOR, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="2a1b6-139">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> </dl>

 

 




