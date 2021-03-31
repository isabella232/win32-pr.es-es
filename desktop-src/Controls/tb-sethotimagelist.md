---
title: Mensaje de TB_SETHOTIMAGELIST (commctrl. h)
description: Establece la lista de imágenes que utilizará el control de barra de herramientas para mostrar los botones de acceso rápido.
ms.assetid: 3c29cdde-bd57-4194-984f-220dbf963733
keywords:
- TB_SETHOTIMAGELIST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a84c3420eaf64710ac1f8764db20d2cfc88b7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996800"
---
# <a name="tb_sethotimagelist-message"></a><span data-ttu-id="a0589-104">\_Mensaje SETHOTIMAGELIST TB</span><span class="sxs-lookup"><span data-stu-id="a0589-104">TB\_SETHOTIMAGELIST message</span></span>

<span data-ttu-id="a0589-105">Establece la lista de imágenes que utilizará el control de barra de herramientas para mostrar los botones de acceso rápido.</span><span class="sxs-lookup"><span data-stu-id="a0589-105">Sets the image list that the toolbar control will use to display hot buttons.</span></span>

## <a name="parameters"></a><span data-ttu-id="a0589-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a0589-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0589-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a0589-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a0589-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a0589-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a0589-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a0589-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0589-110">Identificador de la lista de imágenes que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="a0589-110">Handle to the image list that will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0589-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a0589-111">Return value</span></span>

<span data-ttu-id="a0589-112">Devuelve el identificador de la lista de imágenes utilizada previamente para mostrar los botones de acceso rápido, o **null** si no se ha establecido previamente ninguna lista de imágenes.</span><span class="sxs-lookup"><span data-stu-id="a0589-112">Returns the handle to the image list previously used to display hot buttons, or **NULL** if no image list was previously set.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0589-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a0589-113">Remarks</span></span>

<span data-ttu-id="a0589-114">Un botón está activo cuando el cursor se sitúa sobre él.</span><span class="sxs-lookup"><span data-stu-id="a0589-114">A button is hot when the cursor is over it.</span></span> <span data-ttu-id="a0589-115">Los controles de barra de herramientas deben tener el estilo de [**\_ lista**](toolbar-control-and-button-styles.md) [**TBSTYLE \_ plano**](toolbar-control-and-button-styles.md) o TBSTYLE para tener elementos activos.</span><span class="sxs-lookup"><span data-stu-id="a0589-115">Toolbar controls must have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) or [**TBSTYLE\_LIST**](toolbar-control-and-button-styles.md) style to have hot items.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0589-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0589-116">Requirements</span></span>



| <span data-ttu-id="a0589-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0589-117">Requirement</span></span> | <span data-ttu-id="a0589-118">Value</span><span class="sxs-lookup"><span data-stu-id="a0589-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0589-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0589-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a0589-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a0589-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a0589-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0589-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a0589-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a0589-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a0589-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a0589-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0589-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0589-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





