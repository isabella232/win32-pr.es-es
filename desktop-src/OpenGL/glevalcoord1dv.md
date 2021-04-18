---
title: función glEvalCoord1dv (GL. h)
description: La función glEvalCoord1dv evalúa las asignaciones unidimensionales habilitadas.
ms.assetid: 6f966141-d4e6-4b54-b465-3ced33b57caf
keywords:
- glEvalCoord1dv (función) OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord1dv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018c984c74ed6fa0d7224e7e0520c023e8b6bdf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666034"
---
# <a name="glevalcoord1dv-function"></a><span data-ttu-id="f5e5d-104">glEvalCoord1dv función)</span><span class="sxs-lookup"><span data-stu-id="f5e5d-104">glEvalCoord1dv function</span></span>

<span data-ttu-id="f5e5d-105">La función [**glEvalCoord1dv**](glevalcoord1d.md) evalúa las asignaciones unidimensionales habilitadas.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-105">The [**glEvalCoord1dv**](glevalcoord1d.md) function evaluates enabled one-dimensional maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5e5d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5e5d-106">Syntax</span></span>


```C++
void WINAPI glEvalCoord1dv(
   const GLdouble *u
);
```



## <a name="parameters"></a><span data-ttu-id="f5e5d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f5e5d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5e5d-108">*u*</span><span class="sxs-lookup"><span data-stu-id="f5e5d-108">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="f5e5d-109">Puntero a una matriz que contiene la coordenada del dominio *u*.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-109">A pointer to an array containing the domain coordinate *u*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5e5d-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f5e5d-110">Return value</span></span>

<span data-ttu-id="f5e5d-111">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5e5d-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5e5d-112">Remarks</span></span>

<span data-ttu-id="f5e5d-113">La función **glEvalCoord1dv** evalúa las asignaciones unidimensionales habilitadas en el argumento *u*.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-113">The **glEvalCoord1dv** function evaluates enabled one-dimensional maps at argument *u*.</span></span> <span data-ttu-id="f5e5d-114">Definir asignaciones con [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="f5e5d-114">Define maps with [**glMap1**](glmap1.md).</span></span> <span data-ttu-id="f5e5d-115">Habilitarlas o deshabilitarlas con [**glEnable**](glenable.md) y [**glDisable**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="f5e5d-115">Enable or disable them with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="f5e5d-116">Cuando se emite una de las funciones **glEvalCoord** , se evalúan todas las asignaciones habilitadas actualmente de la dimensión indicada.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-116">When one of the **glEvalCoord** functions is issued, all currently enabled maps of the indicated dimension are evaluated.</span></span> <span data-ttu-id="f5e5d-117">A continuación, para cada asignación habilitada, es como si la función de OpenGL correspondiente se hubiera emitido con el valor calculado.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-117">Then, for each enabled map, it is as if the corresponding OpenGL function were issued with the computed value.</span></span> <span data-ttu-id="f5e5d-118">Es decir, si \_ \_ se habilita GL MAP1 index o GL \_ MAP2 ( \_ index, se simula una función [**glIndex**](glindex-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="f5e5d-118">That is, if GL\_MAP1\_INDEX or GL\_MAP2\_INDEX is enabled, a [**glIndex**](glindex-functions.md) function is simulated.</span></span> <span data-ttu-id="f5e5d-119">Si GL \_ MAP1 \_ color \_ 4 o GL \_ MAP2 ( \_ color \_ 4 está habilitado, se simula una función **glcolor** .</span><span class="sxs-lookup"><span data-stu-id="f5e5d-119">If GL\_MAP1\_COLOR\_4 or GL\_MAP2\_COLOR\_4 is enabled, a **glcolor** function is simulated.</span></span> <span data-ttu-id="f5e5d-120">Si GL \_ MAP1 \_ normal o GL \_ MAP2 ( \_ normal está habilitado, se genera un vector normal, y si alguno de los MAP1 de contabilidad de la textura de GL \_ \_ \_ \_ 1, GL MAP1 Texture 4, GL MAP1 Texture de la textura 3, GL \_ \_ \_ \_ \_ \_ \_ \_ \_ MAP1 \_ Texture \_ \_ 4, GL \_ MAP2 ( \_ Texture \_ 4, \_ GL \_ MAP2 ( \_ Texture \_ coordenadas \_ 2, GL \_ MAP2 (Texture 4 y \_ \_ \_ GL \_ MAP2 ( \_ Texture \_ coordenadas \_ 4 está habilitado, se simula una función [**glTexCoord**](gltexcoord-functions.md) adecuada.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-120">If GL\_MAP1\_NORMAL or GL\_MAP2\_NORMAL is enabled, a normal vector is produced, and if any of GL\_MAP1\_TEXTURE\_COORD\_1, GL\_MAP1\_TEXTURE\_COORD\_2, GL\_MAP1\_TEXTURE\_COORD\_3, GL\_MAP1\_TEXTURE\_COORD\_4, GL\_MAP2\_TEXTURE\_COORD\_1, GL\_MAP2\_TEXTURE\_COORD\_2, GL\_MAP2\_TEXTURE\_COORD\_3, and GL\_MAP2\_TEXTURE\_COORD\_4 is enabled, then an appropriate [**glTexCoord**](gltexcoord-functions.md) function is simulated.</span></span>

