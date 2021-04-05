---
title: Mensaje de TB_GETIDEALSIZE (commctrl. h)
description: Obtiene el tamaño ideal de la barra de herramientas.
ms.assetid: d3b5ea4d-fd80-4f07-be4f-89b53a8bdf4d
keywords:
- TB_GETIDEALSIZE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a59b8701a4f4debcfb8e43f37068e7e7a4ef4f11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078998"
---
# <a name="tb_getidealsize-message"></a><span data-ttu-id="f786d-104">\_Mensaje GETIDEALSIZE TB</span><span class="sxs-lookup"><span data-stu-id="f786d-104">TB\_GETIDEALSIZE message</span></span>

<span data-ttu-id="f786d-105">Obtiene el tamaño ideal de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="f786d-105">Gets the ideal size of the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="f786d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f786d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f786d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f786d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f786d-108">Un **booleano** que indica si se va a recuperar el alto o ancho idóneos de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="f786d-108">A **BOOL** that indicates whether to retrieve the ideal height or width of the toolbar.</span></span> <span data-ttu-id="f786d-109">Use **true** para recuperar el alto ideal, **false** para recuperar el ancho ideal.</span><span class="sxs-lookup"><span data-stu-id="f786d-109">Use **TRUE** to retrieve the ideal height, **FALSE** to retrieve the ideal width.</span></span></dd> <dt>

<span data-ttu-id="f786d-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f786d-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f786d-111">Puntero a una estructura de [**tamaño**](/previous-versions//dd145106(v=vs.85)) que recibe el alto o el ancho en el que se mostrarán todos los botones.</span><span class="sxs-lookup"><span data-stu-id="f786d-111">Pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure that receives the height or width at which all buttons would be displayed.</span></span> <span data-ttu-id="f786d-112">Si *wParam* es **true**, solo el miembro **CY** (height) es válido.</span><span class="sxs-lookup"><span data-stu-id="f786d-112">If *wParam* is **TRUE**, only the **cy** member (height) is valid.</span></span> <span data-ttu-id="f786d-113">Si *wParam* es **false**, solo el miembro de **CX** (width) es válido.</span><span class="sxs-lookup"><span data-stu-id="f786d-113">If *wParam* is **FALSE**, only the **cx** member (width) is valid.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f786d-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f786d-114">Return value</span></span>

<span data-ttu-id="f786d-115">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f786d-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f786d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f786d-116">Requirements</span></span>



| <span data-ttu-id="f786d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f786d-117">Requirement</span></span> | <span data-ttu-id="f786d-118">Value</span><span class="sxs-lookup"><span data-stu-id="f786d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f786d-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f786d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f786d-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f786d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f786d-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f786d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f786d-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f786d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f786d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f786d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f786d-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f786d-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

