---
title: Mensaje de TTM_GETTITLE (commctrl. h)
description: Recupera información relativa al título de un control ToolTip.
ms.assetid: d8992dd1-1610-44e8-8c0f-8ae1ac4b5898
keywords:
- TTM_GETTITLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_GETTITLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0048925ed3dc267ac07b10b85e2ea1ca1449996c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996410"
---
# <a name="ttm_gettitle-message"></a><span data-ttu-id="f7b90-104">TTM \_ GETTITLE</span><span class="sxs-lookup"><span data-stu-id="f7b90-104">TTM\_GETTITLE message</span></span>

<span data-ttu-id="f7b90-105">Recupera información relativa al título de un control ToolTip.</span><span class="sxs-lookup"><span data-stu-id="f7b90-105">Retrieve information concerning the title of a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f7b90-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f7b90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7b90-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f7b90-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f7b90-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f7b90-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f7b90-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f7b90-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7b90-110">Puntero a una estructura [**TTGETTITLE**](/windows/desktop/api/Commctrl/ns-commctrl-ttgettitle) que contiene información sobre un título de información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="f7b90-110">Pointer to a [**TTGETTITLE**](/windows/desktop/api/Commctrl/ns-commctrl-ttgettitle) structure that contains information about a tooltip title.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7b90-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f7b90-111">Return value</span></span>

<span data-ttu-id="f7b90-112">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="f7b90-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7b90-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f7b90-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f7b90-114">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="f7b90-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="f7b90-115">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f7b90-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f7b90-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7b90-116">Requirements</span></span>



| <span data-ttu-id="f7b90-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7b90-117">Requirement</span></span> | <span data-ttu-id="f7b90-118">Value</span><span class="sxs-lookup"><span data-stu-id="f7b90-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b90-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7b90-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f7b90-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f7b90-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f7b90-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7b90-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f7b90-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f7b90-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f7b90-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f7b90-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7b90-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7b90-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





