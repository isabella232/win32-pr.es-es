---
title: Mensaje de TTM_WINDOWFROMPOINT (commctrl. h)
description: Permite que un procedimiento de subclase provoque que una información sobre herramientas muestre texto para una ventana distinta de la que se encuentra debajo del cursor del mouse.
ms.assetid: f3bf6917-1745-4e4f-a9c1-8fe86b2b3906
keywords:
- TTM_WINDOWFROMPOINT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_WINDOWFROMPOINT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68679f6b6c2477a8279c22f11d0d300e44c8370d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802845"
---
# <a name="ttm_windowfrompoint-message"></a><span data-ttu-id="99e84-104">TTM \_ WINDOWFROMPOINT</span><span class="sxs-lookup"><span data-stu-id="99e84-104">TTM\_WINDOWFROMPOINT message</span></span>

<span data-ttu-id="99e84-105">Permite que un procedimiento de subclase provoque que una información sobre herramientas muestre texto para una ventana distinta de la que se encuentra debajo del cursor del mouse.</span><span class="sxs-lookup"><span data-stu-id="99e84-105">Allows a subclass procedure to cause a tooltip to display text for a window other than the one beneath the mouse cursor.</span></span>

## <a name="parameters"></a><span data-ttu-id="99e84-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="99e84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99e84-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="99e84-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="99e84-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="99e84-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="99e84-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="99e84-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99e84-110">Puntero a una estructura de [**punto**](/previous-versions//dd162805(v=vs.85)) que define el punto que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="99e84-110">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that defines the point to be checked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99e84-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="99e84-111">Return value</span></span>

<span data-ttu-id="99e84-112">El valor devuelto es el identificador de la ventana que contiene el punto o **null** si no existe ninguna ventana en el punto especificado.</span><span class="sxs-lookup"><span data-stu-id="99e84-112">The return value is the handle to the window that contains the point, or **NULL** if no window exists at the specified point.</span></span>

## <a name="remarks"></a><span data-ttu-id="99e84-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="99e84-113">Remarks</span></span>

<span data-ttu-id="99e84-114">Este mensaje está diseñado para ser procesado por una aplicación que subclase una información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="99e84-114">This message is intended to be processed by an application that subclasses a tooltip.</span></span> <span data-ttu-id="99e84-115">No está diseñado para ser enviado por una aplicación.</span><span class="sxs-lookup"><span data-stu-id="99e84-115">It is not intended to be sent by an application.</span></span> <span data-ttu-id="99e84-116">La información sobre herramientas envía este mensaje a sí mismo antes de mostrar el texto de una ventana.</span><span class="sxs-lookup"><span data-stu-id="99e84-116">A tooltip sends this message to itself before displaying the text for a window.</span></span> <span data-ttu-id="99e84-117">Al cambiar las coordenadas del punto especificado por *lParam*, el procedimiento de subclase puede hacer que la información sobre herramientas muestre texto para una ventana que no sea la que se encuentra debajo del cursor del mouse.</span><span class="sxs-lookup"><span data-stu-id="99e84-117">By changing the coordinates of the point specified by *lParam*, the subclass procedure can cause the tooltip to display text for a window other than the one beneath the mouse cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="99e84-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99e84-118">Requirements</span></span>



| <span data-ttu-id="99e84-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="99e84-119">Requirement</span></span> | <span data-ttu-id="99e84-120">Value</span><span class="sxs-lookup"><span data-stu-id="99e84-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="99e84-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99e84-121">Minimum supported client</span></span><br/> | <span data-ttu-id="99e84-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="99e84-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="99e84-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99e84-123">Minimum supported server</span></span><br/> | <span data-ttu-id="99e84-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="99e84-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="99e84-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="99e84-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="99e84-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="99e84-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

