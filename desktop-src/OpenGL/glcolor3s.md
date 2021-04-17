---
title: función glColor3s (GL. h)
description: Establece el color actual. | función glColor3s (GL. h)
ms.assetid: 6d4308c7-d640-447d-8efc-1fd547975516
keywords:
- glColor3s (función) OpenGL
topic_type:
- apiref
api_name:
- glColor3s
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f909c93ebb09417330363ad4913bd902213019e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105670189"
---
# <a name="glcolor3s-function"></a><span data-ttu-id="0783a-105">glColor3s función)</span><span class="sxs-lookup"><span data-stu-id="0783a-105">glColor3s function</span></span>

<span data-ttu-id="0783a-106">Establece el color actual.</span><span class="sxs-lookup"><span data-stu-id="0783a-106">Sets the current color.</span></span>

## <a name="syntax"></a><span data-ttu-id="0783a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0783a-107">Syntax</span></span>


```C++
void WINAPI glColor3s(
   GLshort red,
   GLshort green,
   GLshort blue
);
```



## <a name="parameters"></a><span data-ttu-id="0783a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0783a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0783a-109">*alerta*</span><span class="sxs-lookup"><span data-stu-id="0783a-109">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="0783a-110">Nuevo valor rojo para el color actual.</span><span class="sxs-lookup"><span data-stu-id="0783a-110">The new red value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="0783a-111">*verde*</span><span class="sxs-lookup"><span data-stu-id="0783a-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="0783a-112">Nuevo valor verde para el color actual.</span><span class="sxs-lookup"><span data-stu-id="0783a-112">The new green value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="0783a-113">*azul*</span><span class="sxs-lookup"><span data-stu-id="0783a-113">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="0783a-114">Nuevo valor azul para el color actual.</span><span class="sxs-lookup"><span data-stu-id="0783a-114">The new blue value for the current color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0783a-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0783a-115">Return value</span></span>

<span data-ttu-id="0783a-116">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="0783a-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0783a-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0783a-117">Remarks</span></span>

<span data-ttu-id="0783a-118">El libro de contabilidad almacena un índice de color de un solo valor actual y un color RGBA de cuatro valores actual.</span><span class="sxs-lookup"><span data-stu-id="0783a-118">The GL stores both a current single-valued color index and a current four-valued RGBA color.</span></span> <span data-ttu-id="0783a-119">**glcolor** establece un nuevo color RGBA de cuatro valores.</span><span class="sxs-lookup"><span data-stu-id="0783a-119">**glcolor** sets a new four-valued RGBA color.</span></span> <span data-ttu-id="0783a-120">**glcolor** tiene dos variantes principales: **glcolor3** y **glcolor4**.</span><span class="sxs-lookup"><span data-stu-id="0783a-120">**glcolor** has two major variants: **glcolor3** and **glcolor4**.</span></span> <span data-ttu-id="0783a-121">las variantes de **glcolor3** especifican nuevos valores rojo, verde y azul explícitamente y establecen el valor alfa actual en 1,0 (intensidad total) implícitamente.</span><span class="sxs-lookup"><span data-stu-id="0783a-121">**glcolor3** variants specify new red, green, and blue values explicitly and set the current alpha value to 1.0 (full intensity) implicitly.</span></span> <span data-ttu-id="0783a-122">las variantes de **glcolor4** especifican los cuatro componentes de color explícitamente.</span><span class="sxs-lookup"><span data-stu-id="0783a-122">**glcolor4** variants specify all four color components explicitly.</span></span>

<span data-ttu-id="0783a-123">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i** y **glcolor4i** toman tres o cuatro enteros con signo, cortos o largos como argumentos.</span><span class="sxs-lookup"><span data-stu-id="0783a-123">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i**, and **glcolor4i** take three or four signed byte, short, or long integers as arguments.</span></span> <span data-ttu-id="0783a-124">Cuando se anexa v al nombre, los comandos de color pueden tomar un puntero a una matriz de estos valores.</span><span class="sxs-lookup"><span data-stu-id="0783a-124">When v is appended to the name, the color commands can take a pointer to an array of such values.</span></span>

<span data-ttu-id="0783a-125">Los valores de color actuales se almacenan en formato de punto flotante, con la mantisa y los tamaños de exponente no especificados.</span><span class="sxs-lookup"><span data-stu-id="0783a-125">Current color values are stored in floating-point format, with unspecified mantissa and exponent sizes.</span></span> <span data-ttu-id="0783a-126">Los componentes de color de entero sin signo, cuando se especifican, se asignan linealmente a valores de punto flotante, de modo que el mayor valor que se puede representar se asigna a 1,0 (intensidad total) y 0 se asigna a 0,0 (intensidad cero).</span><span class="sxs-lookup"><span data-stu-id="0783a-126">Unsigned integer color components, when specified, are linearly mapped to floating-point values such that the largest representable value maps to 1.0 (full intensity), and 0 maps to 0.0 (zero intensity).</span></span> <span data-ttu-id="0783a-127">Los componentes de color de entero con signo, cuando se especifican, se asignan linealmente a valores de punto flotante, de modo que el valor representable más positivo se asigna a 1,0 y el valor representable más negativo se asigna a-1,0.</span><span class="sxs-lookup"><span data-stu-id="0783a-127">Signed integer color components, when specified, are linearly mapped to floating-point values such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="0783a-128">(Tenga en cuenta que esta asignación no convierte 0 exactamente a 0,0). Los valores de punto flotante se asignan directamente.</span><span class="sxs-lookup"><span data-stu-id="0783a-128">(Note that this mapping does not convert 0 precisely to 0.0.) Floating-point values are mapped directly.</span></span>

<span data-ttu-id="0783a-129">Ninguno de los valores de punto flotante ni de entero con signo se fijan en el intervalo de \[ 0 a 1 \] antes de que se actualice el color actual.</span><span class="sxs-lookup"><span data-stu-id="0783a-129">Neither floating-point nor signed integer values are clamped to the range \[0,1\] before the current color is updated.</span></span> <span data-ttu-id="0783a-130">Sin embargo, los componentes de color se fijan en este intervalo antes de que se interpolen o se escriban en un búfer de color.</span><span class="sxs-lookup"><span data-stu-id="0783a-130">However, color components are clamped to this range before they are interpolated or written into a color buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="0783a-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0783a-131">Requirements</span></span>



| <span data-ttu-id="0783a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="0783a-132">Requirement</span></span> | <span data-ttu-id="0783a-133">Value</span><span class="sxs-lookup"><span data-stu-id="0783a-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0783a-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0783a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0783a-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0783a-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0783a-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0783a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0783a-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0783a-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0783a-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0783a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="0783a-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="0783a-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="0783a-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0783a-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="0783a-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0783a-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0783a-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0783a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0783a-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0783a-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0783a-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="0783a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0783a-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="0783a-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="0783a-146">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="0783a-146">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="0783a-147">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0783a-147">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="0783a-148">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="0783a-148">**glIndex**</span></span>](glindexd.md)
</dt> </dl>

 

 





