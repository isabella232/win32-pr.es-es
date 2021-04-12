---
title: función glEvalCoord1f (GL. h)
description: La función glEvalCoord1f evalúa las asignaciones unidimensionales habilitadas.
ms.assetid: 520e2d31-b9c2-4b06-ab61-c2c7aa18448a
keywords:
- glEvalCoord1f (función) OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord1f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 135d1b7faebf155c6027b715c64573fbb9463868
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489730"
---
# <a name="glevalcoord1f-function"></a><span data-ttu-id="b22c0-104">glEvalCoord1f función)</span><span class="sxs-lookup"><span data-stu-id="b22c0-104">glEvalCoord1f function</span></span>

<span data-ttu-id="b22c0-105">La función **glEvalCoord1f** evalúa las asignaciones unidimensionales habilitadas.</span><span class="sxs-lookup"><span data-stu-id="b22c0-105">The **glEvalCoord1f** function evaluates enabled one-dimensional maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="b22c0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b22c0-106">Syntax</span></span>


```C++
void WINAPI glEvalCoord1f(
   GLfloat u
);
```



## <a name="parameters"></a><span data-ttu-id="b22c0-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b22c0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b22c0-108">*u*</span><span class="sxs-lookup"><span data-stu-id="b22c0-108">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="b22c0-109">Un valor que es la coordenada del dominio *u* a la función base definida en una función [**glMap1**](glmap1.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="b22c0-109">A value that is the domain coordinate *u* to the basis function defined in a previous [**glMap1**](glmap1.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b22c0-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b22c0-110">Return value</span></span>

<span data-ttu-id="b22c0-111">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b22c0-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b22c0-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b22c0-112">Remarks</span></span>

