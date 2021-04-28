---
title: TB_SETHOTITEM2 mensaje (Commctrl.h)
description: 'TB_SETHOTITEM2 mensaje: establece el elemento de acceso rápido en una barra de herramientas.'
ms.assetid: 43666b1d-1197-452f-aa79-eb0a1a23e5b7
keywords:
- TB_SETHOTITEM2 mensaje Controles de Windows
topic_type:
- apiref
api_name:
- TB_SETHOTITEM2
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7daf67839837adccfbec99bf03fc4dfff97738db
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104143"
---
# <a name="tb_sethotitem2-message"></a><span data-ttu-id="be640-104">Mensaje \_ SETHOTITEM2 de TB</span><span class="sxs-lookup"><span data-stu-id="be640-104">TB\_SETHOTITEM2 message</span></span>

<span data-ttu-id="be640-105">Establece el elemento de acceso rápido en una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="be640-105">Sets the hot item in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="be640-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="be640-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be640-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="be640-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be640-108">Índice del elemento que se hará en caliente.</span><span class="sxs-lookup"><span data-stu-id="be640-108">Index of the item that will be made hot.</span></span> <span data-ttu-id="be640-109">Si este valor es -1, ninguno de los elementos estará en caliente.</span><span class="sxs-lookup"><span data-stu-id="be640-109">If this value is -1, none of the items will be hot.</span></span>

</dd> <dt>

<span data-ttu-id="be640-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="be640-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="be640-111">Combinación de marcas XXX \_ de HICF.</span><span class="sxs-lookup"><span data-stu-id="be640-111">A combination of HICF\_xxx flags.</span></span> <span data-ttu-id="be640-112">Vea <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**NMTBHOTITEM.**</a></span><span class="sxs-lookup"><span data-stu-id="be640-112">See <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**NMTBHOTITEM**</a>.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be640-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be640-113">Return value</span></span>

<span data-ttu-id="be640-114">Devuelve el índice del elemento de acceso actual anterior o -1 si no había ningún elemento de acceso.</span><span class="sxs-lookup"><span data-stu-id="be640-114">Returns the index of the previous hot item, or -1 if there was no hot item.</span></span>

## <a name="remarks"></a><span data-ttu-id="be640-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="be640-115">Remarks</span></span>

<span data-ttu-id="be640-116">El comportamiento de este mensaje no está definido para las barras de herramientas que no tienen el [**estilo TBSTYLE \_ FLAT.**](toolbar-control-and-button-styles.md)</span><span class="sxs-lookup"><span data-stu-id="be640-116">The behavior of this message is not defined for toolbars that do not have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="be640-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be640-117">Requirements</span></span>



| <span data-ttu-id="be640-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="be640-118">Requirement</span></span> | <span data-ttu-id="be640-119">Valor</span><span class="sxs-lookup"><span data-stu-id="be640-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="be640-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be640-120">Minimum supported client</span></span><br/> | <span data-ttu-id="be640-121">Solo aplicaciones de escritorio de Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="be640-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="be640-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be640-122">Minimum supported server</span></span><br/> | <span data-ttu-id="be640-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="be640-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="be640-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="be640-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="be640-125"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="be640-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





