---
title: Mensaje de LVM_GETHOTITEM (commctrl. h)
description: Recupera el índice del elemento activo. Puede enviar este mensaje explícitamente o utilizar la \_ macro GetHotItem de ListView.
ms.assetid: f80189da-6c8b-4faf-925a-0c33fedf8c4e
keywords:
- LVM_GETHOTITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56c7bbfb845518eb40b55556df5294d59cff3d7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150897"
---
# <a name="lvm_gethotitem-message"></a><span data-ttu-id="2e059-105">\_Mensaje GETHOTITEM LVM</span><span class="sxs-lookup"><span data-stu-id="2e059-105">LVM\_GETHOTITEM message</span></span>

<span data-ttu-id="2e059-106">Recupera el índice del elemento activo.</span><span class="sxs-lookup"><span data-stu-id="2e059-106">Retrieves the index of the hot item.</span></span> <span data-ttu-id="2e059-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetHotItem de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotitem) .</span><span class="sxs-lookup"><span data-stu-id="2e059-107">You can send this message explicitly or use the [**ListView\_GetHotItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2e059-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e059-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e059-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2e059-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2e059-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2e059-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2e059-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e059-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2e059-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2e059-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e059-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e059-113">Return value</span></span>

<span data-ttu-id="2e059-114">Devuelve el índice del elemento que está activo.</span><span class="sxs-lookup"><span data-stu-id="2e059-114">Returns the index of the item that is hot.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e059-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e059-115">Requirements</span></span>



| <span data-ttu-id="2e059-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e059-116">Requirement</span></span> | <span data-ttu-id="2e059-117">Value</span><span class="sxs-lookup"><span data-stu-id="2e059-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e059-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e059-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2e059-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2e059-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2e059-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e059-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2e059-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2e059-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2e059-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e059-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e059-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e059-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





