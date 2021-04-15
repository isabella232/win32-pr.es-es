---
title: función glEnd (GL. h)
description: Las funciones glBegin y glend delimitan los vértices de un primitivo o un grupo de primitivos similares. | función glEnd (GL. h)
ms.assetid: 040f8573-683c-4a8a-ae51-66abb0541ac4
keywords:
- glEnd (función) OpenGL
topic_type:
- apiref
api_name:
- glEnd
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9bb41395b3ed2e38a64094506e07e2a69ad1d52
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105670135"
---
# <a name="glend-function"></a><span data-ttu-id="8831b-105">glEnd función)</span><span class="sxs-lookup"><span data-stu-id="8831b-105">glEnd function</span></span>

<span data-ttu-id="8831b-106">Las funciones [**glBegin**](glbegin.md) y **glend** delimitan los vértices de un primitivo o un grupo de primitivos similares.</span><span class="sxs-lookup"><span data-stu-id="8831b-106">The [**glBegin**](glbegin.md) and **glend** functions delimit the vertices of a primitive or a group of like primitives.</span></span>

## <a name="syntax"></a><span data-ttu-id="8831b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8831b-107">Syntax</span></span>


```C++
void WINAPI glEnd(void);
```



## <a name="parameters"></a><span data-ttu-id="8831b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8831b-108">Parameters</span></span>

<span data-ttu-id="8831b-109">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="8831b-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8831b-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8831b-110">Return value</span></span>

<span data-ttu-id="8831b-111">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8831b-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8831b-112">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="8831b-112">Error codes</span></span>

