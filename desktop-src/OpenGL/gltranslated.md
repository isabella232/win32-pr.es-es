---
title: función glTranslated (GL. h)
description: La función glTranslated multiplica la matriz actual por una matriz de traslación.
ms.assetid: 9f066a92-ee78-44d1-b8f8-0eacde0e1a47
keywords:
- glTranslated (función) OpenGL
topic_type:
- apiref
api_name:
- glTranslated
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705c8dd0635294b066897db99c0770b5f6622c75
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105689612"
---
# <a name="gltranslated-function"></a><span data-ttu-id="350a1-104">glTranslated función)</span><span class="sxs-lookup"><span data-stu-id="350a1-104">glTranslated function</span></span>

<span data-ttu-id="350a1-105">La función **glTranslated** multiplica la matriz actual por una matriz de traslación.</span><span class="sxs-lookup"><span data-stu-id="350a1-105">The **glTranslated** function multiplies the current matrix by a translation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="350a1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="350a1-106">Syntax</span></span>


```C++
void WINAPI glTranslated(
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a><span data-ttu-id="350a1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="350a1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="350a1-108">*x*</span><span class="sxs-lookup"><span data-stu-id="350a1-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="350a1-109">Coordenada *x* de un vector de traslación.</span><span class="sxs-lookup"><span data-stu-id="350a1-109">The *x* coordinate of a translation vector.</span></span>

</dd> <dt>

<span data-ttu-id="350a1-110">*y*</span><span class="sxs-lookup"><span data-stu-id="350a1-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="350a1-111">Coordenada *y* de un vector de traslación.</span><span class="sxs-lookup"><span data-stu-id="350a1-111">The *y* coordinate of a translation vector.</span></span>

</dd> <dt>

<span data-ttu-id="350a1-112">*z*</span><span class="sxs-lookup"><span data-stu-id="350a1-112">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="350a1-113">Coordenada *z* de un vector de traslación.</span><span class="sxs-lookup"><span data-stu-id="350a1-113">The *z* coordinate of a translation vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="350a1-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="350a1-114">Return value</span></span>

<span data-ttu-id="350a1-115">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="350a1-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="350a1-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="350a1-116">Remarks</span></span>

<span data-ttu-id="350a1-117">La función **glTranslated** produce la traducción especificada por (*x*, *y*, *z*).</span><span class="sxs-lookup"><span data-stu-id="350a1-117">The **glTranslated** function produces the translation specified by (*x*, *y*, *z*).</span></span> <span data-ttu-id="350a1-118">El vector de conversión se usa para calcular una matriz de traslación 4x4:</span><span class="sxs-lookup"><span data-stu-id="350a1-118">The translation vector is used to compute a 4x4 translation matrix:</span></span>

![Diagrama que muestra la matriz de traslación 4x4 especificada por x, y, z.](images/trans01.png)

<span data-ttu-id="350a1-120">La matriz actual (vea [**glMatrixMode**](glmatrixmode.md)) se multiplica por esta matriz de traducción, con el producto que reemplaza la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="350a1-120">The current matrix (see [**glMatrixMode**](glmatrixmode.md)) is multiplied by this translation matrix, with the product replacing the current matrix.</span></span> <span data-ttu-id="350a1-121">Es decir, si M es la matriz actual y T es la matriz de traslación, M se reemplaza por M T.</span><span class="sxs-lookup"><span data-stu-id="350a1-121">That is, if M is the current matrix and T is the translation matrix, then M is replaced with M T.</span></span>

<span data-ttu-id="350a1-122">Si el modo de matriz es \_ MODELVIEW de GL o \_ proyección de contabilidad, se traducen todos los objetos dibujados después de **glTranslated** .</span><span class="sxs-lookup"><span data-stu-id="350a1-122">If the matrix mode is either GL\_MODELVIEW or GL\_PROJECTION, all objects drawn after **glTranslated** is called are translated.</span></span> <span data-ttu-id="350a1-123">Use [**glPushMatrix**](glpushmatrix.md) y **glPopMatrix** para guardar y restaurar el sistema de coordenadas sin traducir.</span><span class="sxs-lookup"><span data-stu-id="350a1-123">Use [**glPushMatrix**](glpushmatrix.md) and **glPopMatrix** to save and restore the untranslated coordinate system.</span></span>

<span data-ttu-id="350a1-124">Las siguientes funciones recuperan información relacionada con [**glTranslated**](gltranslate.md):</span><span class="sxs-lookup"><span data-stu-id="350a1-124">The following functions retrieve information related to [**glTranslated**](gltranslate.md):</span></span>

<span data-ttu-id="350a1-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de matriz de contabilidad de argumentos \_</span><span class="sxs-lookup"><span data-stu-id="350a1-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="350a1-126">**glGet** con el argumento \_ MODELVIEW \_ matriz de contabilidad</span><span class="sxs-lookup"><span data-stu-id="350a1-126">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="350a1-127">**glGet** con el argumento \_ matriz de proyección de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="350a1-127">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="350a1-128">**glGet** con el argumento \_ matriz de textura de GL \_</span><span class="sxs-lookup"><span data-stu-id="350a1-128">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="350a1-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="350a1-129">Requirements</span></span>



| <span data-ttu-id="350a1-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="350a1-130">Requirement</span></span> | <span data-ttu-id="350a1-131">Value</span><span class="sxs-lookup"><span data-stu-id="350a1-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="350a1-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="350a1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="350a1-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="350a1-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="350a1-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="350a1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="350a1-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="350a1-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="350a1-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="350a1-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="350a1-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="350a1-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="350a1-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="350a1-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="350a1-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="350a1-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="350a1-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="350a1-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="350a1-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="350a1-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="350a1-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="350a1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="350a1-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="350a1-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="350a1-144">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="350a1-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="350a1-145">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="350a1-145">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="350a1-146">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="350a1-146">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="350a1-147">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="350a1-147">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="350a1-148">**glRotate**</span><span class="sxs-lookup"><span data-stu-id="350a1-148">**glRotate**</span></span>](glrotate.md)
</dt> <dt>

[<span data-ttu-id="350a1-149">**glScale**</span><span class="sxs-lookup"><span data-stu-id="350a1-149">**glScale**</span></span>](glscale.md)
</dt> </dl>

 

 





