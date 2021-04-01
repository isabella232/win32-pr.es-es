---
title: Mensaje de TB_SETEXTENDEDSTYLE (commctrl. h)
description: Establece los estilos extendidos para un control de barra de herramientas.
ms.assetid: aec64bc7-74b4-4efc-9864-2c8a9fbd35c2
keywords:
- TB_SETEXTENDEDSTYLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a540aaeff61bd81b649f0509e064a29282f598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150739"
---
# <a name="tb_setextendedstyle-message"></a><span data-ttu-id="f7db9-104">\_Mensaje SETEXTENDEDSTYLE TB</span><span class="sxs-lookup"><span data-stu-id="f7db9-104">TB\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="f7db9-105">Establece los estilos extendidos para un control de barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="f7db9-105">Sets the extended styles for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f7db9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f7db9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7db9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f7db9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f7db9-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f7db9-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f7db9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f7db9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7db9-110">Valor que especifica los nuevos estilos extendidos.</span><span class="sxs-lookup"><span data-stu-id="f7db9-110">Value specifying the new extended styles.</span></span> <span data-ttu-id="f7db9-111">Este parámetro puede ser una combinación de [estilos extendidos](toolbar-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="f7db9-111">This parameter can be a combination of [extended styles](toolbar-extended-styles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7db9-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f7db9-112">Return value</span></span>

<span data-ttu-id="f7db9-113">Devuelve un **valor DWORD** que representa los estilos extendidos anteriores.</span><span class="sxs-lookup"><span data-stu-id="f7db9-113">Returns a **DWORD** that represents the previous extended styles.</span></span> <span data-ttu-id="f7db9-114">Este valor puede ser una combinación de [estilos extendidos](toolbar-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="f7db9-114">This value can be a combination of [extended styles](toolbar-extended-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f7db9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7db9-115">Requirements</span></span>



| <span data-ttu-id="f7db9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7db9-116">Requirement</span></span> | <span data-ttu-id="f7db9-117">Value</span><span class="sxs-lookup"><span data-stu-id="f7db9-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f7db9-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7db9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f7db9-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f7db9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f7db9-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7db9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f7db9-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f7db9-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f7db9-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f7db9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7db9-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7db9-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7db9-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7db9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7db9-125">**TB \_ GETEXTENDEDSTYLE**</span><span class="sxs-lookup"><span data-stu-id="f7db9-125">**TB\_GETEXTENDEDSTYLE**</span></span>](tb-getextendedstyle.md)
</dt> </dl>

 

 





