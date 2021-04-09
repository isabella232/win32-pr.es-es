---
title: Mensaje de RB_GETROWHEIGHT (commctrl. h)
description: Recupera el alto de una fila especificada en un control rebar.
ms.assetid: 1ff6a32e-b344-4dbc-b4a4-fb13f11a9d8c
keywords:
- RB_GETROWHEIGHT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_GETROWHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ce137eef6168d95abfe493a6f22ab66d58460b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905400"
---
# <a name="rb_getrowheight-message"></a><span data-ttu-id="22a50-104">Mensaje de GETROWHEIGHT de RB \_</span><span class="sxs-lookup"><span data-stu-id="22a50-104">RB\_GETROWHEIGHT message</span></span>

<span data-ttu-id="22a50-105">Recupera el alto de una fila especificada en un control rebar.</span><span class="sxs-lookup"><span data-stu-id="22a50-105">Retrieves the height of a specified row in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="22a50-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22a50-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22a50-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="22a50-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22a50-108">Índice de base cero de una banda.</span><span class="sxs-lookup"><span data-stu-id="22a50-108">Zero-based index of a band.</span></span> <span data-ttu-id="22a50-109">Se recuperará el alto de la fila que contiene la banda especificada.</span><span class="sxs-lookup"><span data-stu-id="22a50-109">The height of the row that contains the specified band will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="22a50-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="22a50-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="22a50-111">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="22a50-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22a50-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22a50-112">Return value</span></span>

<span data-ttu-id="22a50-113">Devuelve un valor **uint** que representa el alto de la fila, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="22a50-113">Returns a **UINT** value that represents the row height, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="22a50-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="22a50-114">Remarks</span></span>

<span data-ttu-id="22a50-115">Para recuperar el número de filas de un control rebar, utilice el mensaje de [**\_ ingetrowcount de RB**](rb-getrowcount.md) .</span><span class="sxs-lookup"><span data-stu-id="22a50-115">To retrieve the number of rows in a rebar control, use the [**RB\_GETROWCOUNT**](rb-getrowcount.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="22a50-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22a50-116">Requirements</span></span>



| <span data-ttu-id="22a50-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="22a50-117">Requirement</span></span> | <span data-ttu-id="22a50-118">Value</span><span class="sxs-lookup"><span data-stu-id="22a50-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="22a50-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22a50-119">Minimum supported client</span></span><br/> | <span data-ttu-id="22a50-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="22a50-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="22a50-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22a50-121">Minimum supported server</span></span><br/> | <span data-ttu-id="22a50-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="22a50-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="22a50-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22a50-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="22a50-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="22a50-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





