---
title: Mensaje de LVM_GETHEADER (commctrl. h)
description: Obtiene el identificador del control de encabezado utilizado por el control de vista de lista. Puede enviar este mensaje explícitamente o usar la macro de ListView \_ GetHeader.
ms.assetid: 4708b493-4449-4844-bf0d-e6969bcf0246
keywords:
- LVM_GETHEADER controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETHEADER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d53082092118cad373005743849498791f0e1ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078940"
---
# <a name="lvm_getheader-message"></a><span data-ttu-id="05297-105">Mensaje de LVM \_ GETHEADER</span><span class="sxs-lookup"><span data-stu-id="05297-105">LVM\_GETHEADER message</span></span>

<span data-ttu-id="05297-106">Obtiene el identificador del control de encabezado utilizado por el control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="05297-106">Gets the handle to the header control used by the list-view control.</span></span> <span data-ttu-id="05297-107">Puede enviar este mensaje explícitamente o usar la macro de [**ListView \_ GetHeader**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getheader) .</span><span class="sxs-lookup"><span data-stu-id="05297-107">You can send this message explicitly or use the [**ListView\_GetHeader**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getheader) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="05297-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="05297-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05297-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="05297-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="05297-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="05297-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="05297-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="05297-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="05297-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="05297-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05297-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="05297-113">Return value</span></span>

<span data-ttu-id="05297-114">Devuelve el identificador del control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="05297-114">Returns the handle to the header control.</span></span>

## <a name="requirements"></a><span data-ttu-id="05297-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05297-115">Requirements</span></span>



| <span data-ttu-id="05297-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="05297-116">Requirement</span></span> | <span data-ttu-id="05297-117">Value</span><span class="sxs-lookup"><span data-stu-id="05297-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="05297-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05297-118">Minimum supported client</span></span><br/> | <span data-ttu-id="05297-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="05297-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="05297-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05297-120">Minimum supported server</span></span><br/> | <span data-ttu-id="05297-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="05297-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="05297-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="05297-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="05297-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="05297-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





