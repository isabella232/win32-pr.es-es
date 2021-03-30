---
title: función glGenLists (GL. h)
description: La función glGenLists genera un conjunto contiguo de listas de presentación vacías.
ms.assetid: 07a97e89-1fbe-4405-b1b0-c4c47b098633
keywords:
- glGenLists (función) OpenGL
topic_type:
- apiref
api_name:
- glGenLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc556e789da9c768a7ed1aef6880ad48022a1ee4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801508"
---
# <a name="glgenlists-function"></a><span data-ttu-id="1ead2-104">glGenLists función)</span><span class="sxs-lookup"><span data-stu-id="1ead2-104">glGenLists function</span></span>

<span data-ttu-id="1ead2-105">La función **glGenLists** genera un conjunto contiguo de listas de presentación vacías.</span><span class="sxs-lookup"><span data-stu-id="1ead2-105">The **glGenLists** function generates a contiguous set of empty display lists.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ead2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1ead2-106">Syntax</span></span>


```C++
GLuint WINAPI glGenLists(
   GLsizei range
);
```



## <a name="parameters"></a><span data-ttu-id="1ead2-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ead2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ead2-108">*range*</span><span class="sxs-lookup"><span data-stu-id="1ead2-108">*range*</span></span> 
</dt> <dd>

<span data-ttu-id="1ead2-109">Número de listas de presentación vacías contiguas que se van a generar.</span><span class="sxs-lookup"><span data-stu-id="1ead2-109">The number of contiguous empty display lists to be generated.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="1ead2-110">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="1ead2-110">Error codes</span></span>

<span data-ttu-id="1ead2-111">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="1ead2-111">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="1ead2-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="1ead2-112">Name</span></span>                                                                                                  | <span data-ttu-id="1ead2-113">Significado</span><span class="sxs-lookup"><span data-stu-id="1ead2-113">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1ead2-114"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1ead2-114"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="1ead2-115">el *intervalo* era negativo.</span><span class="sxs-lookup"><span data-stu-id="1ead2-115">*range* was negative.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="1ead2-116"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1ead2-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="1ead2-117">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="1ead2-117">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1ead2-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1ead2-118">Remarks</span></span>

<span data-ttu-id="1ead2-119">La función **glGenLists** tiene un argumento, *Range*.</span><span class="sxs-lookup"><span data-stu-id="1ead2-119">The **glGenLists** function has one argument, *range*.</span></span> <span data-ttu-id="1ead2-120">Devuelve un número entero *n* que indica que *hay listas de presentación* vacías contiguas, denominadas *n*, *n* + 1.</span><span class="sxs-lookup"><span data-stu-id="1ead2-120">It returns an integer *n* such that *range* contiguous empty display lists, named *n*, *n* + 1, .</span></span> <span data-ttu-id="1ead2-121">.</span><span class="sxs-lookup"><span data-stu-id="1ead2-121">.</span></span> <span data-ttu-id="1ead2-122">, se crean *n* + (*intervalo* -1).</span><span class="sxs-lookup"><span data-stu-id="1ead2-122">., *n* + (*range* - 1), are created.</span></span> <span data-ttu-id="1ead2-123">Si el *intervalo* es cero, si no hay ningún grupo de nombres contiguos de *intervalo* disponibles, o si se genera algún error, no se genera ninguna lista de presentación y se devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="1ead2-123">If *range* is zero, if there is no group of *range* contiguous names available, or if any error is generated, then no display lists are generated and zero is returned.</span></span>

<span data-ttu-id="1ead2-124">La siguiente función recupera información relacionada con **glGenLists**:</span><span class="sxs-lookup"><span data-stu-id="1ead2-124">The following function retrieves information related to **glGenLists**:</span></span>

[<span data-ttu-id="1ead2-125">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="1ead2-125">**glIsList**</span></span>](glislist.md)

## <a name="requirements"></a><span data-ttu-id="1ead2-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ead2-126">Requirements</span></span>



| <span data-ttu-id="1ead2-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ead2-127">Requirement</span></span> | <span data-ttu-id="1ead2-128">Value</span><span class="sxs-lookup"><span data-stu-id="1ead2-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ead2-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ead2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1ead2-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1ead2-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1ead2-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ead2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1ead2-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1ead2-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1ead2-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1ead2-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ead2-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ead2-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1ead2-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1ead2-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="1ead2-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ead2-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1ead2-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1ead2-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ead2-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ead2-138"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ead2-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ead2-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ead2-140">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="1ead2-140">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="1ead2-141">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="1ead2-141">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="1ead2-142">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="1ead2-142">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="1ead2-143">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="1ead2-143">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="1ead2-144">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="1ead2-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="1ead2-145">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="1ead2-145">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="1ead2-146">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="1ead2-146">**glNewList**</span></span>](glnewlist.md)
</dt> </dl>

 

 





