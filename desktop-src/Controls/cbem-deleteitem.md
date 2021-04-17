---
title: Mensaje de CBEM_DELETEITEM (commctrl. h)
description: Quita un elemento de un control ComboBoxEx.
ms.assetid: 688cf388-54ba-4b45-88d7-628da49d8615
keywords:
- CBEM_DELETEITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CBEM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa3034f79dffabcd7d7aa780582646e17d30b62f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658395"
---
# <a name="cbem_deleteitem-message"></a><span data-ttu-id="e8da1-104">Mensaje de CBEM \_ DELETEITEM</span><span class="sxs-lookup"><span data-stu-id="e8da1-104">CBEM\_DELETEITEM message</span></span>

<span data-ttu-id="e8da1-105">Quita un elemento de un control ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="e8da1-105">Removes an item from a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e8da1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8da1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8da1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e8da1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8da1-108">Índice de base cero del elemento que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="e8da1-108">The zero-based index of the item to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="e8da1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e8da1-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e8da1-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="e8da1-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8da1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e8da1-111">Return value</span></span>

<span data-ttu-id="e8da1-112">Devuelve un valor INT que representa el número de elementos que quedan en el control.</span><span class="sxs-lookup"><span data-stu-id="e8da1-112">Returns an INT value that represents the number of items remaining in the control.</span></span> <span data-ttu-id="e8da1-113">Si *iIndex* no es válido, el mensaje devuelve un \_ error CB.</span><span class="sxs-lookup"><span data-stu-id="e8da1-113">If *iIndex* is invalid, the message returns CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8da1-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e8da1-114">Remarks</span></span>

<span data-ttu-id="e8da1-115">Este mensaje se asigna al mensaje de control de cuadro combinado [**CB \_ DELETESTRING**](cb-deletestring.md).</span><span class="sxs-lookup"><span data-stu-id="e8da1-115">This message maps to the combo box control message [**CB\_DELETESTRING**](cb-deletestring.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8da1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8da1-116">Requirements</span></span>



| <span data-ttu-id="e8da1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8da1-117">Requirement</span></span> | <span data-ttu-id="e8da1-118">Value</span><span class="sxs-lookup"><span data-stu-id="e8da1-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8da1-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8da1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e8da1-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e8da1-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e8da1-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8da1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e8da1-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e8da1-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e8da1-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8da1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8da1-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8da1-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





