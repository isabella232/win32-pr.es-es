---
title: Mensaje de RB_GETBARINFO (commctrl. h)
description: Recupera información sobre el control rebar y la lista de imágenes que utiliza.
ms.assetid: d3d56b95-7540-4e45-bb2e-b9d41cfcca0d
keywords:
- RB_GETBARINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_GETBARINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d224c7c826bad0d5d6ae76ce5a4c2266632fa8a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079557"
---
# <a name="rb_getbarinfo-message"></a><span data-ttu-id="dd3cb-104">Mensaje de GETBARINFO de RB \_</span><span class="sxs-lookup"><span data-stu-id="dd3cb-104">RB\_GETBARINFO message</span></span>

<span data-ttu-id="dd3cb-105">Recupera información sobre el control rebar y la lista de imágenes que utiliza.</span><span class="sxs-lookup"><span data-stu-id="dd3cb-105">Retrieves information about the rebar control and the image list it uses.</span></span>

## <a name="parameters"></a><span data-ttu-id="dd3cb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dd3cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd3cb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dd3cb-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="dd3cb-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="dd3cb-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="dd3cb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dd3cb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dd3cb-110">Puntero a una estructura [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) que recibirá la información del control rebar.</span><span class="sxs-lookup"><span data-stu-id="dd3cb-110">Pointer to a [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) structure that will receive the rebar control information.</span></span> <span data-ttu-id="dd3cb-111">Debe establecer el miembro **cbSize** de esta estructura en **sizeof**(REBARINFO) antes de enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="dd3cb-111">You must set the **cbSize** member of this structure to **sizeof**(REBARINFO) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd3cb-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dd3cb-112">Return value</span></span>

<span data-ttu-id="dd3cb-113">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="dd3cb-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd3cb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd3cb-114">Requirements</span></span>



| <span data-ttu-id="dd3cb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd3cb-115">Requirement</span></span> | <span data-ttu-id="dd3cb-116">Value</span><span class="sxs-lookup"><span data-stu-id="dd3cb-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd3cb-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd3cb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dd3cb-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dd3cb-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dd3cb-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd3cb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="dd3cb-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="dd3cb-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dd3cb-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dd3cb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd3cb-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd3cb-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





