---
title: función glEvalCoord2d (GL. h)
description: La función glEvalCoord2d evalúa las asignaciones bidimensionales habilitadas.
ms.assetid: 95963abc-841a-4154-92d5-5ae3e6de0f97
keywords:
- glEvalCoord2d (función) OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord2d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 036e2ee10d1ceac6df6a68a35c1da881d1d478b5
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "104566368"
---
# <a name="glevalcoord2d-function"></a><span data-ttu-id="40e73-104">glEvalCoord2d función)</span><span class="sxs-lookup"><span data-stu-id="40e73-104">glEvalCoord2d function</span></span>

<span data-ttu-id="40e73-105">La función **glEvalCoord2d** evalúa las asignaciones bidimensionales habilitadas.</span><span class="sxs-lookup"><span data-stu-id="40e73-105">The **glEvalCoord2d** function evaluates enabled two-dimensional maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="40e73-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="40e73-106">Syntax</span></span>


```C++
void WINAPI glEvalCoord2d(
   GLdouble u,
   GLdouble v
);
```



## <a name="parameters"></a><span data-ttu-id="40e73-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="40e73-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40e73-108">*u*</span><span class="sxs-lookup"><span data-stu-id="40e73-108">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="40e73-109">Un valor que es la coordenada del dominio *u* a la función base definida en una función [**glMap2**](glmap2.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="40e73-109">A value that is the domain coordinate *u* to the basis function defined in a previous [**glMap2**](glmap2.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="40e73-110">*v*</span><span class="sxs-lookup"><span data-stu-id="40e73-110">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="40e73-111">Un valor que es la coordenada de dominio *v* a la función de base definida en una función [**glMap2**](glmap2.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="40e73-111">A value that is the domain coordinate *v* to the basis function defined in a previous [**glMap2**](glmap2.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40e73-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="40e73-112">Return value</span></span>

<span data-ttu-id="40e73-113">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="40e73-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="40e73-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="40e73-114">Remarks</span></span>

