---
title: Mensaje de SB_GETICON (commctrl. h)
description: Recupera el icono de un elemento en una barra de estado.
ms.assetid: f99508e3-afa8-48fd-b87a-fce41c4410ff
keywords:
- SB_GETICON controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SB_GETICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab86809df54d796b8e83f05f2a2b9041450ce2fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905459"
---
# <a name="sb_geticon-message"></a><span data-ttu-id="892be-104">\_Mensaje GETICON de SB</span><span class="sxs-lookup"><span data-stu-id="892be-104">SB\_GETICON message</span></span>

<span data-ttu-id="892be-105">Recupera el icono de un elemento en una barra de estado.</span><span class="sxs-lookup"><span data-stu-id="892be-105">Retrieves the icon for a part in a status bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="892be-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="892be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="892be-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="892be-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="892be-108">Índice de base cero del elemento que contiene el icono que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="892be-108">Zero-based index of the part that contains the icon to be retrieved.</span></span> <span data-ttu-id="892be-109">Si este parámetro es-1, se supone que la barra de estado es una barra de estado de [modo simple](status-bars.md) .</span><span class="sxs-lookup"><span data-stu-id="892be-109">If this parameter is -1, the status bar is assumed to be a [Simple Mode](status-bars.md) status bar.</span></span>

</dd> <dt>

<span data-ttu-id="892be-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="892be-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="892be-111">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="892be-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="892be-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="892be-112">Return value</span></span>

<span data-ttu-id="892be-113">Devuelve el identificador del icono si se realiza correctamente o **null** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="892be-113">Returns the handle to the icon if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="892be-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="892be-114">Requirements</span></span>



| <span data-ttu-id="892be-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="892be-115">Requirement</span></span> | <span data-ttu-id="892be-116">Value</span><span class="sxs-lookup"><span data-stu-id="892be-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="892be-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="892be-117">Minimum supported client</span></span><br/> | <span data-ttu-id="892be-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="892be-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="892be-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="892be-119">Minimum supported server</span></span><br/> | <span data-ttu-id="892be-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="892be-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="892be-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="892be-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="892be-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="892be-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





