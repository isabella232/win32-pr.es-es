---
title: Mensaje de TB_GETSTYLE (commctrl. h)
description: Recupera los estilos actualmente en uso para un control de barra de herramientas.
ms.assetid: 6fbe8733-79df-462e-acb6-6568105e5058
keywords:
- TB_GETSTYLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14f8de0addae729a4a8c641d21fd1771137d8c8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492130"
---
# <a name="tb_getstyle-message"></a><span data-ttu-id="6f846-104">\_Mensaje GETSTYLE de TB</span><span class="sxs-lookup"><span data-stu-id="6f846-104">TB\_GETSTYLE message</span></span>

<span data-ttu-id="6f846-105">Recupera los estilos actualmente en uso para un control de barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="6f846-105">Retrieves the styles currently in use for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6f846-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f846-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f846-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6f846-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6f846-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="6f846-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6f846-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6f846-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6f846-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="6f846-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f846-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f846-111">Return value</span></span>

<span data-ttu-id="6f846-112">Devuelve un valor **DWORD** que es una combinación de [estilos de control de barra de herramientas](toolbar-control-and-button-styles.md).</span><span class="sxs-lookup"><span data-stu-id="6f846-112">Returns a **DWORD** value that is a combination of [toolbar control styles](toolbar-control-and-button-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f846-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f846-113">Requirements</span></span>



| <span data-ttu-id="6f846-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f846-114">Requirement</span></span> | <span data-ttu-id="6f846-115">Value</span><span class="sxs-lookup"><span data-stu-id="6f846-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6f846-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f846-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6f846-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6f846-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6f846-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f846-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6f846-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6f846-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6f846-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f846-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f846-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f846-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





