---
title: función glDeleteLists (GL. h)
description: La función glDeleteLists elimina un grupo contiguo de listas de presentación.
ms.assetid: 979ab352-99db-4822-922c-a1813b9fcfce
keywords:
- glDeleteLists (función) OpenGL
topic_type:
- apiref
api_name:
- glDeleteLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c11ae41273cba5bd050a62ea330cef9da0647769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676783"
---
# <a name="gldeletelists-function"></a><span data-ttu-id="23bec-104">glDeleteLists función)</span><span class="sxs-lookup"><span data-stu-id="23bec-104">glDeleteLists function</span></span>

<span data-ttu-id="23bec-105">La función **glDeleteLists** elimina un grupo contiguo de listas de presentación.</span><span class="sxs-lookup"><span data-stu-id="23bec-105">The **glDeleteLists** function deletes a contiguous group of display lists.</span></span>

## <a name="syntax"></a><span data-ttu-id="23bec-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23bec-106">Syntax</span></span>


```C++
void WINAPI glDeleteLists(
   GLuint  list,
   GLsizei range
);
```



## <a name="parameters"></a><span data-ttu-id="23bec-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="23bec-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23bec-108">*list*</span><span class="sxs-lookup"><span data-stu-id="23bec-108">*list*</span></span> 
</dt> <dd>

<span data-ttu-id="23bec-109">Nombre entero de la primera lista de visualización que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="23bec-109">The integer name of the first display list to delete.</span></span>

</dd> <dt>

<span data-ttu-id="23bec-110">*range*</span><span class="sxs-lookup"><span data-stu-id="23bec-110">*range*</span></span> 
</dt> <dd>

<span data-ttu-id="23bec-111">Número de listas de presentación que se van a eliminar.</span><span class="sxs-lookup"><span data-stu-id="23bec-111">The number of display lists to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23bec-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="23bec-112">Return value</span></span>

<span data-ttu-id="23bec-113">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="23bec-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="23bec-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="23bec-114">Error codes</span></span>

<span data-ttu-id="23bec-115">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="23bec-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="23bec-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="23bec-116">Name</span></span>                                                                                                  | <span data-ttu-id="23bec-117">Significado</span><span class="sxs-lookup"><span data-stu-id="23bec-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="23bec-118"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="23bec-118"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="23bec-119">el *intervalo* era negativo.</span><span class="sxs-lookup"><span data-stu-id="23bec-119">*range* was negative.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="23bec-120"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="23bec-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="23bec-121">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="23bec-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="23bec-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="23bec-122">Remarks</span></span>

<span data-ttu-id="23bec-123">La función **glDeleteLists** hace que se elimine un grupo contiguo de listas de presentación.</span><span class="sxs-lookup"><span data-stu-id="23bec-123">The **glDeleteLists** function causes a contiguous group of display lists to be deleted.</span></span> <span data-ttu-id="23bec-124">El parámetro *List* es el nombre de la primera lista de visualización que se va a eliminar y *Range* es el número de listas de presentación que se van a eliminar.</span><span class="sxs-lookup"><span data-stu-id="23bec-124">The *list* parameter is the name of the first display list to be deleted, and *range* is the number of display lists to delete.</span></span> <span data-ttu-id="23bec-125">Se eliminan todas las listas de pantallas *d* *con*  =    =    +  el *intervalo* de lista d de lista 1.</span><span class="sxs-lookup"><span data-stu-id="23bec-125">All display lists *d* with *list* = *d* = *list* + *range* - 1 are deleted.</span></span>

<span data-ttu-id="23bec-126">Todas las ubicaciones de almacenamiento asignadas a las listas de visualización especificadas se liberan y los nombres están disponibles para su reutilización en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="23bec-126">All storage locations allocated to the specified display lists are freed, and the names are available for reuse at a later time.</span></span> <span data-ttu-id="23bec-127">Se omiten los nombres del intervalo que no tienen una lista de visualización asociada.</span><span class="sxs-lookup"><span data-stu-id="23bec-127">Names within the range that do not have an associated display list are ignored.</span></span> <span data-ttu-id="23bec-128">Si el *intervalo* es cero, no sucede nada.</span><span class="sxs-lookup"><span data-stu-id="23bec-128">If *range* is zero, nothing happens.</span></span>

## <a name="requirements"></a><span data-ttu-id="23bec-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23bec-129">Requirements</span></span>



| <span data-ttu-id="23bec-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="23bec-130">Requirement</span></span> | <span data-ttu-id="23bec-131">Value</span><span class="sxs-lookup"><span data-stu-id="23bec-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23bec-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23bec-132">Minimum supported client</span></span><br/> | <span data-ttu-id="23bec-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="23bec-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="23bec-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23bec-134">Minimum supported server</span></span><br/> | <span data-ttu-id="23bec-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="23bec-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="23bec-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23bec-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="23bec-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="23bec-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="23bec-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="23bec-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="23bec-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23bec-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="23bec-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="23bec-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23bec-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23bec-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23bec-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="23bec-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23bec-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="23bec-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="23bec-144">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="23bec-144">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="23bec-145">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="23bec-145">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="23bec-146">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="23bec-146">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="23bec-147">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="23bec-147">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="23bec-148">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="23bec-148">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="23bec-149">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="23bec-149">**glNewList**</span></span>](glnewlist.md)
</dt> </dl>

 

 





