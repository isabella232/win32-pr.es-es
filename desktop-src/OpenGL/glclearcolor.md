---
title: función glClearColor (GL. h)
description: La función glClearColor especifica valores claros para los búferes de color.
ms.assetid: f938e3f4-9db3-4c24-97ae-531b6799224e
keywords:
- glClearColor (función) OpenGL
topic_type:
- apiref
api_name:
- glClearColor
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34005ce34900f5fee8a4c9b2f1b963b7fe4bb6d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802605"
---
# <a name="glclearcolor-function"></a><span data-ttu-id="121d5-104">glClearColor función)</span><span class="sxs-lookup"><span data-stu-id="121d5-104">glClearColor function</span></span>

<span data-ttu-id="121d5-105">La función **glClearColor** especifica valores claros para los búferes de color.</span><span class="sxs-lookup"><span data-stu-id="121d5-105">The **glClearColor** function specifies clear values for the color buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="121d5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="121d5-106">Syntax</span></span>


```C++
void WINAPI glClearColor(
   GLclampf red,
   GLclampf green,
   GLclampf blue,
   GLclampf alpha
);
```



## <a name="parameters"></a><span data-ttu-id="121d5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="121d5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="121d5-108">*alerta*</span><span class="sxs-lookup"><span data-stu-id="121d5-108">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="121d5-109">Valor rojo que [**glClear**](glclear.md) usa para borrar los búferes de color.</span><span class="sxs-lookup"><span data-stu-id="121d5-109">The red value that [**glClear**](glclear.md) uses to clear the color buffers.</span></span> <span data-ttu-id="121d5-110">El valor predeterminado es cero.</span><span class="sxs-lookup"><span data-stu-id="121d5-110">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="121d5-111">*verde*</span><span class="sxs-lookup"><span data-stu-id="121d5-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="121d5-112">Valor verde que [**glClear**](glclear.md) usa para borrar los búferes de color.</span><span class="sxs-lookup"><span data-stu-id="121d5-112">The green value that [**glClear**](glclear.md) uses to clear the color buffers.</span></span> <span data-ttu-id="121d5-113">El valor predeterminado es cero.</span><span class="sxs-lookup"><span data-stu-id="121d5-113">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="121d5-114">*azul*</span><span class="sxs-lookup"><span data-stu-id="121d5-114">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="121d5-115">Valor azul que [**glClear**](glclear.md) usa para borrar los búferes de color.</span><span class="sxs-lookup"><span data-stu-id="121d5-115">The blue value that [**glClear**](glclear.md) uses to clear the color buffers.</span></span> <span data-ttu-id="121d5-116">El valor predeterminado es cero.</span><span class="sxs-lookup"><span data-stu-id="121d5-116">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="121d5-117">*alpha*</span><span class="sxs-lookup"><span data-stu-id="121d5-117">*alpha*</span></span> 
</dt> <dd>

<span data-ttu-id="121d5-118">Valor alfa que [**glClear**](glclear.md) usa para borrar los búferes de color.</span><span class="sxs-lookup"><span data-stu-id="121d5-118">The alpha value that [**glClear**](glclear.md) uses to clear the color buffers.</span></span> <span data-ttu-id="121d5-119">El valor predeterminado es cero.</span><span class="sxs-lookup"><span data-stu-id="121d5-119">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="121d5-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="121d5-120">Return value</span></span>

<span data-ttu-id="121d5-121">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="121d5-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="121d5-122">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="121d5-122">Error codes</span></span>

<span data-ttu-id="121d5-123">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="121d5-123">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="121d5-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="121d5-124">Name</span></span>                                                                                                  | <span data-ttu-id="121d5-125">Significado</span><span class="sxs-lookup"><span data-stu-id="121d5-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="121d5-126"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="121d5-126"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="121d5-127">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="121d5-127">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="121d5-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="121d5-128">Remarks</span></span>

<span data-ttu-id="121d5-129">La función **glClearColor** especifica los valores rojo, verde, azul y alfa usados por [**glClear**](glclear.md) para borrar los búferes de color.</span><span class="sxs-lookup"><span data-stu-id="121d5-129">The **glClearColor** function specifies the red, green, blue, and alpha values used by [**glClear**](glclear.md) to clear the color buffers.</span></span> <span data-ttu-id="121d5-130">Los valores especificados por **glClearColor** se fijan en el intervalo \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="121d5-130">Values specified by **glClearColor** are clamped to the range \[0,1\].</span></span>

<span data-ttu-id="121d5-131">Las siguientes funciones recuperan información relacionada con la función **glClearColor** :</span><span class="sxs-lookup"><span data-stu-id="121d5-131">The following functions retrieve information related to the **glClearColor** function:</span></span>

<span data-ttu-id="121d5-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ valor Clear acumulado de GL \_</span><span class="sxs-lookup"><span data-stu-id="121d5-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ACCUM\_CLEAR\_VALUE</span></span>

<span data-ttu-id="121d5-133">**glGet** con el argumento \_ GL \_ color \_ valor sin formato</span><span class="sxs-lookup"><span data-stu-id="121d5-133">**glGet** with argument GL\_COLOR\_CLEAR\_VALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="121d5-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="121d5-134">Requirements</span></span>



| <span data-ttu-id="121d5-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="121d5-135">Requirement</span></span> | <span data-ttu-id="121d5-136">Value</span><span class="sxs-lookup"><span data-stu-id="121d5-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="121d5-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="121d5-137">Minimum supported client</span></span><br/> | <span data-ttu-id="121d5-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="121d5-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="121d5-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="121d5-139">Minimum supported server</span></span><br/> | <span data-ttu-id="121d5-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="121d5-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="121d5-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="121d5-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="121d5-142"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="121d5-142"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="121d5-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="121d5-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="121d5-144"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="121d5-144"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="121d5-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="121d5-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="121d5-146"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="121d5-146"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="121d5-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="121d5-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="121d5-148">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="121d5-148">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="121d5-149">**glClear**</span><span class="sxs-lookup"><span data-stu-id="121d5-149">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="121d5-150">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="121d5-150">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="121d5-151">**glGet**</span><span class="sxs-lookup"><span data-stu-id="121d5-151">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