<span data-ttu-id="b22c0-113">La función **glEvalCoord1f** evalúa las asignaciones unidimensionales habilitadas en el argumento *u*.</span><span class="sxs-lookup"><span data-stu-id="b22c0-113">The **glEvalCoord1f** function evaluates enabled one-dimensional maps at argument *u*.</span></span> <span data-ttu-id="b22c0-114">Definir asignaciones con [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="b22c0-114">Define maps with [**glMap1**](glmap1.md).</span></span> <span data-ttu-id="b22c0-115">Habilitarlas o deshabilitarlas con [**glEnable**](glenable.md) y [**glDisable**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="b22c0-115">Enable or disable them with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="b22c0-116">Cuando se emite una de las funciones **glEvalCoord** , se evalúan todas las asignaciones habilitadas actualmente de la dimensión indicada.</span><span class="sxs-lookup"><span data-stu-id="b22c0-116">When one of the **glEvalCoord** functions is issued, all currently enabled maps of the indicated dimension are evaluated.</span></span> <span data-ttu-id="b22c0-117">A continuación, para cada asignación habilitada, es como si la función de OpenGL correspondiente se hubiera emitido con el valor calculado.</span><span class="sxs-lookup"><span data-stu-id="b22c0-117">Then, for each enabled map, it is as if the corresponding OpenGL function were issued with the computed value.</span></span> <span data-ttu-id="b22c0-118">Es decir, si \_ \_ se habilita GL MAP1 index o GL \_ MAP2 ( \_ index, se simula una función [**glIndex**](glindex-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="b22c0-118">That is, if GL\_MAP1\_INDEX or GL\_MAP2\_INDEX is enabled, a [**glIndex**](glindex-functions.md) function is simulated.</span></span> <span data-ttu-id="b22c0-119">Si GL \_ MAP1 \_ color \_ 4 o GL \_ MAP2 ( \_ color \_ 4 está habilitado, se simula una función **glcolor** .</span><span class="sxs-lookup"><span data-stu-id="b22c0-119">If GL\_MAP1\_COLOR\_4 or GL\_MAP2\_COLOR\_4 is enabled, a **glcolor** function is simulated.</span></span> <span data-ttu-id="b22c0-120">Si GL \_ MAP1 \_ normal o GL \_ MAP2 ( \_ normal está habilitado, se genera un vector normal, y si alguno de los MAP1 de contabilidad de la textura de GL \_ \_ \_ \_ 1, GL MAP1 Texture 4, GL MAP1 Texture de la textura 3, GL \_ \_ \_ \_ \_ \_ \_ \_ \_ MAP1 \_ Texture \_ \_ 4, GL \_ MAP2 ( \_ Texture \_ 4, \_ GL \_ MAP2 ( \_ Texture \_ coordenadas \_ 2, GL \_ MAP2 (Texture 4 y \_ \_ \_ GL \_ MAP2 ( \_ Texture \_ coordenadas \_ 4 está habilitado, se simula una función [**glTexCoord**](gltexcoord-functions.md) adecuada.</span><span class="sxs-lookup"><span data-stu-id="b22c0-120">If GL\_MAP1\_NORMAL or GL\_MAP2\_NORMAL is enabled, a normal vector is produced, and if any of GL\_MAP1\_TEXTURE\_COORD\_1, GL\_MAP1\_TEXTURE\_COORD\_2, GL\_MAP1\_TEXTURE\_COORD\_3, GL\_MAP1\_TEXTURE\_COORD\_4, GL\_MAP2\_TEXTURE\_COORD\_1, GL\_MAP2\_TEXTURE\_COORD\_2, GL\_MAP2\_TEXTURE\_COORD\_3, and GL\_MAP2\_TEXTURE\_COORD\_4 is enabled, then an appropriate [**glTexCoord**](gltexcoord-functions.md) function is simulated.</span></span>

<span data-ttu-id="b22c0-121">OpenGL usa los valores evaluados en lugar de los valores actuales de las evaluaciones que están habilitadas, y los valores actuales en caso contrario, para las coordenadas de color, índice de color, normal y textura.</span><span class="sxs-lookup"><span data-stu-id="b22c0-121">OpenGL uses evaluated values instead of current values for those evaluations that are enabled, and current values otherwise, for color, color index, normal, and texture coordinates.</span></span> <span data-ttu-id="b22c0-122">Sin embargo, los valores evaluados no actualizan los valores actuales.</span><span class="sxs-lookup"><span data-stu-id="b22c0-122">However, the evaluated values do not update the current values.</span></span> <span data-ttu-id="b22c0-123">Por lo tanto, si las funciones de [**glVertex**](glvertex-functions.md) se intercalan con las funciones **glEvalCoord** , las coordenadas de color, normal y de textura asociadas con las funciones **glVertex** no se ven afectadas por los valores generados por las funciones **GlEvalCoord** , sino solo por las funciones [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md)y [**glTexCoord**](gltexcoord-functions.md) más recientes.</span><span class="sxs-lookup"><span data-stu-id="b22c0-123">Thus, if [**glVertex**](glvertex-functions.md) functions are interspersed with **glEvalCoord** functions, the color, normal, and texture coordinates associated with the **glVertex** functions are not affected by the values generated by the **glEvalCoord** functions, but only by the most recent [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md), and [**glTexCoord**](gltexcoord-functions.md) functions.</span></span>

<span data-ttu-id="b22c0-124">Las siguientes funciones recuperan información relacionada con la función **glEvalCoord1f** :</span><span class="sxs-lookup"><span data-stu-id="b22c0-124">The following functions retrieve information related to the **glEvalCoord1f** function:</span></span>

<span data-ttu-id="b22c0-125">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ Vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="b22c0-125">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_3</span></span>

<span data-ttu-id="b22c0-126">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ Vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="b22c0-126">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_4</span></span>

<span data-ttu-id="b22c0-127">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ index</span><span class="sxs-lookup"><span data-stu-id="b22c0-127">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_INDEX</span></span>

<span data-ttu-id="b22c0-128">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ color \_ 4</span><span class="sxs-lookup"><span data-stu-id="b22c0-128">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_COLOR\_4</span></span>

<span data-ttu-id="b22c0-129">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ normal</span><span class="sxs-lookup"><span data-stu-id="b22c0-129">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_NORMAL</span></span>

<span data-ttu-id="b22c0-130">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ Texture \_ coordenadas \_ 1</span><span class="sxs-lookup"><span data-stu-id="b22c0-130">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="b22c0-131">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ Texture \_ coordenadas \_ 2</span><span class="sxs-lookup"><span data-stu-id="b22c0-131">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="b22c0-132">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ Texture \_ coordenadas \_ 3</span><span class="sxs-lookup"><span data-stu-id="b22c0-132">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="b22c0-133">[**glIsEnabled**](glisenabled.md) con el argumento \_ GL \_ MAP1 \_ Texture \_ 4</span><span class="sxs-lookup"><span data-stu-id="b22c0-133">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="b22c0-134">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ Vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="b22c0-134">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_3</span></span>

<span data-ttu-id="b22c0-135">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ Vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="b22c0-135">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_4</span></span>

<span data-ttu-id="b22c0-136">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ index</span><span class="sxs-lookup"><span data-stu-id="b22c0-136">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_INDEX</span></span>

<span data-ttu-id="b22c0-137">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ color \_ 4</span><span class="sxs-lookup"><span data-stu-id="b22c0-137">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_COLOR\_4</span></span>

<span data-ttu-id="b22c0-138">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ normal</span><span class="sxs-lookup"><span data-stu-id="b22c0-138">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_NORMAL</span></span>

<span data-ttu-id="b22c0-139">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ Texture \_ coordenadas \_ 1</span><span class="sxs-lookup"><span data-stu-id="b22c0-139">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="b22c0-140">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ Texture \_ coordenadas \_ 2</span><span class="sxs-lookup"><span data-stu-id="b22c0-140">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="b22c0-141">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ Texture \_ coordenadas \_ 3</span><span class="sxs-lookup"><span data-stu-id="b22c0-141">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="b22c0-142">[**glIsEnabled**](glisenabled.md) con el argumento \_ GL \_ MAP2 ( \_ Texture \_ 4</span><span class="sxs-lookup"><span data-stu-id="b22c0-142">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="b22c0-143">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ auto \_ normal</span><span class="sxs-lookup"><span data-stu-id="b22c0-143">[**glIsEnabled**](glisenabled.md) with argument GL\_AUTO\_NORMAL</span></span>

## <a name="requirements"></a><span data-ttu-id="b22c0-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b22c0-144">Requirements</span></span>



| <span data-ttu-id="b22c0-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="b22c0-145">Requirement</span></span> | <span data-ttu-id="b22c0-146">Value</span><span class="sxs-lookup"><span data-stu-id="b22c0-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b22c0-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b22c0-147">Minimum supported client</span></span><br/> | <span data-ttu-id="b22c0-148">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b22c0-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b22c0-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b22c0-149">Minimum supported server</span></span><br/> | <span data-ttu-id="b22c0-150">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b22c0-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b22c0-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b22c0-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="b22c0-152"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b22c0-152"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b22c0-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b22c0-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="b22c0-154"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b22c0-154"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b22c0-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b22c0-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b22c0-156"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b22c0-156"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b22c0-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="b22c0-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b22c0-158">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b22c0-158">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b22c0-159">**glColor**</span><span class="sxs-lookup"><span data-stu-id="b22c0-159">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="b22c0-160">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="b22c0-160">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="b22c0-161">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="b22c0-161">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="b22c0-162">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b22c0-162">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b22c0-163">**glEvalMesh**</span><span class="sxs-lookup"><span data-stu-id="b22c0-163">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="b22c0-164">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="b22c0-164">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="b22c0-165">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="b22c0-165">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="b22c0-166">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="b22c0-166">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="b22c0-167">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="b22c0-167">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="b22c0-168">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="b22c0-168">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="b22c0-169">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="b22c0-169">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="b22c0-170">**glMapGrid**</span><span class="sxs-lookup"><span data-stu-id="b22c0-170">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> <dt>

[<span data-ttu-id="b22c0-171">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="b22c0-171">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="b22c0-172">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="b22c0-172">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="b22c0-173">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="b22c0-173">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





