---
title: Mensaje de BM_SETDONTCLICK (Winuser. h)
description: Establece una marca en un botón de radio que controla la generación de \_ mensajes clics de BN cuando el botón recibe el foco.
ms.assetid: 91d98bce-abea-4afc-a995-0f426ba7a518
keywords:
- BM_SETDONTCLICK controles de mensajes de Windows
topic_type:
- apiref
api_name:
- BM_SETDONTCLICK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8596ec679ff07b87b3433d5b5a7805698f56f84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656494"
---
# <a name="bm_setdontclick-message"></a><span data-ttu-id="a0f2d-104">\_Mensaje SETDONTCLICK de BM</span><span class="sxs-lookup"><span data-stu-id="a0f2d-104">BM\_SETDONTCLICK message</span></span>

<span data-ttu-id="a0f2d-105">Establece una marca en un botón de radio que controla la generación de mensajes [ \_ clics de BN](bn-clicked.md) cuando el botón recibe el foco.</span><span class="sxs-lookup"><span data-stu-id="a0f2d-105">Sets a flag on a radio button that controls the generation of [BN\_CLICKED](bn-clicked.md) messages when the button receives focus.</span></span>

## <a name="parameters"></a><span data-ttu-id="a0f2d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a0f2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0f2d-107">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a0f2d-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f2d-108">Un **booleano** que especifica el estado.</span><span class="sxs-lookup"><span data-stu-id="a0f2d-108">A **BOOL** that specifies the state.</span></span> <span data-ttu-id="a0f2d-109">**True** para establecer la marca; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="a0f2d-109">**TRUE** to set the flag, otherwise **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a0f2d-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a0f2d-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0f2d-111">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="a0f2d-111">Not used.</span></span> <span data-ttu-id="a0f2d-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a0f2d-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0f2d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a0f2d-113">Return value</span></span>

<span data-ttu-id="a0f2d-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a0f2d-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0f2d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0f2d-115">Requirements</span></span>



| <span data-ttu-id="a0f2d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0f2d-116">Requirement</span></span> | <span data-ttu-id="a0f2d-117">Value</span><span class="sxs-lookup"><span data-stu-id="a0f2d-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0f2d-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0f2d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a0f2d-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a0f2d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a0f2d-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0f2d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a0f2d-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a0f2d-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a0f2d-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a0f2d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0f2d-123"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0f2d-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