<span data-ttu-id="8831b-113">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="8831b-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="8831b-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="8831b-114">Name</span></span>                                                                                                  | <span data-ttu-id="8831b-115">Significado</span><span class="sxs-lookup"><span data-stu-id="8831b-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8831b-116"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8831b-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="8831b-117">Se llamó a una función que no sea **glVertex**, **glColor**, **glIndex**, **glNormal**, **glTexCoord**, **glEvalCoord**, **GlEvalPoint**, **glMaterial**, **glEdgeFlag**, **glCallList** o **glCallLists** entre **glBegin** y el **glEnd** correspondiente.</span><span class="sxs-lookup"><span data-stu-id="8831b-117">A function other than **glVertex**, **glColor**, **glIndex**, **glNormal**, **glTexCoord**, **glEvalCoord**, **glEvalPoint**, **glMaterial**, **glEdgeFlag**, **glCallList**, or **glCallLists** was called between **glBegin** and the corresponding **glEnd**.</span></span> <span data-ttu-id="8831b-118">Se llamó a la función **glEnd** antes de que se llamara al **glBegin** correspondiente, o bien se llamó a **glBegin** dentro de una secuencia **glBegin** / **glEnd** .</span><span class="sxs-lookup"><span data-stu-id="8831b-118">The function **glEnd** was called before the corresponding **glBegin** was called, or **glBegin** was called within a **glBegin**/**glEnd** sequence.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="8831b-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8831b-119">Remarks</span></span>

<span data-ttu-id="8831b-120">Las funciones [**glBegin**](glbegin.md) y **glend** delimitan los vértices que definen un primitivo o un grupo de primitivos similares.</span><span class="sxs-lookup"><span data-stu-id="8831b-120">The [**glBegin**](glbegin.md) and **glend** functions delimit the vertices that define a primitive or a group of like primitives.</span></span> <span data-ttu-id="8831b-121">La función **glBegin** acepta un solo argumento que especifica los diez primitivos que componen los vértices.</span><span class="sxs-lookup"><span data-stu-id="8831b-121">The **glBegin** function accepts a single argument that specifies which of ten primitives the vertices compose.</span></span> <span data-ttu-id="8831b-122">Tomando *n* como un recuento entero a partir de uno, y *n* como el número total de vértices especificado, las interpretaciones son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="8831b-122">Taking *n* as an integer count starting at one, and *N* as the total number of vertices specified, the interpretations are as follows:</span></span>

-   <span data-ttu-id="8831b-123">Solo se puede usar un subconjunto de funciones de OpenGL entre **glBegin** y **glEnd**.</span><span class="sxs-lookup"><span data-stu-id="8831b-123">You can use only a subset of OpenGL functions between **glBegin** and **glEnd**.</span></span> <span data-ttu-id="8831b-124">Las funciones que puede usar son:</span><span class="sxs-lookup"><span data-stu-id="8831b-124">The functions you can use are:</span></span>

    -   [<span data-ttu-id="8831b-125">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="8831b-125">**glVertex**</span></span>](glvertex-functions.md)
    -   [<span data-ttu-id="8831b-126">**glColor**</span><span class="sxs-lookup"><span data-stu-id="8831b-126">**glColor**</span></span>](glcolor-functions.md)
    -   [<span data-ttu-id="8831b-127">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="8831b-127">**glIndex**</span></span>](glindex-functions.md)
    -   [<span data-ttu-id="8831b-128">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="8831b-128">**glNormal**</span></span>](glnormal-functions.md)
    -   [<span data-ttu-id="8831b-129">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="8831b-129">**glTexCoord**</span></span>](gltexcoord-functions.md)
    -   [<span data-ttu-id="8831b-130">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="8831b-130">**glEvalCoord**</span></span>](glevalcoord-functions.md)
    -   [<span data-ttu-id="8831b-131">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="8831b-131">**glEvalPoint**</span></span>](glevalpoint.md)
    -   [<span data-ttu-id="8831b-132">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="8831b-132">**glMaterial**</span></span>](glmaterial-functions.md)
    -   [<span data-ttu-id="8831b-133">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="8831b-133">**glEdgeFlag**</span></span>](gledgeflag-functions.md)

    <span data-ttu-id="8831b-134">También puede usar [**glCallList**](glcalllist.md) o [**glCallLists**](glcalllists.md) para ejecutar listas de presentación que incluyen solo las funciones anteriores.</span><span class="sxs-lookup"><span data-stu-id="8831b-134">You can also use [**glCallList**](glcalllist.md) or [**glCallLists**](glcalllists.md) to execute display lists that include only the preceding functions.</span></span> <span data-ttu-id="8831b-135">Si se llama a cualquier otra función de OpenGL entre **glBegin** y **glEnd**, se establece la marca de error y se omite la función.</span><span class="sxs-lookup"><span data-stu-id="8831b-135">If any other OpenGL function is called between **glBegin** and **glEnd**, the error flag is set and the function is ignored.</span></span>

-   <span data-ttu-id="8831b-136">Independientemente del valor elegido para el *modo* en **glBegin**, no hay ningún límite en el número de vértices que puede definir entre **glBegin** y **glEnd**.</span><span class="sxs-lookup"><span data-stu-id="8831b-136">Regardless of the value chosen for *mode* in **glBegin**, there is no limit to the number of vertices you can define between **glBegin** and **glEnd**.</span></span> <span data-ttu-id="8831b-137">No se dibujan líneas, triángulos, quadrilaterals ni polígonos que se hayan especificado de una vez incompleta.</span><span class="sxs-lookup"><span data-stu-id="8831b-137">Lines, triangles, quadrilaterals, and polygons that are incompletely specified are not drawn.</span></span> <span data-ttu-id="8831b-138">Resultados de especificación incompletos cuando se proporcionan muy pocos vértices para especificar incluso un único primitivo o cuando se especifica un múltiplo incorrecto de vértices.</span><span class="sxs-lookup"><span data-stu-id="8831b-138">Incomplete specification results when either too few vertices are provided to specify even a single primitive or when an incorrect multiple of vertices is specified.</span></span> <span data-ttu-id="8831b-139">Se omite el primitivo incompleto; se dibujan los primitivos completos.</span><span class="sxs-lookup"><span data-stu-id="8831b-139">The incomplete primitive is ignored; the complete primitives are drawn.</span></span>
-   <span data-ttu-id="8831b-140">La especificación mínima de los vértices para cada primitiva es:</span><span class="sxs-lookup"><span data-stu-id="8831b-140">The minimum specification of vertices for each primitive is:</span></span> 

    | <span data-ttu-id="8831b-141">Número mínimo de vértices</span><span class="sxs-lookup"><span data-stu-id="8831b-141">Minimum number of vertices</span></span> | <span data-ttu-id="8831b-142">Tipo de primitivo</span><span class="sxs-lookup"><span data-stu-id="8831b-142">Type of primitive</span></span> |
    |----------------------------|-------------------|
    | <span data-ttu-id="8831b-143">1</span><span class="sxs-lookup"><span data-stu-id="8831b-143">1</span></span>                          | <span data-ttu-id="8831b-144">point</span><span class="sxs-lookup"><span data-stu-id="8831b-144">point</span></span>             |
    | <span data-ttu-id="8831b-145">2</span><span class="sxs-lookup"><span data-stu-id="8831b-145">2</span></span>                          | <span data-ttu-id="8831b-146">line</span><span class="sxs-lookup"><span data-stu-id="8831b-146">line</span></span>              |
    | <span data-ttu-id="8831b-147">3</span><span class="sxs-lookup"><span data-stu-id="8831b-147">3</span></span>                          | <span data-ttu-id="8831b-148">triangle</span><span class="sxs-lookup"><span data-stu-id="8831b-148">triangle</span></span>          |
    | <span data-ttu-id="8831b-149">4</span><span class="sxs-lookup"><span data-stu-id="8831b-149">4</span></span>                          | <span data-ttu-id="8831b-150">cuadrangular</span><span class="sxs-lookup"><span data-stu-id="8831b-150">quadrilateral</span></span>     |
    | <span data-ttu-id="8831b-151">3</span><span class="sxs-lookup"><span data-stu-id="8831b-151">3</span></span>                          | <span data-ttu-id="8831b-152">polygon</span><span class="sxs-lookup"><span data-stu-id="8831b-152">polygon</span></span>           |

    

     

-   <span data-ttu-id="8831b-153">Los modos que requieren un determinado múltiplo de vértices son \_ las líneas de libro de contabilidad (2), los \_ triángulos de contabilidad (3), los \_ cuatro cuádruples (4) y la \_ franja cuádruple de GL \_ (2).</span><span class="sxs-lookup"><span data-stu-id="8831b-153">Modes that require a certain multiple of vertices are GL\_LINES (2), GL\_TRIANGLES (3), GL\_QUADS (4), and GL\_QUAD\_STRIP (2).</span></span>

## <a name="requirements"></a><span data-ttu-id="8831b-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8831b-154">Requirements</span></span>



| <span data-ttu-id="8831b-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="8831b-155">Requirement</span></span> | <span data-ttu-id="8831b-156">Value</span><span class="sxs-lookup"><span data-stu-id="8831b-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8831b-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8831b-157">Minimum supported client</span></span><br/> | <span data-ttu-id="8831b-158">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8831b-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8831b-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8831b-159">Minimum supported server</span></span><br/> | <span data-ttu-id="8831b-160">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8831b-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8831b-161">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8831b-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="8831b-162"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8831b-162"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8831b-163">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8831b-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="8831b-164"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8831b-164"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8831b-165">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8831b-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8831b-166"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8831b-166"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8831b-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="8831b-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8831b-168">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="8831b-168">**glBegin**</span></span>](/windows/desktop/OpenGL/glbegin)
</dt> <dt>

[<span data-ttu-id="8831b-169">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="8831b-169">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="8831b-170">**glColor**</span><span class="sxs-lookup"><span data-stu-id="8831b-170">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="8831b-171">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="8831b-171">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="8831b-172">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="8831b-172">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="8831b-173">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="8831b-173">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="8831b-174">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="8831b-174">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="8831b-175">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="8831b-175">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="8831b-176">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="8831b-176">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="8831b-177">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="8831b-177">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="8831b-178">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="8831b-178">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

