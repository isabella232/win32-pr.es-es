---
title: Mensaje EM_GETTOUCHOPTIONS (RichEdit. h)
description: Recupera las opciones de toque que están asociadas a un control Rich Edit.
ms.assetid: 1D367818-5625-4A5A-A7A1-330FED516990
keywords:
- EM_GETTOUCHOPTIONS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETTOUCHOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812d37de1972c6da205944d9913dc3fa046c205d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079611"
---
# <a name="em_gettouchoptions-message"></a><span data-ttu-id="2248d-104">\_Mensaje GETTOUCHOPTIONS em</span><span class="sxs-lookup"><span data-stu-id="2248d-104">EM\_GETTOUCHOPTIONS message</span></span>

<span data-ttu-id="2248d-105">Recupera las opciones de toque que están asociadas a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="2248d-105">Retrieves the touch options that are associated with a rich edit control.</span></span>


```C++
#define EM_GETTOUCHOPTIONS       (WM_USER + 310)
```



## <a name="parameters"></a><span data-ttu-id="2248d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2248d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2248d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2248d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2248d-108">Opciones de toque que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="2248d-108">The touch options to retrieve.</span></span> <span data-ttu-id="2248d-109">Puede ser uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="2248d-109">It can be one of the following values.</span></span>



| <span data-ttu-id="2248d-110">Value</span><span class="sxs-lookup"><span data-stu-id="2248d-110">Value</span></span>                                                                                                                                                                        | <span data-ttu-id="2248d-111">Significado</span><span class="sxs-lookup"><span data-stu-id="2248d-111">Meaning</span></span>                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <span data-ttu-id="2248d-112"><dt>**RTO \_ SHOWHANDLES**</dt></span><span class="sxs-lookup"><span data-stu-id="2248d-112"><dt>**RTO\_SHOWHANDLES**</dt></span></span> </dl>          | <span data-ttu-id="2248d-113">Recupera si las redimensionamientos táctiles están visibles.</span><span class="sxs-lookup"><span data-stu-id="2248d-113">Retrieves whether the touch grippers are visible.</span></span><br/> |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <span data-ttu-id="2248d-114"><dt>**RTO \_ DISABLEHANDLES**</dt></span><span class="sxs-lookup"><span data-stu-id="2248d-114"><dt>**RTO\_DISABLEHANDLES**</dt></span></span> </dl> | <span data-ttu-id="2248d-115">No se ha implementado la recuperación de esta marca.</span><span class="sxs-lookup"><span data-stu-id="2248d-115">Retrieving this flag is not implemented.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="2248d-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2248d-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2248d-117">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2248d-117">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2248d-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2248d-118">Return value</span></span>

<span data-ttu-id="2248d-119">Devuelve el valor de la opción especificada por el parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="2248d-119">Returns the value of the option specified by the *wParam* parameter.</span></span> <span data-ttu-id="2248d-120">Es distinto de cero si *wParam* es **RTO \_ SHOWHANDLES** y las redimensionadores táctiles son visibles; de lo contrario, es cero.</span><span class="sxs-lookup"><span data-stu-id="2248d-120">It is nonzero if *wParam* is **RTO\_SHOWHANDLES** and the touch grippers are visible; zero, otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="2248d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2248d-121">Requirements</span></span>



| <span data-ttu-id="2248d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2248d-122">Requirement</span></span> | <span data-ttu-id="2248d-123">Value</span><span class="sxs-lookup"><span data-stu-id="2248d-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2248d-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2248d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2248d-125">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="2248d-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="2248d-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2248d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2248d-127">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="2248d-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2248d-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2248d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2248d-129"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2248d-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2248d-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="2248d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2248d-131">**\_SETTOUCHOPTIONS em**</span><span class="sxs-lookup"><span data-stu-id="2248d-131">**EM\_SETTOUCHOPTIONS**</span></span>](em-settouchoptions.md)
</dt> </dl>

 

 





