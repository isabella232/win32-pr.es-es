---
title: Mensaje de LVM_GETINSERTMARKRECT (commctrl. h)
description: Recupera el rectángulo que delimita el punto de inserción.
ms.assetid: 7b10229c-73ab-426c-8a8a-71258a33e248
keywords:
- LVM_GETINSERTMARKRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARKRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd85bfb94f6425d2666372fd141b531fcb238643
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996917"
---
# <a name="lvm_getinsertmarkrect-message"></a><span data-ttu-id="53a9a-104">\_Mensaje GETINSERTMARKRECT LVM</span><span class="sxs-lookup"><span data-stu-id="53a9a-104">LVM\_GETINSERTMARKRECT message</span></span>

<span data-ttu-id="53a9a-105">Recupera el rectángulo que delimita el punto de inserción.</span><span class="sxs-lookup"><span data-stu-id="53a9a-105">Retrieves the rectangle that bounds the insertion point.</span></span>

## <a name="parameters"></a><span data-ttu-id="53a9a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="53a9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53a9a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="53a9a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="53a9a-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="53a9a-108">Not used; must be zero.</span></span></dd> <dt>

<span data-ttu-id="53a9a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53a9a-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="53a9a-110">Puntero a una estructura <a href="/previous-versions//dd162897(v=vs.85)">**Rect**</a> que contiene las coordenadas de un rectángulo que delimita el punto de inserción.</span><span class="sxs-lookup"><span data-stu-id="53a9a-110">Pointer to a <a href="/previous-versions//dd162897(v=vs.85)">**RECT**</a> structure that contains the coordinates of a rectangle that bounds the insertion point.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53a9a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53a9a-111">Return value</span></span>

<span data-ttu-id="53a9a-112">Devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="53a9a-112">Returns one of the following values.</span></span>



| <span data-ttu-id="53a9a-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="53a9a-113">Return code</span></span>                                                                      | <span data-ttu-id="53a9a-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="53a9a-114">Description</span></span>                          |
|----------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="53a9a-115"><dt>**0,1**</dt></span><span class="sxs-lookup"><span data-stu-id="53a9a-115"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="53a9a-116">No se encontró ningún punto de inserción.</span><span class="sxs-lookup"><span data-stu-id="53a9a-116">No insertion point found.</span></span><br/> |
| <dl> <span data-ttu-id="53a9a-117"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="53a9a-117"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="53a9a-118">Se encontró el punto de inserción.</span><span class="sxs-lookup"><span data-stu-id="53a9a-118">Insertion point found.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="53a9a-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53a9a-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="53a9a-120">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="53a9a-120">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="53a9a-121">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="53a9a-121">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="53a9a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53a9a-122">Requirements</span></span>



| <span data-ttu-id="53a9a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="53a9a-123">Requirement</span></span> | <span data-ttu-id="53a9a-124">Value</span><span class="sxs-lookup"><span data-stu-id="53a9a-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="53a9a-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53a9a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="53a9a-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="53a9a-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="53a9a-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53a9a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="53a9a-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="53a9a-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="53a9a-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53a9a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="53a9a-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="53a9a-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

