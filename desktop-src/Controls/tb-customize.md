---
title: Mensaje de TB_CUSTOMIZE (commctrl. h)
description: Muestra el cuadro de diálogo Personalizar barra de herramientas.
ms.assetid: 45249467-d585-4ffd-8bbe-e39739059c40
keywords:
- TB_CUSTOMIZE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_CUSTOMIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dada0ef195e898b7a46487a2d775e46d6af854ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658404"
---
# <a name="tb_customize-message"></a><span data-ttu-id="52e49-104">TB \_ personalizar mensaje</span><span class="sxs-lookup"><span data-stu-id="52e49-104">TB\_CUSTOMIZE message</span></span>

<span data-ttu-id="52e49-105">Muestra el cuadro de diálogo **personalizar barra de herramientas** .</span><span class="sxs-lookup"><span data-stu-id="52e49-105">Displays the **Customize Toolbar** dialog box.</span></span>

## <a name="parameters"></a><span data-ttu-id="52e49-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="52e49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52e49-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="52e49-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52e49-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="52e49-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="52e49-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="52e49-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52e49-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="52e49-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52e49-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="52e49-111">Return value</span></span>

<span data-ttu-id="52e49-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="52e49-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="52e49-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52e49-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="52e49-114">La barra de herramientas debe controlar las notificaciones [TBN \_ QUERYINSERT](tbn-queryinsert.md) y [TBN \_ QUERYDELETE](tbn-querydelete.md) para que aparezca el cuadro de diálogo **personalizar barra de herramientas** .</span><span class="sxs-lookup"><span data-stu-id="52e49-114">The toolbar must handle the [TBN\_QUERYINSERT](tbn-queryinsert.md) and [TBN\_QUERYDELETE](tbn-querydelete.md) notifications for the **Customize Toolbar** dialog box to appear.</span></span> <span data-ttu-id="52e49-115">Si la barra de herramientas no controla esas notificaciones, la **\_ Personalización de TB** no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="52e49-115">If the toolbar does not handle those notifications, **TB\_CUSTOMIZE** has no effect.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="52e49-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52e49-116">Requirements</span></span>



| <span data-ttu-id="52e49-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="52e49-117">Requirement</span></span> | <span data-ttu-id="52e49-118">Value</span><span class="sxs-lookup"><span data-stu-id="52e49-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52e49-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52e49-119">Minimum supported client</span></span><br/> | <span data-ttu-id="52e49-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="52e49-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="52e49-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52e49-121">Minimum supported server</span></span><br/> | <span data-ttu-id="52e49-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="52e49-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="52e49-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52e49-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="52e49-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="52e49-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





