---
title: función glStencilMask (GL. h)
description: La función glStencilMask controla la escritura de bits individuales en los planos de la galería de símbolos.
ms.assetid: c586f9db-bad5-4f06-a194-a8d979842d0c
keywords:
- glStencilMask (función) OpenGL
topic_type:
- apiref
api_name:
- glStencilMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e63790fa30e88abbde6e1ba47e624c6caf2dcfc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151192"
---
# <a name="glstencilmask-function"></a><span data-ttu-id="82e0b-104">glStencilMask función)</span><span class="sxs-lookup"><span data-stu-id="82e0b-104">glStencilMask function</span></span>

<span data-ttu-id="82e0b-105">La función **glStencilMask** controla la escritura de bits individuales en los planos de la galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="82e0b-105">The **glStencilMask** function controls the writing of individual bits in the stencil planes.</span></span>

## <a name="syntax"></a><span data-ttu-id="82e0b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82e0b-106">Syntax</span></span>


```C++
void WINAPI glStencilMask(
   GLuint mask
);
```



## <a name="parameters"></a><span data-ttu-id="82e0b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82e0b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82e0b-108">*mask*</span><span class="sxs-lookup"><span data-stu-id="82e0b-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="82e0b-109">Máscara de bits para habilitar y deshabilitar la escritura de bits individuales en los planos de la galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="82e0b-109">A bit mask to enable and disable writing of individual bits in the stencil planes.</span></span> <span data-ttu-id="82e0b-110">Inicialmente, la máscara es todas.</span><span class="sxs-lookup"><span data-stu-id="82e0b-110">Initially, the mask is all ones.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82e0b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82e0b-111">Return value</span></span>

<span data-ttu-id="82e0b-112">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="82e0b-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="82e0b-113">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="82e0b-113">Error codes</span></span>

<span data-ttu-id="82e0b-114">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="82e0b-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="82e0b-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="82e0b-115">Name</span></span>                                                                                                  | <span data-ttu-id="82e0b-116">Significado</span><span class="sxs-lookup"><span data-stu-id="82e0b-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="82e0b-117"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="82e0b-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="82e0b-118">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="82e0b-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="82e0b-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82e0b-119">Remarks</span></span>

<span data-ttu-id="82e0b-120">La función **glStencilMask** controla la escritura de bits individuales en los planos de la galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="82e0b-120">The **glStencilMask** function controls the writing of individual bits in the stencil planes.</span></span> <span data-ttu-id="82e0b-121">Los *n* bits menos significativos de la *máscara*, donde *n* es el número de bits en el búfer de estarcido, especifique una máscara.</span><span class="sxs-lookup"><span data-stu-id="82e0b-121">The least significant *n* bits of *mask*, where *n* is the number of bits in the stencil buffer, specify a mask.</span></span> <span data-ttu-id="82e0b-122">Siempre que aparezca una en la máscara, el bit correspondiente en el búfer de estarcido se convierte en grabable.</span><span class="sxs-lookup"><span data-stu-id="82e0b-122">Wherever a one appears in the mask, the corresponding bit in the stencil buffer is made writable.</span></span> <span data-ttu-id="82e0b-123">Cuando aparece un cero, el bit está protegido contra escritura.</span><span class="sxs-lookup"><span data-stu-id="82e0b-123">Where a zero appears, the bit is write-protected.</span></span> <span data-ttu-id="82e0b-124">Inicialmente, todos los bits están habilitados para escritura.</span><span class="sxs-lookup"><span data-stu-id="82e0b-124">Initially, all bits are enabled for writing.</span></span>

<span data-ttu-id="82e0b-125">Las siguientes funciones recuperan información relacionada con **glStencilMask**:</span><span class="sxs-lookup"><span data-stu-id="82e0b-125">The following functions retrieve information related to **glStencilMask**:</span></span>

<span data-ttu-id="82e0b-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL de la \_ Galería de símbolos \_ WRITEMASK</span><span class="sxs-lookup"><span data-stu-id="82e0b-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_STENCIL\_WRITEMASK</span></span>

<span data-ttu-id="82e0b-127">glGet con el argumento \_ bits de estarcido GL \_</span><span class="sxs-lookup"><span data-stu-id="82e0b-127">glGet with argument GL\_STENCIL\_BITS</span></span>

## <a name="requirements"></a><span data-ttu-id="82e0b-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82e0b-128">Requirements</span></span>



| <span data-ttu-id="82e0b-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="82e0b-129">Requirement</span></span> | <span data-ttu-id="82e0b-130">Value</span><span class="sxs-lookup"><span data-stu-id="82e0b-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82e0b-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82e0b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="82e0b-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="82e0b-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="82e0b-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82e0b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="82e0b-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="82e0b-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="82e0b-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82e0b-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="82e0b-136"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="82e0b-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="82e0b-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="82e0b-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="82e0b-138"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82e0b-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="82e0b-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="82e0b-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82e0b-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82e0b-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82e0b-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="82e0b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82e0b-142">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="82e0b-142">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="82e0b-143">**glColorMask**</span><span class="sxs-lookup"><span data-stu-id="82e0b-143">**glColorMask**</span></span>](glcolormask.md)
</dt> <dt>

[<span data-ttu-id="82e0b-144">**glDepthMask**</span><span class="sxs-lookup"><span data-stu-id="82e0b-144">**glDepthMask**</span></span>](gldepthmask.md)
</dt> <dt>

[<span data-ttu-id="82e0b-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="82e0b-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="82e0b-146">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="82e0b-146">**glIndexMask**</span></span>](glindexmask.md)
</dt> <dt>

[<span data-ttu-id="82e0b-147">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="82e0b-147">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> <dt>

[<span data-ttu-id="82e0b-148">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="82e0b-148">**glStencilOp**</span></span>](glstencilop.md)
</dt> </dl>

 

 





