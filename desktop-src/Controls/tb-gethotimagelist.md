---
title: Mensaje de TB_GETHOTIMAGELIST (commctrl. h)
description: Recupera la lista de imágenes que usa un control de barra de herramientas para mostrar los botones de acceso rápido.
ms.assetid: 63054449-2768-459c-933c-781d31bdcc15
keywords:
- TB_GETHOTIMAGELIST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e19c1f3989b0d749a9c663d00b5fb7b54d67fc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150402"
---
# <a name="tb_gethotimagelist-message"></a><span data-ttu-id="9c408-104">\_Mensaje GETHOTIMAGELIST TB</span><span class="sxs-lookup"><span data-stu-id="9c408-104">TB\_GETHOTIMAGELIST message</span></span>

<span data-ttu-id="9c408-105">Recupera la lista de imágenes que usa un control de barra de herramientas para mostrar los botones de acceso rápido.</span><span class="sxs-lookup"><span data-stu-id="9c408-105">Retrieves the image list that a toolbar control uses to display hot buttons.</span></span>

## <a name="parameters"></a><span data-ttu-id="9c408-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9c408-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c408-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9c408-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9c408-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="9c408-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9c408-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c408-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9c408-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="9c408-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c408-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c408-111">Return value</span></span>

<span data-ttu-id="9c408-112">Devuelve el identificador de la lista de imágenes que utiliza el control para mostrar los botones de acceso rápido, o **null** si no se ha establecido ninguna lista de imágenes activas.</span><span class="sxs-lookup"><span data-stu-id="9c408-112">Returns the handle to the image list that the control uses to display hot buttons, or **NULL** if no hot image list is set.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c408-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c408-113">Remarks</span></span>

<span data-ttu-id="9c408-114">Un botón está activo cuando el cursor se sitúa sobre él.</span><span class="sxs-lookup"><span data-stu-id="9c408-114">A button is hot when the cursor is over it.</span></span> <span data-ttu-id="9c408-115">Los controles de barra de herramientas deben tener el estilo de [**\_ lista**](toolbar-control-and-button-styles.md) [**TBSTYLE \_ plano**](toolbar-control-and-button-styles.md) o TBSTYLE para tener elementos activos.</span><span class="sxs-lookup"><span data-stu-id="9c408-115">Toolbar controls must have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) or [**TBSTYLE\_LIST**](toolbar-control-and-button-styles.md) style to have hot items.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c408-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c408-116">Requirements</span></span>



| <span data-ttu-id="9c408-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c408-117">Requirement</span></span> | <span data-ttu-id="9c408-118">Value</span><span class="sxs-lookup"><span data-stu-id="9c408-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9c408-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c408-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9c408-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9c408-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9c408-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c408-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9c408-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c408-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9c408-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9c408-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c408-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c408-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





