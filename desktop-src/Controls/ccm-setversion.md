---
title: Mensaje de CCM_SETVERSION (commctrl. h)
description: Este mensaje se utiliza para informar al control de que está esperando un comportamiento asociado a una versión determinada.
ms.assetid: f87b20bc-0139-4d0a-b38c-32c75743d6f6
keywords:
- CCM_SETVERSION controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CCM_SETVERSION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 349935173c41cd9c90a016ef3d2f3c77df8f159c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079534"
---
# <a name="ccm_setversion-message"></a><span data-ttu-id="be54b-104">\_Mensaje SETVERSION de CCM</span><span class="sxs-lookup"><span data-stu-id="be54b-104">CCM\_SETVERSION message</span></span>

<span data-ttu-id="be54b-105">Este mensaje se utiliza para informar al control de que está esperando un comportamiento asociado a una versión determinada.</span><span class="sxs-lookup"><span data-stu-id="be54b-105">This message is used to inform the control that you are expecting a behavior associated with a particular version.</span></span>

## <a name="parameters"></a><span data-ttu-id="be54b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="be54b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be54b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="be54b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be54b-108">El número de versión.</span><span class="sxs-lookup"><span data-stu-id="be54b-108">The version number.</span></span>

</dd> <dt>

<span data-ttu-id="be54b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="be54b-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="be54b-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="be54b-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be54b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be54b-111">Return value</span></span>

<span data-ttu-id="be54b-112">Devuelve la versión especificada en el mensaje **\_ SETVERSION de CCM** anterior.</span><span class="sxs-lookup"><span data-stu-id="be54b-112">Returns the version specified in the previous **CCM\_SETVERSION** message.</span></span> <span data-ttu-id="be54b-113">Si *wParam* se establece en un valor mayor que la versión del archivo dll actual, devuelve-1.</span><span class="sxs-lookup"><span data-stu-id="be54b-113">If *wParam* is set to a value greater than the current DLL version, it returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="be54b-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="be54b-114">Remarks</span></span>

<span data-ttu-id="be54b-115">En algunos casos, es posible que un control se comporte de forma diferente, dependiendo de la versión.</span><span class="sxs-lookup"><span data-stu-id="be54b-115">In a few cases, a control may behave differently, depending on the version.</span></span> <span data-ttu-id="be54b-116">Esto se aplica principalmente a errores corregidos en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="be54b-116">This primarily applies to bugs that were fixed in later versions.</span></span> <span data-ttu-id="be54b-117">El **mensaje \_ SETVERSION de CCM** le permite informar al control del comportamiento que se espera.</span><span class="sxs-lookup"><span data-stu-id="be54b-117">The **CCM\_SETVERSION** message enables you to inform the control which behavior is expected.</span></span> <span data-ttu-id="be54b-118">Puede determinar qué versión ha especificado mediante el envío de un mensaje de [**\_ GETVERSION de CCM**](ccm-getversion.md) .</span><span class="sxs-lookup"><span data-stu-id="be54b-118">You can determine which version you have specified by sending a [**CCM\_GETVERSION**](ccm-getversion.md) message.</span></span> <span data-ttu-id="be54b-119">Para obtener un ejemplo de cómo usar este mensaje, vea [dibujo personalizado con controles de List-View y Tree-View](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="be54b-119">For an example of how to use this message, see [Custom Draw With List-View and Tree-View Controls](custom-draw.md).</span></span>

<span data-ttu-id="be54b-120">Si tiene instalada la versión 6 de ComCtl32.dll, independientemente del valor que establezca en *wParam*, el **mensaje \_ SETVERSION de CCM** devuelve la versión 6.</span><span class="sxs-lookup"><span data-stu-id="be54b-120">If you have ComCtl32.dll version 6 installed, regardless of what value you set in *wParam*, the **CCM\_SETVERSION** message returns version 6.</span></span>

> [!Note]  
> <span data-ttu-id="be54b-121">Este mensaje solo establece el número de versión del control al que se envía.</span><span class="sxs-lookup"><span data-stu-id="be54b-121">This message only sets the version number for the control to which it is sent.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="be54b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be54b-122">Requirements</span></span>



| <span data-ttu-id="be54b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="be54b-123">Requirement</span></span> | <span data-ttu-id="be54b-124">Value</span><span class="sxs-lookup"><span data-stu-id="be54b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="be54b-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be54b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="be54b-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="be54b-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="be54b-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be54b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="be54b-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="be54b-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="be54b-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="be54b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="be54b-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="be54b-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





