---
title: Mensaje de TB_SETLISTGAP (commctrl. h)
description: Establece la distancia entre los botones de la barra de herramientas en una barra de herramientas concreta.
ms.assetid: ca8ba6e4-cf70-41ca-ac61-cd13671d4010
keywords:
- TB_SETLISTGAP controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETLISTGAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 224a709b7beefcfdf49ea7838f905977487aca8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103904984"
---
# <a name="tb_setlistgap-message"></a><span data-ttu-id="f700d-104">\_Mensaje SETLISTGAP TB</span><span class="sxs-lookup"><span data-stu-id="f700d-104">TB\_SETLISTGAP message</span></span>

<span data-ttu-id="f700d-105">Establece la distancia entre los botones de la barra de herramientas en una barra de herramientas concreta.</span><span class="sxs-lookup"><span data-stu-id="f700d-105">Sets the distance between the toolbar buttons on a specific toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="f700d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f700d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f700d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f700d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f700d-108">Espacio, en píxeles, entre los botones de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="f700d-108">The gap, in pixels, between buttons on the toolbar.</span></span>

</dd> <dt>

<span data-ttu-id="f700d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f700d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f700d-110">ignorado.</span><span class="sxs-lookup"><span data-stu-id="f700d-110">Ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f700d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f700d-111">Return value</span></span>

<span data-ttu-id="f700d-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f700d-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f700d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f700d-113">Remarks</span></span>

<span data-ttu-id="f700d-114">El intervalo entre los botones solo se aplica a la ventana de control de la barra de herramientas que recibe este mensaje.</span><span class="sxs-lookup"><span data-stu-id="f700d-114">The gap between buttons only applies to the toolbar control window that receives this message.</span></span> <span data-ttu-id="f700d-115">La recepción de este mensaje desencadena un reenvío de la barra de herramientas, si la barra de herramientas está visible actualmente.</span><span class="sxs-lookup"><span data-stu-id="f700d-115">Receipt of this message triggers a repaint of the toolbar, if the toolbar is currently visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="f700d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f700d-116">Requirements</span></span>



| <span data-ttu-id="f700d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f700d-117">Requirement</span></span> | <span data-ttu-id="f700d-118">Value</span><span class="sxs-lookup"><span data-stu-id="f700d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f700d-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f700d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f700d-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f700d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f700d-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f700d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f700d-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f700d-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f700d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f700d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f700d-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f700d-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





