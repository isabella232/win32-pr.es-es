---
title: función glIndexMask (GL. h)
description: La función glIndexMask controla la escritura de bits individuales en los búferes de índice de color.
ms.assetid: f4b5df36-390f-4254-95fb-98589750a11b
keywords:
- glIndexMask (función) OpenGL
topic_type:
- apiref
api_name:
- glIndexMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d426cb1f4bb2e794bef53853d0336db1d64b263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665934"
---
# <a name="glindexmask-function"></a><span data-ttu-id="e28b4-104">glIndexMask función)</span><span class="sxs-lookup"><span data-stu-id="e28b4-104">glIndexMask function</span></span>

<span data-ttu-id="e28b4-105">La función **glIndexMask** controla la escritura de bits individuales en los búferes de índice de color.</span><span class="sxs-lookup"><span data-stu-id="e28b4-105">The **glIndexMask** function controls the writing of individual bits in the color-index buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="e28b4-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e28b4-106">Syntax</span></span>


```C++
void WINAPI glIndexMask(
   GLuint mask
);
```



## <a name="parameters"></a><span data-ttu-id="e28b4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e28b4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e28b4-108">*mask*</span><span class="sxs-lookup"><span data-stu-id="e28b4-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="e28b4-109">Máscara de bits para habilitar y deshabilitar la escritura de bits individuales en los búferes de índice de color.</span><span class="sxs-lookup"><span data-stu-id="e28b4-109">A bit mask to enable and disable the writing of individual bits in the color-index buffers.</span></span> <span data-ttu-id="e28b4-110">Inicialmente, la máscara es todas.</span><span class="sxs-lookup"><span data-stu-id="e28b4-110">Initially, the mask is all ones.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e28b4-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e28b4-111">Return value</span></span>

<span data-ttu-id="e28b4-112">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e28b4-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e28b4-113">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="e28b4-113">Error codes</span></span>

<span data-ttu-id="e28b4-114">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="e28b4-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e28b4-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="e28b4-115">Name</span></span>                                                                                                  | <span data-ttu-id="e28b4-116">Significado</span><span class="sxs-lookup"><span data-stu-id="e28b4-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e28b4-117"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e28b4-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e28b4-118">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="e28b4-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e28b4-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e28b4-119">Remarks</span></span>

<span data-ttu-id="e28b4-120">La función **glIndexMask** controla la escritura de bits individuales en los búferes de índice de color.</span><span class="sxs-lookup"><span data-stu-id="e28b4-120">The **glIndexMask** function controls the writing of individual bits in the color-index buffers.</span></span> <span data-ttu-id="e28b4-121">Los *n* bits menos significativos de la *máscara*, donde *1* es el número de bits en un búfer de índice de color, especifique una máscara.</span><span class="sxs-lookup"><span data-stu-id="e28b4-121">The least significant *n* bits of *mask*, where *1* is the number of bits in a color-index buffer, specify a mask.</span></span> <span data-ttu-id="e28b4-122">Siempre que aparezca una en la máscara, el bit correspondiente en el búfer de índice de color (o búferes) se convierte en grabable.</span><span class="sxs-lookup"><span data-stu-id="e28b4-122">Wherever a one appears in the mask, the corresponding bit in the color-index buffer (or buffers) is made writable.</span></span> <span data-ttu-id="e28b4-123">Cuando aparece un cero, el bit está protegido contra escritura.</span><span class="sxs-lookup"><span data-stu-id="e28b4-123">Where a zero appears, the bit is write-protected.</span></span>

<span data-ttu-id="e28b4-124">Esta máscara solo se usa en modo de índice de color y afecta solo a los búferes seleccionados actualmente para escritura (vea [**glDrawBuffer**](gldrawbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="e28b4-124">This mask is used only in color-index mode, and it affects only the buffers currently selected for writing (see [**glDrawBuffer**](gldrawbuffer.md)).</span></span> <span data-ttu-id="e28b4-125">Inicialmente, todos los bits están habilitados para escritura.</span><span class="sxs-lookup"><span data-stu-id="e28b4-125">Initially, all bits are enabled for writing.</span></span>

<span data-ttu-id="e28b4-126">La siguiente función recupera información relacionada con **glIndexMask**:</span><span class="sxs-lookup"><span data-stu-id="e28b4-126">The following function retrieves information related to **glIndexMask**:</span></span>

<span data-ttu-id="e28b4-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ index \_ WRITEMASK</span><span class="sxs-lookup"><span data-stu-id="e28b4-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_INDEX\_WRITEMASK</span></span>

## <a name="requirements"></a><span data-ttu-id="e28b4-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e28b4-128">Requirements</span></span>



| <span data-ttu-id="e28b4-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e28b4-129">Requirement</span></span> | <span data-ttu-id="e28b4-130">Value</span><span class="sxs-lookup"><span data-stu-id="e28b4-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e28b4-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e28b4-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e28b4-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e28b4-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e28b4-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e28b4-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e28b4-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e28b4-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e28b4-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e28b4-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e28b4-136"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e28b4-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e28b4-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e28b4-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="e28b4-138"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e28b4-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e28b4-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e28b4-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e28b4-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e28b4-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e28b4-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="e28b4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e28b4-142">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e28b4-142">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e28b4-143">**glDepthMask**</span><span class="sxs-lookup"><span data-stu-id="e28b4-143">**glDepthMask**</span></span>](gldepthmask.md)
</dt> <dt>

[<span data-ttu-id="e28b4-144">**glDrawBuffer**</span><span class="sxs-lookup"><span data-stu-id="e28b4-144">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="e28b4-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e28b4-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e28b4-146">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="e28b4-146">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="e28b4-147">**glStencilMask**</span><span class="sxs-lookup"><span data-stu-id="e28b4-147">**glStencilMask**</span></span>](glstencilmask.md)
</dt> </dl>

 

 





