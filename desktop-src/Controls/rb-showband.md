---
title: Mensaje de RB_SHOWBAND (commctrl. h)
description: Muestra u oculta una banda determinada en un control rebar.
ms.assetid: 18097aca-e1b4-4359-9d08-4e62406f3f7f
keywords:
- RB_SHOWBAND controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_SHOWBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27c9cedeb42e7eeed9432af9c2a040ac4991810
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151142"
---
# <a name="rb_showband-message"></a><span data-ttu-id="8522a-104">Mensaje de SHOWBAND de RB \_</span><span class="sxs-lookup"><span data-stu-id="8522a-104">RB\_SHOWBAND message</span></span>

<span data-ttu-id="8522a-105">Muestra u oculta una banda determinada en un control rebar.</span><span class="sxs-lookup"><span data-stu-id="8522a-105">Shows or hides a given band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8522a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8522a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8522a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8522a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8522a-108">Índice de base cero de una banda del control rebar.</span><span class="sxs-lookup"><span data-stu-id="8522a-108">Zero-based index of a band in the rebar control.</span></span>

</dd> <dt>

<span data-ttu-id="8522a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8522a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8522a-110">Valor **booleano** que indica si se debe mostrar u ocultar la banda.</span><span class="sxs-lookup"><span data-stu-id="8522a-110">**BOOL** value that indicates if the band should be shown or hidden.</span></span> <span data-ttu-id="8522a-111">Si este valor es distinto de cero, se mostrará la banda.</span><span class="sxs-lookup"><span data-stu-id="8522a-111">If this value is nonzero, the band will be shown.</span></span> <span data-ttu-id="8522a-112">De lo contrario, se ocultará la banda.</span><span class="sxs-lookup"><span data-stu-id="8522a-112">Otherwise, the band will be hidden.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8522a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8522a-113">Return value</span></span>

<span data-ttu-id="8522a-114">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="8522a-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8522a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8522a-115">Requirements</span></span>



| <span data-ttu-id="8522a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8522a-116">Requirement</span></span> | <span data-ttu-id="8522a-117">Value</span><span class="sxs-lookup"><span data-stu-id="8522a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8522a-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8522a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8522a-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8522a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8522a-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8522a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8522a-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8522a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8522a-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8522a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8522a-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8522a-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





