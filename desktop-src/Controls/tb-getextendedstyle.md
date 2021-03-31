---
title: Mensaje de TB_GETEXTENDEDSTYLE (commctrl. h)
description: Recupera los estilos extendidos para un control de barra de herramientas.
ms.assetid: d9e31a8e-5e5a-4d2d-bc3b-65ac40e8592f
keywords:
- TB_GETEXTENDEDSTYLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80bc4f4ad45e5c1c75366e0890f3fd76ec1fa74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802059"
---
# <a name="tb_getextendedstyle-message"></a><span data-ttu-id="47a50-104">\_Mensaje GETEXTENDEDSTYLE TB</span><span class="sxs-lookup"><span data-stu-id="47a50-104">TB\_GETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="47a50-105">Recupera los estilos extendidos para un control de barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="47a50-105">Retrieves the extended styles for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="47a50-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47a50-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47a50-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="47a50-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="47a50-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="47a50-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="47a50-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="47a50-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="47a50-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="47a50-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47a50-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="47a50-111">Return value</span></span>

<span data-ttu-id="47a50-112">Devuelve un **valor DWORD** que representa los estilos actualmente en uso para el control Toolbar.</span><span class="sxs-lookup"><span data-stu-id="47a50-112">Returns a **DWORD** that represents the styles currently in use for the toolbar control.</span></span> <span data-ttu-id="47a50-113">Este valor puede ser una combinación de [estilos extendidos](toolbar-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="47a50-113">This value can be a combination of [extended styles](toolbar-extended-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="47a50-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47a50-114">Requirements</span></span>



| <span data-ttu-id="47a50-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="47a50-115">Requirement</span></span> | <span data-ttu-id="47a50-116">Value</span><span class="sxs-lookup"><span data-stu-id="47a50-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="47a50-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47a50-117">Minimum supported client</span></span><br/> | <span data-ttu-id="47a50-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="47a50-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="47a50-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47a50-119">Minimum supported server</span></span><br/> | <span data-ttu-id="47a50-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="47a50-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="47a50-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="47a50-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="47a50-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="47a50-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47a50-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="47a50-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47a50-124">**TB \_ SETEXTENDEDSTYLE**</span><span class="sxs-lookup"><span data-stu-id="47a50-124">**TB\_SETEXTENDEDSTYLE**</span></span>](tb-setextendedstyle.md)
</dt> </dl>

 

 





