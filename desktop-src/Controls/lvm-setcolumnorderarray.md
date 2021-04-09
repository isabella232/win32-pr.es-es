---
title: Mensaje de LVM_SETCOLUMNORDERARRAY (commctrl. h)
description: Establece el orden de izquierda a derecha de las columnas en un control de vista de lista. Puede enviar este mensaje explícitamente o utilizar la \_ macro SetColumnOrderArray de ListView.
ms.assetid: 9b491832-42cc-4262-8f6c-23cbc2c889bf
keywords:
- LVM_SETCOLUMNORDERARRAY controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETCOLUMNORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94fdeb27074a3f6762e7fb3788fd7ccc0a2dcc5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078863"
---
# <a name="lvm_setcolumnorderarray-message"></a><span data-ttu-id="59b92-105">\_Mensaje SETCOLUMNORDERARRAY LVM</span><span class="sxs-lookup"><span data-stu-id="59b92-105">LVM\_SETCOLUMNORDERARRAY message</span></span>

<span data-ttu-id="59b92-106">Establece el orden de izquierda a derecha de las columnas en un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="59b92-106">Sets the left-to-right order of columns in a list-view control.</span></span> <span data-ttu-id="59b92-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ SetColumnOrderArray de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnorderarray) .</span><span class="sxs-lookup"><span data-stu-id="59b92-107">You can send this message explicitly or use the [**ListView\_SetColumnOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnorderarray) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="59b92-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="59b92-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59b92-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="59b92-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59b92-110">Tamaño, en elementos, del búfer en *lParam*.</span><span class="sxs-lookup"><span data-stu-id="59b92-110">Size, in elements, of the buffer at *lParam*.</span></span>

</dd> <dt>

<span data-ttu-id="59b92-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="59b92-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59b92-112">Puntero a una matriz que especifica el orden en el que se deben mostrar las columnas, de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="59b92-112">Pointer to an array that specifies the order in which columns should be displayed, from left to right.</span></span> <span data-ttu-id="59b92-113">Por ejemplo, si el contenido de la matriz es {2,0,1} , el control muestra la columna 2, la columna 0 y la columna 1 en ese orden.</span><span class="sxs-lookup"><span data-stu-id="59b92-113">For example, if the contents of the array are {2,0,1}, the control displays column 2, column 0, and column 1 in that order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59b92-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="59b92-114">Return value</span></span>

<span data-ttu-id="59b92-115">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="59b92-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="59b92-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59b92-116">Requirements</span></span>



| <span data-ttu-id="59b92-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="59b92-117">Requirement</span></span> | <span data-ttu-id="59b92-118">Value</span><span class="sxs-lookup"><span data-stu-id="59b92-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="59b92-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59b92-119">Minimum supported client</span></span><br/> | <span data-ttu-id="59b92-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="59b92-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="59b92-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59b92-121">Minimum supported server</span></span><br/> | <span data-ttu-id="59b92-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="59b92-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="59b92-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59b92-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="59b92-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="59b92-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





