---
title: Mensaje de LVM_GETCOLUMNORDERARRAY (commctrl. h)
description: Obtiene el orden de izquierda a derecha actual de las columnas en un control de vista de lista. Puede enviar este mensaje explícitamente o utilizar la \_ macro GetColumnOrderArray de ListView.
ms.assetid: d4636aa8-c61e-4467-abc7-eea897bf370e
keywords:
- LVM_GETCOLUMNORDERARRAY controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aee387f65abd3f30826e361778d5acac02dfab7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078871"
---
# <a name="lvm_getcolumnorderarray-message"></a><span data-ttu-id="feaa3-105">\_Mensaje GETCOLUMNORDERARRAY LVM</span><span class="sxs-lookup"><span data-stu-id="feaa3-105">LVM\_GETCOLUMNORDERARRAY message</span></span>

<span data-ttu-id="feaa3-106">Obtiene el orden de izquierda a derecha actual de las columnas en un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="feaa3-106">Gets the current left-to-right order of columns in a list-view control.</span></span> <span data-ttu-id="feaa3-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetColumnOrderArray de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnorderarray) .</span><span class="sxs-lookup"><span data-stu-id="feaa3-107">You can send this message explicitly or use the [**ListView\_GetColumnOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnorderarray) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="feaa3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="feaa3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="feaa3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="feaa3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="feaa3-110">El número de columnas en el control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="feaa3-110">The number of columns in the list-view control.</span></span>

</dd> <dt>

<span data-ttu-id="feaa3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="feaa3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="feaa3-112">Puntero a una matriz de enteros que recibe los valores de índice de las columnas en el control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="feaa3-112">A pointer to an array of integers that receives the index values of the columns in the list-view control.</span></span> <span data-ttu-id="feaa3-113">La matriz debe ser lo suficientemente grande como para contener los elementos *wParam* .</span><span class="sxs-lookup"><span data-stu-id="feaa3-113">The array must be large enough to hold *wParam* elements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="feaa3-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="feaa3-114">Return value</span></span>

<span data-ttu-id="feaa3-115">Si es correcto, devuelve un valor distinto de cero y el búfer de *lParam* recibe el índice de columna de cada columna del control en el orden en que aparecen de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="feaa3-115">If successful, returns nonzero, and the buffer at *lParam* receives the column index of each column in the control in the order they appear from left to right.</span></span> <span data-ttu-id="feaa3-116">De lo contrario, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="feaa3-116">Otherwise, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="feaa3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="feaa3-117">Requirements</span></span>



| <span data-ttu-id="feaa3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="feaa3-118">Requirement</span></span> | <span data-ttu-id="feaa3-119">Value</span><span class="sxs-lookup"><span data-stu-id="feaa3-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="feaa3-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="feaa3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="feaa3-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="feaa3-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="feaa3-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="feaa3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="feaa3-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="feaa3-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="feaa3-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="feaa3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="feaa3-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="feaa3-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





