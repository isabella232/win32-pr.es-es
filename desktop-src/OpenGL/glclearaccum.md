---
title: función glClearAccum (GL. h)
description: La función glClearAccum especifica los valores claros para el búfer de acumulación.
ms.assetid: 77d8f340-be47-43f4-96fc-31025a4c8b4e
keywords:
- glClearAccum (función) OpenGL
topic_type:
- apiref
api_name:
- glClearAccum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3098e87a47509b8c05035171a8f31e57d8618424
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150435"
---
# <a name="glclearaccum-function"></a><span data-ttu-id="2cf28-104">glClearAccum función)</span><span class="sxs-lookup"><span data-stu-id="2cf28-104">glClearAccum function</span></span>

<span data-ttu-id="2cf28-105">La función **glClearAccum** especifica los valores claros para el búfer de acumulación.</span><span class="sxs-lookup"><span data-stu-id="2cf28-105">The **glClearAccum** function specifies the clear values for the accumulation buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cf28-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2cf28-106">Syntax</span></span>


```C++
void WINAPI glClearAccum(
   GLfloat red,
   GLfloat green,
   GLfloat blue,
   GLfloat alpha
);
```



## <a name="parameters"></a><span data-ttu-id="2cf28-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2cf28-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cf28-108">*alerta*</span><span class="sxs-lookup"><span data-stu-id="2cf28-108">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="2cf28-109">El valor rojo que se utiliza cuando se borra el búfer de acumulación.</span><span class="sxs-lookup"><span data-stu-id="2cf28-109">The red value used when the accumulation buffer is cleared.</span></span> <span data-ttu-id="2cf28-110">El valor predeterminado es cero.</span><span class="sxs-lookup"><span data-stu-id="2cf28-110">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="2cf28-111">*verde*</span><span class="sxs-lookup"><span data-stu-id="2cf28-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="2cf28-112">El valor verde que se utiliza cuando se borra el búfer de acumulación.</span><span class="sxs-lookup"><span data-stu-id="2cf28-112">The green value used when the accumulation buffer is cleared.</span></span> <span data-ttu-id="2cf28-113">El valor predeterminado es cero.</span><span class="sxs-lookup"><span data-stu-id="2cf28-113">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="2cf28-114">*azul*</span><span class="sxs-lookup"><span data-stu-id="2cf28-114">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="2cf28-115">El valor azul que se utiliza cuando se borra el búfer de acumulación.</span><span class="sxs-lookup"><span data-stu-id="2cf28-115">The blue value used when the accumulation buffer is cleared.</span></span> <span data-ttu-id="2cf28-116">El valor predeterminado es cero.</span><span class="sxs-lookup"><span data-stu-id="2cf28-116">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="2cf28-117">*alpha*</span><span class="sxs-lookup"><span data-stu-id="2cf28-117">*alpha*</span></span> 
</dt> <dd>

<span data-ttu-id="2cf28-118">Valor alfa que se utiliza cuando se borra el búfer de acumulación.</span><span class="sxs-lookup"><span data-stu-id="2cf28-118">The alpha value used when the accumulation buffer is cleared.</span></span> <span data-ttu-id="2cf28-119">El valor predeterminado es cero.</span><span class="sxs-lookup"><span data-stu-id="2cf28-119">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cf28-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2cf28-120">Return value</span></span>

<span data-ttu-id="2cf28-121">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2cf28-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2cf28-122">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="2cf28-122">Error codes</span></span>

<span data-ttu-id="2cf28-123">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="2cf28-123">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="2cf28-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="2cf28-124">Name</span></span>                                                                                                  | <span data-ttu-id="2cf28-125">Significado</span><span class="sxs-lookup"><span data-stu-id="2cf28-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2cf28-126"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2cf28-126"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="2cf28-127">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="2cf28-127">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2cf28-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2cf28-128">Remarks</span></span>

<span data-ttu-id="2cf28-129">La función **glClearAccum** especifica los valores rojo, verde, azul y alfa usados por [**glClear**](glclear.md) para borrar el búfer de acumulación.</span><span class="sxs-lookup"><span data-stu-id="2cf28-129">The **glClearAccum** function specifies the red, green, blue, and alpha values used by [**glClear**](glclear.md) to clear the accumulation buffer.</span></span>

<span data-ttu-id="2cf28-130">Los valores especificados por **glClearAccum** se fijan en el intervalo \[ 1, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="2cf28-130">Values specified by **glClearAccum** are clamped to the range \[1,1\].</span></span>

<span data-ttu-id="2cf28-131">La siguiente función recupera información relacionada con **glClearAccum**:</span><span class="sxs-lookup"><span data-stu-id="2cf28-131">The following function retrieves information related to **glClearAccum**:</span></span>

<span data-ttu-id="2cf28-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ valor Clear acumulado de GL \_</span><span class="sxs-lookup"><span data-stu-id="2cf28-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ACCUM\_CLEAR\_VALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="2cf28-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cf28-133">Requirements</span></span>



| <span data-ttu-id="2cf28-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cf28-134">Requirement</span></span> | <span data-ttu-id="2cf28-135">Value</span><span class="sxs-lookup"><span data-stu-id="2cf28-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2cf28-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2cf28-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2cf28-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2cf28-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2cf28-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2cf28-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2cf28-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2cf28-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2cf28-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2cf28-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cf28-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cf28-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="2cf28-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2cf28-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="2cf28-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2cf28-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2cf28-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2cf28-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cf28-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cf28-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cf28-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="2cf28-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cf28-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="2cf28-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="2cf28-148">**glClear**</span><span class="sxs-lookup"><span data-stu-id="2cf28-148">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="2cf28-149">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="2cf28-149">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="2cf28-150">**glGet**</span><span class="sxs-lookup"><span data-stu-id="2cf28-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