<span data-ttu-id="40e73-115">La función **glEvalCoord2d** evalúa las asignaciones bidimensionales habilitadas con dos valores de dominio, *u* y *v*.</span><span class="sxs-lookup"><span data-stu-id="40e73-115">The **glEvalCoord2d** function evaluates enabled two-dimensional maps using two domain values, *u* and *v*.</span></span> <span data-ttu-id="40e73-116">Definir asignaciones con [**glMap1**](glmap1.md) y [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="40e73-116">Define maps with [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span> <span data-ttu-id="40e73-117">Habilitarlas o deshabilitarlas con [**glEnable**](glenable.md) y [**glDisable**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="40e73-117">Enable or disable them with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="40e73-118">Cuando se emite una de las funciones **glEvalCoord** , se evalúan todas las asignaciones habilitadas actualmente de la dimensión indicada.</span><span class="sxs-lookup"><span data-stu-id="40e73-118">When one of the **glEvalCoord** functions is issued, all currently enabled maps of the indicated dimension are evaluated.</span></span> <span data-ttu-id="40e73-119">A continuación, para cada asignación habilitada, es como si la función de OpenGL correspondiente se hubiera emitido con el valor calculado.</span><span class="sxs-lookup"><span data-stu-id="40e73-119">Then, for each enabled map, it is as if the corresponding OpenGL function were issued with the computed value.</span></span> <span data-ttu-id="40e73-120">Es decir, si \_ \_ se habilita GL MAP1 index o GL \_ MAP2 ( \_ index, se simula una función [**glIndex**](glindex-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="40e73-120">That is, if GL\_MAP1\_INDEX or GL\_MAP2\_INDEX is enabled, a [**glIndex**](glindex-functions.md) function is simulated.</span></span> <span data-ttu-id="40e73-121">Si GL \_ MAP1 \_ color \_ 4 o GL \_ MAP2 ( \_ color \_ 4 está habilitado, se simula una función **glcolor** .</span><span class="sxs-lookup"><span data-stu-id="40e73-121">If GL\_MAP1\_COLOR\_4 or GL\_MAP2\_COLOR\_4 is enabled, a **glcolor** function is simulated.</span></span> <span data-ttu-id="40e73-122">Si GL \_ MAP1 \_ normal o GL \_ MAP2 ( \_ normal está habilitado, se genera un vector normal, y si alguno de los MAP1 de contabilidad de la textura de GL \_ \_ \_ \_ 1, GL MAP1 Texture 4, GL MAP1 Texture de la textura 3, GL \_ \_ \_ \_ \_ \_ \_ \_ \_ MAP1 \_ Texture \_ \_ 4, GL \_ MAP2 ( \_ Texture \_ 4, \_ GL \_ MAP2 ( \_ Texture \_ coordenadas \_ 2, GL \_ MAP2 (Texture 4 y \_ \_ \_ GL \_ MAP2 ( \_ Texture \_ coordenadas \_ 4 está habilitado, se simula una función [**glTexCoord**](gltexcoord-functions.md) adecuada.</span><span class="sxs-lookup"><span data-stu-id="40e73-122">If GL\_MAP1\_NORMAL or GL\_MAP2\_NORMAL is enabled, a normal vector is produced, and if any of GL\_MAP1\_TEXTURE\_COORD\_1, GL\_MAP1\_TEXTURE\_COORD\_2, GL\_MAP1\_TEXTURE\_COORD\_3, GL\_MAP1\_TEXTURE\_COORD\_4, GL\_MAP2\_TEXTURE\_COORD\_1, GL\_MAP2\_TEXTURE\_COORD\_2, GL\_MAP2\_TEXTURE\_COORD\_3, and GL\_MAP2\_TEXTURE\_COORD\_4 is enabled, then an appropriate [**glTexCoord**](gltexcoord-functions.md) function is simulated.</span></span>

<span data-ttu-id="40e73-123">OpenGL usa los valores evaluados en lugar de los valores actuales de las evaluaciones que están habilitadas, y los valores actuales en caso contrario, para las coordenadas de color, índice de color, normal y textura.</span><span class="sxs-lookup"><span data-stu-id="40e73-123">OpenGL uses evaluated values instead of current values for those evaluations that are enabled, and current values otherwise, for color, color index, normal, and texture coordinates.</span></span> <span data-ttu-id="40e73-124">Sin embargo, los valores evaluados no actualizan los valores actuales.</span><span class="sxs-lookup"><span data-stu-id="40e73-124">However, the evaluated values do not update the current values.</span></span> <span data-ttu-id="40e73-125">Por lo tanto, si las funciones de [**glVertex**](glvertex-functions.md) se intercalan con las funciones **glEvalCoord** , las coordenadas de color, normal y de textura asociadas con las funciones **glVertex** no se ven afectadas por los valores generados por las funciones **GlEvalCoord** , sino solo por las funciones [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md)y [**glTexCoord**](gltexcoord-functions.md) más recientes.</span><span class="sxs-lookup"><span data-stu-id="40e73-125">Thus, if [**glVertex**](glvertex-functions.md) functions are interspersed with **glEvalCoord** functions, the color, normal, and texture coordinates associated with the **glVertex** functions are not affected by the values generated by the **glEvalCoord** functions, but only by the most recent [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md), and [**glTexCoord**](gltexcoord-functions.md) functions.</span></span>

<span data-ttu-id="40e73-126">Si la generación automática normal está habilitada, **glEvalCoord2d** llama a [**glEnable**](glenable.md) con el argumento GL \_ auto \_ normal para generar las normales de superficie analíticamente, independientemente del contenido o de la habilitación del \_ mapa normal de GL MAP2 ( \_ .</span><span class="sxs-lookup"><span data-stu-id="40e73-126">If automatic normal generation is enabled, **glEvalCoord2d** calls [**glEnable**](glenable.md) with argument GL\_AUTO\_NORMAL to generate surface normals analytically, regardless of the contents or enabling of the GL\_MAP2\_NORMAL map.</span></span> <span data-ttu-id="40e73-127">Let</span><span class="sxs-lookup"><span data-stu-id="40e73-127">Let</span></span>

![Ecuación que muestra un valor entre productos para un mapa m.](images/evlcrd01.png)

<span data-ttu-id="40e73-129">La **n** normal generada es</span><span class="sxs-lookup"><span data-stu-id="40e73-129">The generated normal **n** is</span></span>

![Ecuación que muestra el n normal generado para la asignación.](images/evlcrd02.png)

<span data-ttu-id="40e73-131">Las siguientes funciones recuperan información relacionada con la función **glEvalCoord2d** :</span><span class="sxs-lookup"><span data-stu-id="40e73-131">The following functions retrieve information related to the **glEvalCoord2d** function:</span></span>

<span data-ttu-id="40e73-132">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ Vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="40e73-132">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_3</span></span>

<span data-ttu-id="40e73-133">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ Vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="40e73-133">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_4</span></span>

<span data-ttu-id="40e73-134">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ index</span><span class="sxs-lookup"><span data-stu-id="40e73-134">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_INDEX</span></span>

<span data-ttu-id="40e73-135">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ color \_ 4</span><span class="sxs-lookup"><span data-stu-id="40e73-135">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_COLOR\_4</span></span>

<span data-ttu-id="40e73-136">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ normal</span><span class="sxs-lookup"><span data-stu-id="40e73-136">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_NORMAL</span></span>

<span data-ttu-id="40e73-137">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ Texture \_ coordenadas \_ 1</span><span class="sxs-lookup"><span data-stu-id="40e73-137">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="40e73-138">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ Texture \_ coordenadas \_ 2</span><span class="sxs-lookup"><span data-stu-id="40e73-138">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="40e73-139">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ Texture \_ coordenadas \_ 3</span><span class="sxs-lookup"><span data-stu-id="40e73-139">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="40e73-140">[**glIsEnabled**](glisenabled.md) con el argumento \_ GL \_ MAP1 \_ Texture \_ 4</span><span class="sxs-lookup"><span data-stu-id="40e73-140">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="40e73-141">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ Vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="40e73-141">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_3</span></span>

<span data-ttu-id="40e73-142">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ Vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="40e73-142">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_4</span></span>

<span data-ttu-id="40e73-143">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ index</span><span class="sxs-lookup"><span data-stu-id="40e73-143">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_INDEX</span></span>

<span data-ttu-id="40e73-144">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ color \_ 4</span><span class="sxs-lookup"><span data-stu-id="40e73-144">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_COLOR\_4</span></span>

<span data-ttu-id="40e73-145">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ normal</span><span class="sxs-lookup"><span data-stu-id="40e73-145">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_NORMAL</span></span>

<span data-ttu-id="40e73-146">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ Texture \_ coordenadas \_ 1</span><span class="sxs-lookup"><span data-stu-id="40e73-146">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="40e73-147">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ Texture \_ coordenadas \_ 2</span><span class="sxs-lookup"><span data-stu-id="40e73-147">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="40e73-148">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ Texture \_ coordenadas \_ 3</span><span class="sxs-lookup"><span data-stu-id="40e73-148">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="40e73-149">[**glIsEnabled**](glisenabled.md) con el argumento \_ GL \_ MAP2 ( \_ Texture \_ 4</span><span class="sxs-lookup"><span data-stu-id="40e73-149">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="40e73-150">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ auto \_ normal</span><span class="sxs-lookup"><span data-stu-id="40e73-150">[**glIsEnabled**](glisenabled.md) with argument GL\_AUTO\_NORMAL</span></span>

## <a name="requirements"></a><span data-ttu-id="40e73-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40e73-151">Requirements</span></span>



| <span data-ttu-id="40e73-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="40e73-152">Requirement</span></span> | <span data-ttu-id="40e73-153">Value</span><span class="sxs-lookup"><span data-stu-id="40e73-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40e73-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40e73-154">Minimum supported client</span></span><br/> | <span data-ttu-id="40e73-155">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="40e73-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="40e73-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40e73-156">Minimum supported server</span></span><br/> | <span data-ttu-id="40e73-157">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="40e73-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="40e73-158">Encabezado</span><span class="sxs-lookup"><span data-stu-id="40e73-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="40e73-159"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="40e73-159"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="40e73-160">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="40e73-160">Library</span></span><br/>                  | <dl> <span data-ttu-id="40e73-161"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="40e73-161"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="40e73-162">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="40e73-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40e73-163"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40e73-163"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40e73-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="40e73-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40e73-165">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="40e73-165">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="40e73-166">**glColor**</span><span class="sxs-lookup"><span data-stu-id="40e73-166">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="40e73-167">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="40e73-167">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="40e73-168">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="40e73-168">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="40e73-169">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="40e73-169">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="40e73-170">**glEvalMesh**</span><span class="sxs-lookup"><span data-stu-id="40e73-170">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="40e73-171">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="40e73-171">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="40e73-172">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="40e73-172">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="40e73-173">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="40e73-173">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="40e73-174">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="40e73-174">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="40e73-175">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="40e73-175">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="40e73-176">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="40e73-176">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="40e73-177">**glMapGrid**</span><span class="sxs-lookup"><span data-stu-id="40e73-177">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> <dt>

[<span data-ttu-id="40e73-178">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="40e73-178">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="40e73-179">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="40e73-179">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="40e73-180">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="40e73-180">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





