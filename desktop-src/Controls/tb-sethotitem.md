---
title: TB_SETHOTITEM mensaje (Commctrl.h)
description: 'TB_SETHOTITEM mensaje: establece el elemento de acceso rápido en una barra de herramientas.'
ms.assetid: 15005741-29d2-48c6-b5f0-15178a49b917
keywords:
- TB_SETHOTITEM mensaje Controles de Windows
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
ms.openlocfilehash: a90e5b38675d33a361857c4303fa2a89f22cff29
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104183"
---
# <a name="tb_sethotitem-message"></a><span data-ttu-id="5f4a3-104">Mensaje \_ SETHOTITEM de TB</span><span class="sxs-lookup"><span data-stu-id="5f4a3-104">TB\_SETHOTITEM message</span></span>

<span data-ttu-id="5f4a3-105">Establece el elemento de acceso rápido en una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="5f4a3-105">Sets the hot item in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="5f4a3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f4a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f4a3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5f4a3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f4a3-108">Índice del elemento que se hará en caliente.</span><span class="sxs-lookup"><span data-stu-id="5f4a3-108">Index of the item that will be made hot.</span></span> <span data-ttu-id="5f4a3-109">Si este valor es -1, ninguno de los elementos estará en caliente.</span><span class="sxs-lookup"><span data-stu-id="5f4a3-109">If this value is -1, none of the items will be hot.</span></span>

</dd> <dt>

<span data-ttu-id="5f4a3-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f4a3-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5f4a3-111">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5f4a3-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f4a3-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f4a3-112">Return value</span></span>

<span data-ttu-id="5f4a3-113">Devuelve el índice del elemento de acceso actual anterior o -1 si no había ningún elemento de acceso.</span><span class="sxs-lookup"><span data-stu-id="5f4a3-113">Returns the index of the previous hot item, or -1 if there was no hot item.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f4a3-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5f4a3-114">Remarks</span></span>

<span data-ttu-id="5f4a3-115">El comportamiento de este mensaje no está definido para las barras de herramientas que no tienen el [**estilo TBSTYLE \_ FLAT.**](toolbar-control-and-button-styles.md)</span><span class="sxs-lookup"><span data-stu-id="5f4a3-115">The behavior of this message is not defined for toolbars that do not have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f4a3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f4a3-116">Requirements</span></span>



| <span data-ttu-id="5f4a3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f4a3-117">Requirement</span></span> | <span data-ttu-id="5f4a3-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5f4a3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f4a3-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f4a3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5f4a3-120">Solo aplicaciones de escritorio de Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="5f4a3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5f4a3-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f4a3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5f4a3-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5f4a3-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5f4a3-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f4a3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f4a3-124"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="5f4a3-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





