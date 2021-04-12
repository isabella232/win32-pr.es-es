---
title: Mensaje EM_INSERTIMAGE (RichEdit. h)
description: Reemplaza la selección por un BLOB que muestra una imagen.
ms.assetid: 147B298B-C4A9-455B-9736-A0B09D72902B
keywords:
- EM_INSERTIMAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_INSERTIMAGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9ff1e0fd355cf5dd8d43d211c44fda6417c638
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489449"
---
# <a name="em_insertimage-message"></a><span data-ttu-id="82ae6-104">\_Mensaje INSERTIMAGE em</span><span class="sxs-lookup"><span data-stu-id="82ae6-104">EM\_INSERTIMAGE message</span></span>

<span data-ttu-id="82ae6-105">Reemplaza la selección por un BLOB que muestra una imagen.</span><span class="sxs-lookup"><span data-stu-id="82ae6-105">Replaces the selection with a blob that displays an image.</span></span>


```C++
#define EM_INSERTIMAGE       (WM_USER + 314)
```



## <a name="parameters"></a><span data-ttu-id="82ae6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82ae6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82ae6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="82ae6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="82ae6-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="82ae6-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="82ae6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="82ae6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="82ae6-110">Puntero a una estructura [**de \_ \_ parámetros de imagen de RICHEDIT**](/windows/win32/api/richedit/ns-richedit-richedit_image_parameters) que contiene el BLOB de la imagen.</span><span class="sxs-lookup"><span data-stu-id="82ae6-110">A pointer to a [**RICHEDIT\_IMAGE\_PARAMETERS**](/windows/win32/api/richedit/ns-richedit-richedit_image_parameters) structure that contains the image blob.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82ae6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82ae6-111">Return value</span></span>

<span data-ttu-id="82ae6-112">Devuelve \_ si es correcto, o uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="82ae6-112">Returns S\_OK if successful, or one of the following error codes.</span></span>



| <span data-ttu-id="82ae6-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="82ae6-113">Return code</span></span>                                                                                    | <span data-ttu-id="82ae6-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="82ae6-114">Description</span></span>                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="82ae6-115"><dt>**E \_ ERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="82ae6-115"><dt>**E\_FAIL** </dt></span></span> </dl>        | <span data-ttu-id="82ae6-116">No se puede insertar la imagen.</span><span class="sxs-lookup"><span data-stu-id="82ae6-116">Cannot insert the image.</span></span> <br/>                          |
| <dl> <span data-ttu-id="82ae6-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="82ae6-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="82ae6-118">El parámetro *lParam* es null o apunta a una imagen no válida.</span><span class="sxs-lookup"><span data-stu-id="82ae6-118">The *lParam* parameter is NULL or points to an invalid image.</span></span> |
| <dl> <span data-ttu-id="82ae6-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="82ae6-119"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl> | <span data-ttu-id="82ae6-120">Memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="82ae6-120">Insufficient memory is available.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="82ae6-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82ae6-121">Remarks</span></span>

<span data-ttu-id="82ae6-122">Si la selección es un punto de inserción, el BLOB de imagen se inserta en el punto de inserción.</span><span class="sxs-lookup"><span data-stu-id="82ae6-122">If the selection is an insertion point, the image blob is inserted at the insertion point.</span></span>

## <a name="requirements"></a><span data-ttu-id="82ae6-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82ae6-123">Requirements</span></span>



| <span data-ttu-id="82ae6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="82ae6-124">Requirement</span></span> | <span data-ttu-id="82ae6-125">Value</span><span class="sxs-lookup"><span data-stu-id="82ae6-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="82ae6-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82ae6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="82ae6-127">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="82ae6-127">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="82ae6-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82ae6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="82ae6-129">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="82ae6-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="82ae6-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82ae6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="82ae6-131"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="82ae6-131"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82ae6-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="82ae6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82ae6-133">**\_INSERTTABLE em**</span><span class="sxs-lookup"><span data-stu-id="82ae6-133">**EM\_INSERTTABLE**</span></span>](em-inserttable.md)
</dt> </dl>

 

 





