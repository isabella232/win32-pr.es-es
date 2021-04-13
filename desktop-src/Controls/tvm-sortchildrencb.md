---
title: Mensaje de TVM_SORTCHILDRENCB (commctrl. h)
description: Ordena los elementos de la vista de árbol usando una función de devolución de llamada definida por la aplicación que compara los elementos. Puede enviar este mensaje explícitamente o mediante la \_ macro SortChildrenCB de TreeView.
ms.assetid: 1669e576-5e57-49f6-8097-7d6547306014
keywords:
- TVM_SORTCHILDRENCB controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_SORTCHILDRENCB
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b1dab4abbbc019a81d7a066c81dbb3537a0d80d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492838"
---
# <a name="tvm_sortchildrencb-message"></a><span data-ttu-id="b6508-105">\_Mensaje de SORTCHILDRENCB TVM</span><span class="sxs-lookup"><span data-stu-id="b6508-105">TVM\_SORTCHILDRENCB message</span></span>

<span data-ttu-id="b6508-106">Ordena los elementos de la vista de árbol usando una función de devolución de llamada definida por la aplicación que compara los elementos.</span><span class="sxs-lookup"><span data-stu-id="b6508-106">Sorts tree-view items using an application-defined callback function that compares the items.</span></span> <span data-ttu-id="b6508-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ SortChildrenCB de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildrencb) .</span><span class="sxs-lookup"><span data-stu-id="b6508-107">You can send this message explicitly or by using the [**TreeView\_SortChildrenCB**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildrencb) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b6508-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b6508-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6508-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6508-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6508-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="b6508-110">Reserved.</span></span> <span data-ttu-id="b6508-111">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b6508-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b6508-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6508-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6508-113">Puntero a una estructura [**TVSORTCB**](/windows/win32/api/commctrl/ns-commctrl-tvsortcb) .</span><span class="sxs-lookup"><span data-stu-id="b6508-113">Pointer to a [**TVSORTCB**](/windows/win32/api/commctrl/ns-commctrl-tvsortcb) structure.</span></span> <span data-ttu-id="b6508-114">El miembro **lpfnCompare** es la dirección de la función de devolución de llamada definida por la aplicación, a la que se llama durante la operación de ordenación cada vez que es necesario comparar el orden relativo de dos elementos de lista.</span><span class="sxs-lookup"><span data-stu-id="b6508-114">The **lpfnCompare** member is the address of the application-defined callback function, which is called during the sort operation each time the relative order of two list items needs to be compared.</span></span> <span data-ttu-id="b6508-115">Para obtener más información sobre la función de devolución de llamada, vea la descripción de **TVSORTCB**.</span><span class="sxs-lookup"><span data-stu-id="b6508-115">For more information about the callback function, see the description of **TVSORTCB**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6508-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b6508-116">Return value</span></span>

<span data-ttu-id="b6508-117">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b6508-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6508-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6508-118">Requirements</span></span>



| <span data-ttu-id="b6508-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6508-119">Requirement</span></span> | <span data-ttu-id="b6508-120">Value</span><span class="sxs-lookup"><span data-stu-id="b6508-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b6508-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6508-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b6508-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b6508-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b6508-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6508-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b6508-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b6508-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b6508-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6508-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6508-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6508-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





