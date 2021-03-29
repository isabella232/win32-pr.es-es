---
title: función glClearDepth (GL. h)
description: La función glClearDepth especifica el valor sin cifrar para el búfer de profundidad.
ms.assetid: 8e26ae78-edc1-4201-a0db-d5bc8ae6dc82
keywords:
- glClearDepth (función) OpenGL
topic_type:
- apiref
api_name:
- glClearDepth
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cf968c7ae172bf4ce354c84b2071d62304327ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359754"
---
# <a name="glcleardepth-function"></a><span data-ttu-id="431c3-104">glClearDepth función)</span><span class="sxs-lookup"><span data-stu-id="431c3-104">glClearDepth function</span></span>

<span data-ttu-id="431c3-105">La función **glClearDepth** especifica el valor sin cifrar para el búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="431c3-105">The **glClearDepth** function specifies the clear value for the depth buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="431c3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="431c3-106">Syntax</span></span>


```C++
void WINAPI glClearDepth(
   GLclampd depth
);
```



## <a name="parameters"></a><span data-ttu-id="431c3-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="431c3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="431c3-108">*amplia*</span><span class="sxs-lookup"><span data-stu-id="431c3-108">*depth*</span></span> 
</dt> <dd>

<span data-ttu-id="431c3-109">Valor de profundidad que se usa cuando se borra el búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="431c3-109">The depth value used when the depth buffer is cleared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="431c3-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="431c3-110">Return value</span></span>

<span data-ttu-id="431c3-111">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="431c3-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="431c3-112">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="431c3-112">Error codes</span></span>

<span data-ttu-id="431c3-113">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="431c3-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="431c3-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="431c3-114">Name</span></span>                                                                                                  | <span data-ttu-id="431c3-115">Significado</span><span class="sxs-lookup"><span data-stu-id="431c3-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="431c3-116"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="431c3-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="431c3-117">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="431c3-117">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="431c3-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="431c3-118">Remarks</span></span>

<span data-ttu-id="431c3-119">La función **glClearDepth** especifica el valor de profundidad usado por [**glClear**](glclear.md) para borrar el búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="431c3-119">The **glClearDepth** function specifies the depth value used by [**glClear**](glclear.md) to clear the depth buffer.</span></span> <span data-ttu-id="431c3-120">Los valores especificados por **glClearDepth** se fijan en el intervalo \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="431c3-120">Values specified by **glClearDepth** are clamped to the range \[0,1\].</span></span>

<span data-ttu-id="431c3-121">La siguiente función recupera información relacionada con la función **glClearDepth** :</span><span class="sxs-lookup"><span data-stu-id="431c3-121">The following function retrieves information related to the **glClearDepth** function:</span></span>

<span data-ttu-id="431c3-122">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con valor de profundidad de GL de argumento \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="431c3-122">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_DEPTH\_CLEAR\_VALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="431c3-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="431c3-123">Requirements</span></span>



| <span data-ttu-id="431c3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="431c3-124">Requirement</span></span> | <span data-ttu-id="431c3-125">Value</span><span class="sxs-lookup"><span data-stu-id="431c3-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="431c3-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="431c3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="431c3-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="431c3-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="431c3-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="431c3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="431c3-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="431c3-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="431c3-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="431c3-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="431c3-131"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="431c3-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="431c3-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="431c3-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="431c3-133"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="431c3-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="431c3-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="431c3-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="431c3-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="431c3-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="431c3-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="431c3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="431c3-137">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="431c3-137">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="431c3-138">**glClear**</span><span class="sxs-lookup"><span data-stu-id="431c3-138">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="431c3-139">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="431c3-139">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="431c3-140">**glGet**</span><span class="sxs-lookup"><span data-stu-id="431c3-140">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





