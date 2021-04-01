---
title: función gluDeleteTess (GLU. h)
description: La función gluDeleteTess destruye un objeto de teselación.
ms.assetid: 7e1540f7-5e7d-4a3b-8c94-5a6800b17411
keywords:
- gluDeleteTess (función) OpenGL
topic_type:
- apiref
api_name:
- gluDeleteTess
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee4625f0a9c2f51e9d7147c9564fcd4fb1fa7117
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801622"
---
# <a name="gludeletetess-function"></a><span data-ttu-id="e49f9-104">gluDeleteTess función)</span><span class="sxs-lookup"><span data-stu-id="e49f9-104">gluDeleteTess function</span></span>

<span data-ttu-id="e49f9-105">La función **gluDeleteTess** destruye un objeto de teselación.</span><span class="sxs-lookup"><span data-stu-id="e49f9-105">The **gluDeleteTess** function destroys a tessellation object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e49f9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e49f9-106">Syntax</span></span>


```C++
void WINAPI gluDeleteTess(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="e49f9-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e49f9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e49f9-108">*tess*</span><span class="sxs-lookup"><span data-stu-id="e49f9-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="e49f9-109">Objeto de teselación que se va a destruir (creado con [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="e49f9-109">The tessellation object to destroy (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e49f9-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e49f9-110">Return value</span></span>

<span data-ttu-id="e49f9-111">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e49f9-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e49f9-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e49f9-112">Remarks</span></span>

<span data-ttu-id="e49f9-113">La función **gluDeleteTess** destruye el objeto de teselación indicado y libera cualquier memoria que haya usado.</span><span class="sxs-lookup"><span data-stu-id="e49f9-113">The **gluDeleteTess** function destroys the indicated tessellation object and frees any memory that it used.</span></span>

## <a name="requirements"></a><span data-ttu-id="e49f9-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e49f9-114">Requirements</span></span>



| <span data-ttu-id="e49f9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e49f9-115">Requirement</span></span> | <span data-ttu-id="e49f9-116">Value</span><span class="sxs-lookup"><span data-stu-id="e49f9-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e49f9-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e49f9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e49f9-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e49f9-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e49f9-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e49f9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e49f9-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e49f9-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e49f9-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e49f9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e49f9-122"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="e49f9-122"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="e49f9-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e49f9-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="e49f9-124"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e49f9-124"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e49f9-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e49f9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e49f9-126"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e49f9-126"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e49f9-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e49f9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e49f9-128">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="e49f9-128">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="e49f9-129">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="e49f9-129">**gluTessBeginPolygon**</span></span>](glubeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="e49f9-130">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="e49f9-130">*gluTessCallback*</span></span>](glutess.md)
</dt> </dl>

 

 





