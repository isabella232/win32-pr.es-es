---
title: Mensaje de TB_GETHOTITEM (commctrl. h)
description: Recupera el índice del elemento activo en una barra de herramientas.
ms.assetid: a87dbfc3-c6be-4a0a-9b6a-301b900d7929
keywords:
- TB_GETHOTITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829864cc9223ba15b49b1ecc623f294fd4a6b4fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490193"
---
# <a name="tb_gethotitem-message"></a><span data-ttu-id="d94c9-104">\_Mensaje GETHOTITEM TB</span><span class="sxs-lookup"><span data-stu-id="d94c9-104">TB\_GETHOTITEM message</span></span>

<span data-ttu-id="d94c9-105">Recupera el índice del elemento activo en una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="d94c9-105">Retrieves the index of the hot item in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="d94c9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d94c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d94c9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d94c9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d94c9-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d94c9-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d94c9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d94c9-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d94c9-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d94c9-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d94c9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d94c9-111">Return value</span></span>

<span data-ttu-id="d94c9-112">Devuelve el índice del elemento activo o-1 si no se ha establecido ningún elemento activo.</span><span class="sxs-lookup"><span data-stu-id="d94c9-112">Returns the index of the hot item, or -1 if no hot item is set.</span></span> <span data-ttu-id="d94c9-113">Los controles de barra de herramientas que no tienen el estilo [**\_ plano TBSTYLE**](toolbar-control-and-button-styles.md) no tienen elementos activos.</span><span class="sxs-lookup"><span data-stu-id="d94c9-113">Toolbar controls that do not have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style do not have hot items.</span></span>

## <a name="requirements"></a><span data-ttu-id="d94c9-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d94c9-114">Requirements</span></span>



| <span data-ttu-id="d94c9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d94c9-115">Requirement</span></span> | <span data-ttu-id="d94c9-116">Value</span><span class="sxs-lookup"><span data-stu-id="d94c9-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d94c9-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d94c9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d94c9-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d94c9-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d94c9-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d94c9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d94c9-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d94c9-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d94c9-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d94c9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d94c9-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d94c9-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





