---
title: Mensaje de HDM_SETORDERARRAY (commctrl. h)
description: Establece el orden de izquierda a derecha de los elementos de encabezado. Puede enviar este mensaje explícitamente o utilizar la \_ macro header SetOrderArray.
ms.assetid: 094c424f-10bd-484d-8236-937811b703a6
keywords:
- HDM_SETORDERARRAY controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_SETORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f07874bfc102babec18b142a087b14e330044ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490865"
---
# <a name="hdm_setorderarray-message"></a><span data-ttu-id="c9ede-105">HDM \_ SETORDERARRAY</span><span class="sxs-lookup"><span data-stu-id="c9ede-105">HDM\_SETORDERARRAY message</span></span>

<span data-ttu-id="c9ede-106">Establece el orden de izquierda a derecha de los elementos de encabezado.</span><span class="sxs-lookup"><span data-stu-id="c9ede-106">Sets the left-to-right order of header items.</span></span> <span data-ttu-id="c9ede-107">Puede enviar este mensaje explícitamente o utilizar la macro [**Header \_ SetOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-header_setorderarray) .</span><span class="sxs-lookup"><span data-stu-id="c9ede-107">You can send this message explicitly or use the [**Header\_SetOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-header_setorderarray) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c9ede-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9ede-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9ede-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c9ede-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9ede-110">Tamaño del búfer en *lParam*, en elementos.</span><span class="sxs-lookup"><span data-stu-id="c9ede-110">The size of the buffer at *lParam*, in elements.</span></span> <span data-ttu-id="c9ede-111">Este valor debe ser igual al valor devuelto por [**HDM \_ GETITEMCOUNT**](hdm-getitemcount.md).</span><span class="sxs-lookup"><span data-stu-id="c9ede-111">This value must equal the value returned by [**HDM\_GETITEMCOUNT**](hdm-getitemcount.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9ede-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c9ede-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9ede-113">Puntero a una matriz que especifica el orden en el que se deben mostrar los elementos, de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="c9ede-113">A pointer to an array that specifies the order in which items should be displayed, from left to right.</span></span> <span data-ttu-id="c9ede-114">Por ejemplo, si el contenido de la matriz es {2,0,1} , el control muestra el elemento 2, el elemento 0 y el elemento 1, de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="c9ede-114">For example, if the contents of the array are {2,0,1}, the control displays item 2, item 0, and item 1, from left to right.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9ede-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9ede-115">Return value</span></span>

<span data-ttu-id="c9ede-116">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="c9ede-116">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9ede-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9ede-117">Requirements</span></span>



| <span data-ttu-id="c9ede-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9ede-118">Requirement</span></span> | <span data-ttu-id="c9ede-119">Value</span><span class="sxs-lookup"><span data-stu-id="c9ede-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9ede-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9ede-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c9ede-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c9ede-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c9ede-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9ede-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c9ede-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c9ede-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c9ede-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9ede-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9ede-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9ede-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