<span data-ttu-id="f5e5d-121">OpenGL usa los valores evaluados en lugar de los valores actuales de las evaluaciones que están habilitadas, y los valores actuales en caso contrario, para las coordenadas de color, índice de color, normal y textura.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-121">OpenGL uses evaluated values instead of current values for those evaluations that are enabled, and current values otherwise, for color, color index, normal, and texture coordinates.</span></span> <span data-ttu-id="f5e5d-122">Sin embargo, los valores evaluados no actualizan los valores actuales.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-122">However, the evaluated values do not update the current values.</span></span> <span data-ttu-id="f5e5d-123">Por lo tanto, si las funciones de [**glVertex**](glvertex-functions.md) se intercalan con las funciones **glEvalCoord** , las coordenadas de color, normal y de textura asociadas con las funciones **glVertex** no se ven afectadas por los valores generados por las funciones **GlEvalCoord** , sino solo por las funciones [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md)y [**glTexCoord**](gltexcoord-functions.md) más recientes.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-123">Thus, if [**glVertex**](glvertex-functions.md) functions are interspersed with **glEvalCoord** functions, the color, normal, and texture coordinates associated with the **glVertex** functions are not affected by the values generated by the **glEvalCoord** functions, but only by the most recent [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md), and [**glTexCoord**](gltexcoord-functions.md) functions.</span></span>

<span data-ttu-id="f5e5d-124">Las siguientes funciones recuperan información relacionada con la función **glEvalCoord1dv** :</span><span class="sxs-lookup"><span data-stu-id="f5e5d-124">The following functions retrieve information related to the **glEvalCoord1dv** function:</span></span>

<span data-ttu-id="f5e5d-125">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ Vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="f5e5d-125">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_3</span></span>

<span data-ttu-id="f5e5d-126">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ Vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="f5e5d-126">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_4</span></span>

<span data-ttu-id="f5e5d-127">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ index</span><span class="sxs-lookup"><span data-stu-id="f5e5d-127">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_INDEX</span></span>

<span data-ttu-id="f5e5d-128">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ color \_ 4</span><span class="sxs-lookup"><span data-stu-id="f5e5d-128">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_COLOR\_4</span></span>

<span data-ttu-id="f5e5d-129">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ normal</span><span class="sxs-lookup"><span data-stu-id="f5e5d-129">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_NORMAL</span></span>

