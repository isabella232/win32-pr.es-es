---
title: Mensaje de TB_SETHOTITEM (commctrl. h)
description: Establece el elemento activo en una barra de herramientas.
ms.assetid: 15005741-29d2-48c6-b5f0-15178a49b917
keywords:
- TB_SETHOTITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c477a445cb6aae78dd5d31e8d23b8ec3be8c61ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905448"
---
# <a name="tb_sethotitem-message"></a><span data-ttu-id="2a272-104">\_Mensaje SETHOTITEM TB</span><span class="sxs-lookup"><span data-stu-id="2a272-104">TB\_SETHOTITEM message</span></span>

<span data-ttu-id="2a272-105">Establece el elemento activo en una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="2a272-105">Sets the hot item in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="2a272-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2a272-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a272-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2a272-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a272-108">Índice del elemento que se hará activo.</span><span class="sxs-lookup"><span data-stu-id="2a272-108">Index of the item that will be made hot.</span></span> <span data-ttu-id="2a272-109">Si este valor es-1, ninguno de los elementos estará activo.</span><span class="sxs-lookup"><span data-stu-id="2a272-109">If this value is -1, none of the items will be hot.</span></span>

</dd> <dt>

<span data-ttu-id="2a272-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a272-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2a272-111">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2a272-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a272-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2a272-112">Return value</span></span>

<span data-ttu-id="2a272-113">Devuelve el índice del elemento activo anterior, o-1 si no hay ningún elemento activo.</span><span class="sxs-lookup"><span data-stu-id="2a272-113">Returns the index of the previous hot item, or -1 if there was no hot item.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a272-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a272-114">Remarks</span></span>

<span data-ttu-id="2a272-115">El comportamiento de este mensaje no está definido para las barras de herramientas que no tienen el estilo [**\_ plano TBSTYLE**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="2a272-115">The behavior of this message is not defined for toolbars that do not have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a272-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a272-116">Requirements</span></span>



| <span data-ttu-id="2a272-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a272-117">Requirement</span></span> | <span data-ttu-id="2a272-118">Value</span><span class="sxs-lookup"><span data-stu-id="2a272-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a272-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a272-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2a272-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2a272-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2a272-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a272-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2a272-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2a272-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2a272-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2a272-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a272-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a272-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





