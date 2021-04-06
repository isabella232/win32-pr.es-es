---
title: Mensaje de TB_SETHOTITEM2 (commctrl. h)
description: Establece el elemento activo en una barra de herramientas.
ms.assetid: 43666b1d-1197-452f-aa79-eb0a1a23e5b7
keywords:
- TB_SETHOTITEM2 controles de mensajes de Windows
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
ms.openlocfilehash: 7027920e4363b46fcc0b6d9b0d87129e01843318
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803139"
---
# <a name="tb_sethotitem2-message"></a><span data-ttu-id="6ebe5-104">\_Mensaje SETHOTITEM2 TB</span><span class="sxs-lookup"><span data-stu-id="6ebe5-104">TB\_SETHOTITEM2 message</span></span>

<span data-ttu-id="6ebe5-105">Establece el elemento activo en una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="6ebe5-105">Sets the hot item in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="6ebe5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ebe5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ebe5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6ebe5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6ebe5-108">Índice del elemento que se hará activo.</span><span class="sxs-lookup"><span data-stu-id="6ebe5-108">Index of the item that will be made hot.</span></span> <span data-ttu-id="6ebe5-109">Si este valor es-1, ninguno de los elementos estará activo.</span><span class="sxs-lookup"><span data-stu-id="6ebe5-109">If this value is -1, none of the items will be hot.</span></span>

</dd> <dt>

<span data-ttu-id="6ebe5-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6ebe5-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6ebe5-111">Combinación de marcas HICF \_ xxx.</span><span class="sxs-lookup"><span data-stu-id="6ebe5-111">A combination of HICF\_xxx flags.</span></span> <span data-ttu-id="6ebe5-112">Vea <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**NMTBHOTITEM**</a>.</span><span class="sxs-lookup"><span data-stu-id="6ebe5-112">See <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**NMTBHOTITEM**</a>.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ebe5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ebe5-113">Return value</span></span>

<span data-ttu-id="6ebe5-114">Devuelve el índice del elemento activo anterior, o-1 si no hay ningún elemento activo.</span><span class="sxs-lookup"><span data-stu-id="6ebe5-114">Returns the index of the previous hot item, or -1 if there was no hot item.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ebe5-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ebe5-115">Remarks</span></span>

<span data-ttu-id="6ebe5-116">El comportamiento de este mensaje no está definido para las barras de herramientas que no tienen el estilo [**\_ plano TBSTYLE**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="6ebe5-116">The behavior of this message is not defined for toolbars that do not have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ebe5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ebe5-117">Requirements</span></span>



| <span data-ttu-id="6ebe5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ebe5-118">Requirement</span></span> | <span data-ttu-id="6ebe5-119">Value</span><span class="sxs-lookup"><span data-stu-id="6ebe5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6ebe5-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ebe5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6ebe5-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6ebe5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6ebe5-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ebe5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6ebe5-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6ebe5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6ebe5-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ebe5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ebe5-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ebe5-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





