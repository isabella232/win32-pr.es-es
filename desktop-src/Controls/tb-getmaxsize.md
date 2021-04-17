---
title: Mensaje de TB_GETMAXSIZE (commctrl. h)
description: Recupera el tamaño total de todos los botones y separadores visibles en la barra de herramientas.
ms.assetid: 560e6ce2-00ef-46c3-b1d8-fbe0ac79c888
keywords:
- TB_GETMAXSIZE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETMAXSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4829e65d90c04181369dd73b9c54634f1077144
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658287"
---
# <a name="tb_getmaxsize-message"></a><span data-ttu-id="f25f5-104">\_Mensaje GETMAXSIZE TB</span><span class="sxs-lookup"><span data-stu-id="f25f5-104">TB\_GETMAXSIZE message</span></span>

<span data-ttu-id="f25f5-105">Recupera el tamaño total de todos los botones y separadores visibles en la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="f25f5-105">Retrieves the total size of all of the visible buttons and separators in the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="f25f5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f25f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f25f5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f25f5-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f25f5-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f25f5-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f25f5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f25f5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f25f5-110">Puntero a una estructura de [**tamaño**](/previous-versions//dd145106(v=vs.85)) que recibe el tamaño de los elementos.</span><span class="sxs-lookup"><span data-stu-id="f25f5-110">Pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure that receives the size of the items.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f25f5-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f25f5-111">Return value</span></span>

<span data-ttu-id="f25f5-112">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="f25f5-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f25f5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f25f5-113">Requirements</span></span>



| <span data-ttu-id="f25f5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f25f5-114">Requirement</span></span> | <span data-ttu-id="f25f5-115">Value</span><span class="sxs-lookup"><span data-stu-id="f25f5-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f25f5-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f25f5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f25f5-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f25f5-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f25f5-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f25f5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f25f5-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f25f5-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f25f5-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f25f5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f25f5-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f25f5-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

