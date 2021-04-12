---
title: función gluQuadricCallback (GLU. h)
description: La función gluQuadricCallback define una devolución de llamada para un objeto quadric.
ms.assetid: 1f1e9fe9-7239-419c-92b6-af2534850ac5
keywords:
- gluQuadricCallback (función) OpenGL
topic_type:
- apiref
api_name:
- gluQuadricCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c0c92e3cd4e723b59ee9060c5e2f33b710e7f69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534798"
---
# <a name="gluquadriccallback-function"></a><span data-ttu-id="8c85c-104">gluQuadricCallback función)</span><span class="sxs-lookup"><span data-stu-id="8c85c-104">gluQuadricCallback function</span></span>

<span data-ttu-id="8c85c-105">La función **gluQuadricCallback** define una devolución de llamada para un objeto quadric.</span><span class="sxs-lookup"><span data-stu-id="8c85c-105">The **gluQuadricCallback** function defines a callback for a quadric object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c85c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c85c-106">Syntax</span></span>


```C++
void WINAPI gluQuadricCallback(
   GLUquadric *qobj,
   GLenum     which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a><span data-ttu-id="8c85c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c85c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c85c-108">*qobj*</span><span class="sxs-lookup"><span data-stu-id="8c85c-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="8c85c-109">El objeto quadric (creado con [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="8c85c-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="8c85c-110">*cuales*</span><span class="sxs-lookup"><span data-stu-id="8c85c-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="8c85c-111">Devolución de llamada que se está definiendo.</span><span class="sxs-lookup"><span data-stu-id="8c85c-111">The callback being defined.</span></span> <span data-ttu-id="8c85c-112">El único valor válido es GLU \_ error.</span><span class="sxs-lookup"><span data-stu-id="8c85c-112">The only valid value is GLU\_ERROR.</span></span>



| <span data-ttu-id="8c85c-113">Value</span><span class="sxs-lookup"><span data-stu-id="8c85c-113">Value</span></span>                                                                                                                                             | <span data-ttu-id="8c85c-114">Significado</span><span class="sxs-lookup"><span data-stu-id="8c85c-114">Meaning</span></span>                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_ERROR"></span><span id="glu_error"></span><dl> <span data-ttu-id="8c85c-115"><dt>**\_error Glu**</dt></span><span class="sxs-lookup"><span data-stu-id="8c85c-115"><dt>**GLU\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="8c85c-116">Se llama a la función **gluQuadricCallback** cuando se produce un error.</span><span class="sxs-lookup"><span data-stu-id="8c85c-116">The **gluQuadricCallback** function is called when an error is encountered.</span></span> <span data-ttu-id="8c85c-117">Su único argumento es de tipo **GLenum** y indica el error específico que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="8c85c-117">Its single argument is of type **GLenum**, and it indicates the specific error that occurred.</span></span> <span data-ttu-id="8c85c-118">Las cadenas de caracteres que describen estos errores se pueden recuperar con la llamada a [**gluErrorString**](gluerrorstring.md) .</span><span class="sxs-lookup"><span data-stu-id="8c85c-118">Character strings describing these errors can be retrieved with the [**gluErrorString**](gluerrorstring.md) call.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8c85c-119">*fn*</span><span class="sxs-lookup"><span data-stu-id="8c85c-119">*fn*</span></span> 
</dt> <dd>

<span data-ttu-id="8c85c-120">Función a la que se va a llamar.</span><span class="sxs-lookup"><span data-stu-id="8c85c-120">The function to be called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c85c-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c85c-121">Return value</span></span>

<span data-ttu-id="8c85c-122">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8c85c-122">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c85c-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c85c-123">Remarks</span></span>

<span data-ttu-id="8c85c-124">Use **gluQuadricCallback** para definir una nueva devolución de llamada que se va a usar en un objeto quadric.</span><span class="sxs-lookup"><span data-stu-id="8c85c-124">Use **gluQuadricCallback** to define a new callback to be used by a quadric object.</span></span> <span data-ttu-id="8c85c-125">Si la devolución de llamada especificada ya está definida, se reemplaza.</span><span class="sxs-lookup"><span data-stu-id="8c85c-125">If the specified callback is already defined, it is replaced.</span></span> <span data-ttu-id="8c85c-126">Si *FN* es **null**, se borra cualquier devolución de llamada existente.</span><span class="sxs-lookup"><span data-stu-id="8c85c-126">If *fn* is **NULL**, any existing callback is erased.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c85c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c85c-127">Requirements</span></span>



| <span data-ttu-id="8c85c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c85c-128">Requirement</span></span> | <span data-ttu-id="8c85c-129">Value</span><span class="sxs-lookup"><span data-stu-id="8c85c-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8c85c-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c85c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8c85c-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8c85c-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8c85c-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c85c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8c85c-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8c85c-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8c85c-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c85c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c85c-135"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c85c-135"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="8c85c-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8c85c-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="8c85c-137"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c85c-137"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8c85c-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8c85c-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c85c-139"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c85c-139"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c85c-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c85c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c85c-141">**gluErrorString**</span><span class="sxs-lookup"><span data-stu-id="8c85c-141">**gluErrorString**</span></span>](gluerrorstring.md)
</dt> <dt>

[<span data-ttu-id="8c85c-142">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="8c85c-142">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> </dl>

 

 





