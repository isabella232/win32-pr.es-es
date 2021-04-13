---
title: función glIsList (GL. h)
description: La función gllsList comprueba la existencia de la lista de visualización.
ms.assetid: 86ef3684-8047-4ee4-befd-ec26bcd036c3
keywords:
- glIsList (función) OpenGL
topic_type:
- apiref
api_name:
- glIsList
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fdc67d0a7dad18f8850c283f0d5eb224ff9ebbd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359805"
---
# <a name="glislist-function"></a><span data-ttu-id="0c142-104">glIsList función)</span><span class="sxs-lookup"><span data-stu-id="0c142-104">glIsList function</span></span>

<span data-ttu-id="0c142-105">La función **gllsList** comprueba la existencia de la lista de visualización.</span><span class="sxs-lookup"><span data-stu-id="0c142-105">The **gllsList** function tests for display list existence.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c142-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c142-106">Syntax</span></span>


```C++
GLboolean WINAPI glIsList(
   GLuint list
);
```



## <a name="parameters"></a><span data-ttu-id="0c142-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0c142-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c142-108">*list*</span><span class="sxs-lookup"><span data-stu-id="0c142-108">*list*</span></span> 
</dt> <dd>

<span data-ttu-id="0c142-109">Un nombre de lista de visualización potencial.</span><span class="sxs-lookup"><span data-stu-id="0c142-109">A potential display list name.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="0c142-110">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="0c142-110">Error codes</span></span>

<span data-ttu-id="0c142-111">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="0c142-111">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="0c142-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="0c142-112">Name</span></span>                                                                                                  | <span data-ttu-id="0c142-113">Significado</span><span class="sxs-lookup"><span data-stu-id="0c142-113">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0c142-114"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0c142-114"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="0c142-115">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="0c142-115">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0c142-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0c142-116">Remarks</span></span>

<span data-ttu-id="0c142-117">La función **gllsList** devuelve GL \_ true si *List* es el nombre de una lista de visualización y devuelve GL \_ false en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0c142-117">The **gllsList** function returns GL\_TRUE if *list* is the name of a display list and returns GL\_FALSE otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c142-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c142-118">Requirements</span></span>



| <span data-ttu-id="0c142-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c142-119">Requirement</span></span> | <span data-ttu-id="0c142-120">Value</span><span class="sxs-lookup"><span data-stu-id="0c142-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c142-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c142-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0c142-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0c142-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0c142-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c142-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0c142-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0c142-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0c142-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0c142-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c142-126"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c142-126"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="0c142-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0c142-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="0c142-128"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c142-128"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0c142-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0c142-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c142-130"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c142-130"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c142-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c142-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c142-132">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="0c142-132">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="0c142-133">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="0c142-133">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="0c142-134">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="0c142-134">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="0c142-135">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="0c142-135">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="0c142-136">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="0c142-136">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="0c142-137">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="0c142-137">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="0c142-138">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="0c142-138">**glNewList**</span></span>](glnewlist.md)
</dt> </dl>

 

 





