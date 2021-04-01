---
title: Mensaje de HDM_GETORDERARRAY (commctrl. h)
description: Obtiene el orden actual de izquierda a derecha de los elementos de un control de encabezado. Puede enviar este mensaje explícitamente o utilizar la \_ macro header GetOrderArray.
ms.assetid: b287d3c1-ae61-41a4-a884-dc008eb24ad8
keywords:
- HDM_GETORDERARRAY controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_GETORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e334b0023ad3441c20048273e9bc58c1b25622b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150316"
---
# <a name="hdm_getorderarray-message"></a><span data-ttu-id="6cb4d-105">HDM \_ GETORDERARRAY</span><span class="sxs-lookup"><span data-stu-id="6cb4d-105">HDM\_GETORDERARRAY message</span></span>

<span data-ttu-id="6cb4d-106">Obtiene el orden actual de izquierda a derecha de los elementos de un control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="6cb4d-106">Gets the current left-to-right order of items in a header control.</span></span> <span data-ttu-id="6cb4d-107">Puede enviar este mensaje explícitamente o utilizar la macro [**Header \_ GetOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-header_getorderarray) .</span><span class="sxs-lookup"><span data-stu-id="6cb4d-107">You can send this message explicitly or use the [**Header\_GetOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-header_getorderarray) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6cb4d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6cb4d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cb4d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6cb4d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6cb4d-110">Número de elementos enteros que puede contener *lParam* .</span><span class="sxs-lookup"><span data-stu-id="6cb4d-110">The number of integer elements that *lParam* can hold.</span></span> <span data-ttu-id="6cb4d-111">Este valor debe ser igual al número de elementos del control (vea [**HDM \_ GETITEMCOUNT**](hdm-getitemcount.md)).</span><span class="sxs-lookup"><span data-stu-id="6cb4d-111">This value must be equal to the number of items in the control (see [**HDM\_GETITEMCOUNT**](hdm-getitemcount.md)).</span></span>

</dd> <dt>

<span data-ttu-id="6cb4d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6cb4d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6cb4d-113">Puntero a una matriz de enteros que reciben los valores de índice de los elementos del encabezado.</span><span class="sxs-lookup"><span data-stu-id="6cb4d-113">A pointer to an array of integers that receive the index values for items in the header.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cb4d-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6cb4d-114">Return value</span></span>

<span data-ttu-id="6cb4d-115">Devuelve un valor distinto de cero si es correcto y el búfer de *lParam* recibe el número de elemento de cada elemento del control de encabezado en el orden en el que aparecen de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="6cb4d-115">Returns nonzero if successful, and the buffer at *lParam* receives the item number for each item in the header control in the order in which they appear from left to right.</span></span> <span data-ttu-id="6cb4d-116">De lo contrario, el mensaje devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="6cb4d-116">Otherwise, the message returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cb4d-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6cb4d-117">Remarks</span></span>

<span data-ttu-id="6cb4d-118">El número de elementos de *lParam* se especifica en *wParam* y debe ser igual al número de elementos del control.</span><span class="sxs-lookup"><span data-stu-id="6cb4d-118">The number of elements in *lParam* is specified in *wParam* and must be equal to the number of items in the control.</span></span> <span data-ttu-id="6cb4d-119">Por ejemplo, el siguiente fragmento de código reservará suficiente memoria para contener los valores de índice.</span><span class="sxs-lookup"><span data-stu-id="6cb4d-119">For example, the following code fragment will reserve enough memory to hold the index values.</span></span>


```
int iItems,

    *lpiArray;



// Get memory for buffer.

(iItems = SendMessage(hwndHD, HDM_GETITEMCOUNT, 0,0))!=-1)

    if(!(lpiArray = calloc(iItems,sizeof(int))))

MessageBox(hwnd, "Out of memory.","Error", MB_OK);
```



## <a name="requirements"></a><span data-ttu-id="6cb4d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cb4d-120">Requirements</span></span>



| <span data-ttu-id="6cb4d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cb4d-121">Requirement</span></span> | <span data-ttu-id="6cb4d-122">Value</span><span class="sxs-lookup"><span data-stu-id="6cb4d-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6cb4d-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6cb4d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6cb4d-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6cb4d-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6cb4d-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6cb4d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6cb4d-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6cb4d-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6cb4d-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6cb4d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cb4d-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cb4d-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