<span data-ttu-id="f5e5d-130">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ Texture \_ coordenadas \_ 1</span><span class="sxs-lookup"><span data-stu-id="f5e5d-130">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="f5e5d-131">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ Texture \_ coordenadas \_ 2</span><span class="sxs-lookup"><span data-stu-id="f5e5d-131">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="f5e5d-132">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ Texture \_ coordenadas \_ 3</span><span class="sxs-lookup"><span data-stu-id="f5e5d-132">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="f5e5d-133">[**glIsEnabled**](glisenabled.md) con el argumento \_ GL \_ MAP1 \_ Texture \_ 4</span><span class="sxs-lookup"><span data-stu-id="f5e5d-133">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="f5e5d-134">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ Vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="f5e5d-134">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_3</span></span>

<span data-ttu-id="f5e5d-135">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ Vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="f5e5d-135">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_4</span></span>

<span data-ttu-id="f5e5d-136">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ index</span><span class="sxs-lookup"><span data-stu-id="f5e5d-136">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_INDEX</span></span>

<span data-ttu-id="f5e5d-137">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ color \_ 4</span><span class="sxs-lookup"><span data-stu-id="f5e5d-137">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_COLOR\_4</span></span>

<span data-ttu-id="f5e5d-138">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ normal</span><span class="sxs-lookup"><span data-stu-id="f5e5d-138">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_NORMAL</span></span>

<span data-ttu-id="f5e5d-139">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ Texture \_ coordenadas \_ 1</span><span class="sxs-lookup"><span data-stu-id="f5e5d-139">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="f5e5d-140">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ Texture \_ coordenadas \_ 2</span><span class="sxs-lookup"><span data-stu-id="f5e5d-140">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="f5e5d-141">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ Texture \_ coordenadas \_ 3</span><span class="sxs-lookup"><span data-stu-id="f5e5d-141">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="f5e5d-142">[**glIsEnabled**](glisenabled.md) con el argumento \_ GL \_ MAP2 ( \_ Texture \_ 4</span><span class="sxs-lookup"><span data-stu-id="f5e5d-142">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="f5e5d-143">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ auto \_ normal</span><span class="sxs-lookup"><span data-stu-id="f5e5d-143">[**glIsEnabled**](glisenabled.md) with argument GL\_AUTO\_NORMAL</span></span>

## <a name="requirements"></a><span data-ttu-id="f5e5d-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5e5d-144">Requirements</span></span>



| <span data-ttu-id="f5e5d-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5e5d-145">Requirement</span></span> | <span data-ttu-id="f5e5d-146">Value</span><span class="sxs-lookup"><span data-stu-id="f5e5d-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5e5d-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5e5d-147">Minimum supported client</span></span><br/> | <span data-ttu-id="f5e5d-148">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f5e5d-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f5e5d-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5e5d-149">Minimum supported server</span></span><br/> | <span data-ttu-id="f5e5d-150">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f5e5d-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f5e5d-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5e5d-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5e5d-152"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5e5d-152"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f5e5d-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f5e5d-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="f5e5d-154"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5e5d-154"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f5e5d-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f5e5d-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5e5d-156"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5e5d-156"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5e5d-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5e5d-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5e5d-158">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f5e5d-158">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f5e5d-159">**glColor**</span><span class="sxs-lookup"><span data-stu-id="f5e5d-159">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="f5e5d-160">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="f5e5d-160">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="f5e5d-161">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="f5e5d-161">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="f5e5d-162">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="f5e5d-162">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f5e5d-163">**glEvalMesh**</span><span class="sxs-lookup"><span data-stu-id="f5e5d-163">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="f5e5d-164">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="f5e5d-164">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="f5e5d-165">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="f5e5d-165">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="f5e5d-166">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="f5e5d-166">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="f5e5d-167">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="f5e5d-167">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="f5e5d-168">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="f5e5d-168">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="f5e5d-169">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="f5e5d-169">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="f5e5d-170">**glMapGrid**</span><span class="sxs-lookup"><span data-stu-id="f5e5d-170">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> <dt>

[<span data-ttu-id="f5e5d-171">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="f5e5d-171">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="f5e5d-172">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="f5e5d-172">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="f5e5d-173">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="f5e5d-173">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





