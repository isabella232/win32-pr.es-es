---
title: Mensaje de PBM_SETBKCOLOR (commctrl. h)
description: Establece el color de fondo de la barra de progreso.
ms.assetid: e28af958-babb-4c2e-9202-89b608c22f8e
keywords:
- PBM_SETBKCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PBM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ddfaf84695221cf998275d76a9d2d67773150da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803055"
---
# <a name="pbm_setbkcolor-message"></a><span data-ttu-id="ce3fc-104">Mensaje de SETBKCOLOR de PBM \_</span><span class="sxs-lookup"><span data-stu-id="ce3fc-104">PBM\_SETBKCOLOR message</span></span>

<span data-ttu-id="ce3fc-105">Establece el color de fondo de la barra de progreso.</span><span class="sxs-lookup"><span data-stu-id="ce3fc-105">Sets the background color in the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="ce3fc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce3fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce3fc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ce3fc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce3fc-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ce3fc-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ce3fc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce3fc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce3fc-110">Valor **COLORREF** que especifica el nuevo color de fondo.</span><span class="sxs-lookup"><span data-stu-id="ce3fc-110">**COLORREF** value that specifies the new background color.</span></span> <span data-ttu-id="ce3fc-111">Especifique el \_ valor predeterminado de CLR para que la barra de progreso use su color de fondo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ce3fc-111">Specify the CLR\_DEFAULT value to cause the progress bar to use its default background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce3fc-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce3fc-112">Return value</span></span>

<span data-ttu-id="ce3fc-113">Devuelve el color de fondo anterior, o el \_ valor predeterminado de CLR si el color de fondo es el color predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ce3fc-113">Returns the previous background color, or CLR\_DEFAULT if the background color is the default color.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce3fc-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ce3fc-114">Remarks</span></span>

<span data-ttu-id="ce3fc-115">Cuando los estilos visuales están habilitados, este mensaje no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="ce3fc-115">When visual styles are enabled, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce3fc-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce3fc-116">Requirements</span></span>



| <span data-ttu-id="ce3fc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce3fc-117">Requirement</span></span> | <span data-ttu-id="ce3fc-118">Value</span><span class="sxs-lookup"><span data-stu-id="ce3fc-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce3fc-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce3fc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ce3fc-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ce3fc-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ce3fc-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce3fc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ce3fc-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ce3fc-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ce3fc-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ce3fc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce3fc-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce3fc-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





