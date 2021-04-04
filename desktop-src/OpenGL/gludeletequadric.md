---
title: función gluDeleteQuadric (GLU. h)
description: La función gluDeleteQuadric destruye un objeto quadric.
ms.assetid: 09efd887-0fe8-4a56-bc6f-2177a4930035
keywords:
- gluDeleteQuadric (función) OpenGL
topic_type:
- apiref
api_name:
- gluDeleteQuadric
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b5ee85e943cd958e394efb191932393d228d948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802822"
---
# <a name="gludeletequadric-function"></a><span data-ttu-id="b922e-104">gluDeleteQuadric función)</span><span class="sxs-lookup"><span data-stu-id="b922e-104">gluDeleteQuadric function</span></span>

<span data-ttu-id="b922e-105">La función **gluDeleteQuadric** destruye un objeto quadric.</span><span class="sxs-lookup"><span data-stu-id="b922e-105">The **gluDeleteQuadric** function destroys a quadric object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b922e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b922e-106">Syntax</span></span>


```C++
void WINAPI gluDeleteQuadric(
   GLUquadricObj *state
);
```



## <a name="parameters"></a><span data-ttu-id="b922e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b922e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b922e-108">*state*</span><span class="sxs-lookup"><span data-stu-id="b922e-108">*state*</span></span> 
</dt> <dd>

<span data-ttu-id="b922e-109">El objeto quadric que se va a destruir (creado con [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="b922e-109">The quadric object to be destroyed (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b922e-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b922e-110">Return value</span></span>

<span data-ttu-id="b922e-111">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b922e-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b922e-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b922e-112">Remarks</span></span>

<span data-ttu-id="b922e-113">La función **gluDeleteQuadric** destruye el objeto quadric y libera cualquier memoria que haya usado.</span><span class="sxs-lookup"><span data-stu-id="b922e-113">The **gluDeleteQuadric** function destroys the quadric object and frees any memory that it used.</span></span> <span data-ttu-id="b922e-114">Después de llamar a **gluDeleteQuadric**, no puede volver a usar el *Estado* .</span><span class="sxs-lookup"><span data-stu-id="b922e-114">After you have called **gluDeleteQuadric**, you cannot use *state* again.</span></span>

## <a name="requirements"></a><span data-ttu-id="b922e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b922e-115">Requirements</span></span>



| <span data-ttu-id="b922e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b922e-116">Requirement</span></span> | <span data-ttu-id="b922e-117">Value</span><span class="sxs-lookup"><span data-stu-id="b922e-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b922e-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b922e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b922e-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b922e-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b922e-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b922e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b922e-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b922e-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b922e-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b922e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b922e-123"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="b922e-123"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="b922e-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b922e-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="b922e-125"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b922e-125"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b922e-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b922e-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b922e-127"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b922e-127"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b922e-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b922e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b922e-129">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="b922e-129">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> </dl>

 

 





