---
title: función glRotatef (GL. h)
description: La función glRotatef multiplica la matriz actual por una matriz de rotación.
ms.assetid: 8216a125-de8c-44e5-afb3-3d4e5ffc600d
keywords:
- glRotatef (función) OpenGL
topic_type:
- apiref
api_name:
- glRotatef
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 953b8ffc5f89e5a4cf9901e4cb5fb5afb4c8dfdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493222"
---
# <a name="glrotatef-function"></a><span data-ttu-id="37435-104">glRotatef función)</span><span class="sxs-lookup"><span data-stu-id="37435-104">glRotatef function</span></span>

<span data-ttu-id="37435-105">La función **glRotatef** multiplica la matriz actual por una matriz de rotación.</span><span class="sxs-lookup"><span data-stu-id="37435-105">The **glRotatef** function multiplies the current matrix by a rotation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="37435-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37435-106">Syntax</span></span>


```C++
void WINAPI glRotatef(
   GLfloat angle,
   GLfloat x,
   GLfloat y,
   GLfloat z
);
```



## <a name="parameters"></a><span data-ttu-id="37435-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37435-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37435-108">*angle*</span><span class="sxs-lookup"><span data-stu-id="37435-108">*angle*</span></span> 
</dt> <dd>

<span data-ttu-id="37435-109">Ángulo de rotación, en grados.</span><span class="sxs-lookup"><span data-stu-id="37435-109">The angle of rotation, in degrees.</span></span>

</dd> <dt>

<span data-ttu-id="37435-110">*x*</span><span class="sxs-lookup"><span data-stu-id="37435-110">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="37435-111">Coordenada *x* de un vector.</span><span class="sxs-lookup"><span data-stu-id="37435-111">The *x* coordinate of a vector.</span></span>

</dd> <dt>

<span data-ttu-id="37435-112">*y*</span><span class="sxs-lookup"><span data-stu-id="37435-112">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="37435-113">Coordenada *y* de un vector.</span><span class="sxs-lookup"><span data-stu-id="37435-113">The *y* coordinate of a vector.</span></span>

</dd> <dt>

<span data-ttu-id="37435-114">*z*</span><span class="sxs-lookup"><span data-stu-id="37435-114">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="37435-115">Coordenada *z* de un vector.</span><span class="sxs-lookup"><span data-stu-id="37435-115">The *z* coordinate of a vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37435-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37435-116">Return value</span></span>

<span data-ttu-id="37435-117">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="37435-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="37435-118">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="37435-118">Error codes</span></span>

<span data-ttu-id="37435-119">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="37435-119">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="37435-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="37435-120">Name</span></span>                                                                                                  | <span data-ttu-id="37435-121">Significado</span><span class="sxs-lookup"><span data-stu-id="37435-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="37435-122"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="37435-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="37435-123">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="37435-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="37435-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="37435-124">Remarks</span></span>

<span data-ttu-id="37435-125">La función **glRotatef** calcula una matriz que realiza un giro en sentido contrario de los grados *angulares* del vector desde el origen hasta el punto (*x*, *y*, *z*).</span><span class="sxs-lookup"><span data-stu-id="37435-125">The **glRotatef** function computes a matrix that performs a counterclockwise rotation of *angle* degrees about the vector from the origin through the point (*x*, *y*, *z*).</span></span>

<span data-ttu-id="37435-126">La matriz actual (vea [**glMatrixMode**](glmatrixmode.md)) se multiplica por esta matriz de rotación, donde el producto reemplaza la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="37435-126">The current matrix (see [**glMatrixMode**](glmatrixmode.md)) is multiplied by this rotation matrix, with the product replacing the current matrix.</span></span> <span data-ttu-id="37435-127">Es decir, si M es la matriz actual y R es la matriz de traslación, M se reemplaza por M R.</span><span class="sxs-lookup"><span data-stu-id="37435-127">That is, if M is the current matrix and R is the translation matrix, then M is replaced with M   R.</span></span>

<span data-ttu-id="37435-128">Si el modo de matriz es \_ MODELVIEW de GL o \_ proyección de contabilidad, se giran todos los objetos dibujados después de **glRotatef** .</span><span class="sxs-lookup"><span data-stu-id="37435-128">If the matrix mode is either GL\_MODELVIEW or GL\_PROJECTION, all objects drawn after **glRotatef** is called are rotated.</span></span> <span data-ttu-id="37435-129">Use [**glPushMatrix**](glpushmatrix.md) y [**glPopMatrix**](glpopmatrix.md) para guardar y restaurar el sistema de coordenadas sin girar.</span><span class="sxs-lookup"><span data-stu-id="37435-129">Use [**glPushMatrix**](glpushmatrix.md) and [**glPopMatrix**](glpopmatrix.md) to save and restore the unrotated coordinate system.</span></span>

<span data-ttu-id="37435-130">Las siguientes funciones recuperan información relacionada con **glRotatef**:</span><span class="sxs-lookup"><span data-stu-id="37435-130">The following functions retrieve information related to **glRotatef**:</span></span>

<span data-ttu-id="37435-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de representación de contabilidad de argumentos \_</span><span class="sxs-lookup"><span data-stu-id="37435-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

<span data-ttu-id="37435-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de matriz de contabilidad de argumentos \_</span><span class="sxs-lookup"><span data-stu-id="37435-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="37435-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ MODELVIEW \_ matriz de contabilidad</span><span class="sxs-lookup"><span data-stu-id="37435-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="37435-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ matriz de proyección de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="37435-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="37435-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ matriz de textura de GL \_</span><span class="sxs-lookup"><span data-stu-id="37435-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="37435-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37435-136">Requirements</span></span>



| <span data-ttu-id="37435-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="37435-137">Requirement</span></span> | <span data-ttu-id="37435-138">Value</span><span class="sxs-lookup"><span data-stu-id="37435-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37435-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37435-139">Minimum supported client</span></span><br/> | <span data-ttu-id="37435-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="37435-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="37435-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37435-141">Minimum supported server</span></span><br/> | <span data-ttu-id="37435-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="37435-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="37435-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37435-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="37435-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="37435-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="37435-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="37435-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="37435-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="37435-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="37435-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="37435-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37435-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37435-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37435-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="37435-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37435-150">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="37435-150">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="37435-151">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="37435-151">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="37435-152">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="37435-152">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="37435-153">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="37435-153">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="37435-154">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="37435-154">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="37435-155">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="37435-155">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="37435-156">**glScale**</span><span class="sxs-lookup"><span data-stu-id="37435-156">**glScale**</span></span>](glscale.md)
</dt> <dt>

[<span data-ttu-id="37435-157">**glTranslate**</span><span class="sxs-lookup"><span data-stu-id="37435-157">**glTranslate**</span></span>](gltranslate.md)
</dt> </dl>

 

 





