---
title: Mensaje de DTM_GETIDEALSIZE (commctrl. h)
description: Obtiene el tamaño necesario para mostrar el control sin recorte. Envíe este mensaje explícitamente o mediante la macro GetIdealSize de fecha y hora \_ .
ms.assetid: 15ec26a1-645b-4a96-af66-1031e1a46c6c
keywords:
- DTM_GETIDEALSIZE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- DTM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a979883f431fea4627f52fe19c3716341e3f2328
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274514"
---
# <a name="dtm_getidealsize-message"></a><span data-ttu-id="1dfea-105">DTM \_ GETIDEALSIZE</span><span class="sxs-lookup"><span data-stu-id="1dfea-105">DTM\_GETIDEALSIZE message</span></span>

<span data-ttu-id="1dfea-106">Obtiene el tamaño necesario para mostrar el control sin recorte.</span><span class="sxs-lookup"><span data-stu-id="1dfea-106">Gets the size needed to display the control without clipping.</span></span> <span data-ttu-id="1dfea-107">Envíe este mensaje explícitamente o mediante la [**macro \_ GetIdealSize de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize) .</span><span class="sxs-lookup"><span data-stu-id="1dfea-107">Send this message explicitly or by using the [**DateTime\_GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1dfea-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1dfea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dfea-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1dfea-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1dfea-110">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="1dfea-110">Not used.</span></span> <span data-ttu-id="1dfea-111">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1dfea-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1dfea-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1dfea-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1dfea-113">Puntero a una estructura de [**tamaño**](/previous-versions//dd145106(v=vs.85)) para recibir el tamaño ideal.</span><span class="sxs-lookup"><span data-stu-id="1dfea-113">A pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure to receive the ideal size.</span></span> <span data-ttu-id="1dfea-114">La aplicación que realiza la llamada es responsable de la asignación de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="1dfea-114">The calling application is responsible for allocating this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dfea-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1dfea-115">Return value</span></span>

<span data-ttu-id="1dfea-116">Devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="1dfea-116">Returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dfea-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1dfea-117">Requirements</span></span>



| <span data-ttu-id="1dfea-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dfea-118">Requirement</span></span> | <span data-ttu-id="1dfea-119">Value</span><span class="sxs-lookup"><span data-stu-id="1dfea-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1dfea-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1dfea-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1dfea-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1dfea-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1dfea-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1dfea-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1dfea-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1dfea-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1dfea-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1dfea-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1dfea-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1dfea-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

