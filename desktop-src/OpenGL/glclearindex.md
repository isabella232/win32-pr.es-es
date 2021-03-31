---
title: función glClearIndex (GL. h)
description: La función glClearIndex especifica el valor no cifrado de los búferes de índice de color.
ms.assetid: 87983d93-c5a1-445f-8621-1c2952d93a0f
keywords:
- glClearIndex (función) OpenGL
topic_type:
- apiref
api_name:
- glClearIndex
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b1ed90b017828e13d387e1e6db440c1d781cb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491134"
---
# <a name="glclearindex-function"></a><span data-ttu-id="a443f-104">glClearIndex función)</span><span class="sxs-lookup"><span data-stu-id="a443f-104">glClearIndex function</span></span>

<span data-ttu-id="a443f-105">La función **glClearIndex** especifica el valor no cifrado de los búferes de índice de color.</span><span class="sxs-lookup"><span data-stu-id="a443f-105">The **glClearIndex** function specifies the clear value for the color-index buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="a443f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a443f-106">Syntax</span></span>


```C++
void WINAPI glClearIndex(
   GLfloat c
);
```



## <a name="parameters"></a><span data-ttu-id="a443f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a443f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a443f-108">*c*</span><span class="sxs-lookup"><span data-stu-id="a443f-108">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="a443f-109">Índice que se utiliza cuando se borran los búferes de índice de color.</span><span class="sxs-lookup"><span data-stu-id="a443f-109">The index used when the color-index buffers are cleared.</span></span> <span data-ttu-id="a443f-110">El valor predeterminado es cero.</span><span class="sxs-lookup"><span data-stu-id="a443f-110">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a443f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a443f-111">Return value</span></span>

<span data-ttu-id="a443f-112">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a443f-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a443f-113">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="a443f-113">Error codes</span></span>

<span data-ttu-id="a443f-114">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="a443f-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a443f-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="a443f-115">Name</span></span>                                                                                                  | <span data-ttu-id="a443f-116">Significado</span><span class="sxs-lookup"><span data-stu-id="a443f-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a443f-117"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a443f-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a443f-118">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="a443f-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a443f-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a443f-119">Remarks</span></span>

<span data-ttu-id="a443f-120">La función **glClearIndex** especifica el índice usado por [**glClear**](glclear.md) para borrar los búferes de índice de color.</span><span class="sxs-lookup"><span data-stu-id="a443f-120">The **glClearIndex** function specifies the index used by [**glClear**](glclear.md) to clear the color-index buffers.</span></span> <span data-ttu-id="a443f-121">El parámetro *c* no está fijado.</span><span class="sxs-lookup"><span data-stu-id="a443f-121">The *c* parameter is not clamped.</span></span> <span data-ttu-id="a443f-122">En su lugar, *c* se convierte en un valor de punto fijo con una precisión no especificada a la derecha del punto binario.</span><span class="sxs-lookup"><span data-stu-id="a443f-122">Rather, *c* is converted to a fixed-point value with unspecified precision to the right of the binary point.</span></span> <span data-ttu-id="a443f-123">A continuación, la parte entera de este valor se enmascara con 2 <sup>m</sup>  -1, donde *m* es el número de bits de un índice de color almacenado en el fotogramas.</span><span class="sxs-lookup"><span data-stu-id="a443f-123">The integer part of this value is then masked with 2 <sup>m</sup>  - 1, where *m* is the number of bits in a color index stored in the framebuffer.</span></span>

<span data-ttu-id="a443f-124">Las siguientes funciones recuperan información relacionada con **glClearIndex**:</span><span class="sxs-lookup"><span data-stu-id="a443f-124">The following functions retrieve information related to **glClearIndex**:</span></span>

<span data-ttu-id="a443f-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ valor sin formato de índice de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="a443f-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_INDEX\_CLEAR\_VALUE</span></span>

<span data-ttu-id="a443f-126">**glGet** con argumento \_ bits de índice de GL \_</span><span class="sxs-lookup"><span data-stu-id="a443f-126">**glGet** with argument GL\_INDEX\_BITS</span></span>

## <a name="requirements"></a><span data-ttu-id="a443f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a443f-127">Requirements</span></span>



| <span data-ttu-id="a443f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a443f-128">Requirement</span></span> | <span data-ttu-id="a443f-129">Value</span><span class="sxs-lookup"><span data-stu-id="a443f-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a443f-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a443f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a443f-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a443f-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a443f-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a443f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a443f-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a443f-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a443f-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a443f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a443f-135"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a443f-135"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a443f-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a443f-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="a443f-137"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a443f-137"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a443f-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a443f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a443f-139"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a443f-139"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a443f-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="a443f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a443f-141">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a443f-141">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a443f-142">**glClear**</span><span class="sxs-lookup"><span data-stu-id="a443f-142">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="a443f-143">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="a443f-143">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a443f-144">**glGet**</span><span class="sxs-lookup"><span data-stu-id="a443f-144">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





