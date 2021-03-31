---
title: Mensaje de LVM_CANCELEDITLABEL (commctrl. h)
description: Cancela una operación de edición de texto del elemento.
ms.assetid: 73e9c922-3223-4c49-a33c-df7c09443ccc
keywords:
- LVM_CANCELEDITLABEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_CANCELEDITLABEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edfed26fb3c38d91f7a5b07683079d29ecd4597d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149907"
---
# <a name="lvm_canceleditlabel-message"></a><span data-ttu-id="87a69-104">\_Mensaje CANCELEDITLABEL LVM</span><span class="sxs-lookup"><span data-stu-id="87a69-104">LVM\_CANCELEDITLABEL message</span></span>

<span data-ttu-id="87a69-105">Cancela una operación de edición de texto del elemento.</span><span class="sxs-lookup"><span data-stu-id="87a69-105">Cancels an item text editing operation.</span></span>

## <a name="parameters"></a><span data-ttu-id="87a69-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="87a69-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87a69-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="87a69-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="87a69-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="87a69-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="87a69-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="87a69-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="87a69-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="87a69-110">Must be zero.</span></span></dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87a69-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="87a69-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="87a69-112">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="87a69-112">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="87a69-113">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="87a69-113">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

<span data-ttu-id="87a69-114">Este mensaje hace que se envíe una notificación [ \_ ENDLABELEDIT de LVN](lvn-endlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="87a69-114">This message causes a an [LVN\_ENDLABELEDIT](lvn-endlabeledit.md) notification to be sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="87a69-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87a69-115">Requirements</span></span>



| <span data-ttu-id="87a69-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="87a69-116">Requirement</span></span> | <span data-ttu-id="87a69-117">Value</span><span class="sxs-lookup"><span data-stu-id="87a69-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="87a69-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87a69-118">Minimum supported client</span></span><br/> | <span data-ttu-id="87a69-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="87a69-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="87a69-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87a69-120">Minimum supported server</span></span><br/> | <span data-ttu-id="87a69-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="87a69-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="87a69-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="87a69-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="87a69-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="87a69-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





