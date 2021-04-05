---
title: Mensaje de LVM_SETITEMINDEXSTATE (commctrl. h)
description: Establece el estado de un elemento de vista de lista. Envíe este mensaje explícitamente o mediante la \_ macro SetItemIndexState de ListView.
ms.assetid: 9fea6420-320a-4d2a-84b5-7923fbb14655
keywords:
- LVM_SETITEMINDEXSTATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETITEMINDEXSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ce8f6847c733127053e2162dd785d52fb77cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079131"
---
# <a name="lvm_setitemindexstate-message"></a><span data-ttu-id="d0920-105">\_Mensaje SETITEMINDEXSTATE LVM</span><span class="sxs-lookup"><span data-stu-id="d0920-105">LVM\_SETITEMINDEXSTATE message</span></span>

<span data-ttu-id="d0920-106">Establece el estado de un elemento de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="d0920-106">Sets the state of a list-view item.</span></span> <span data-ttu-id="d0920-107">Envíe este mensaje explícitamente o mediante la [**macro \_ SetItemIndexState de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemindexstate) .</span><span class="sxs-lookup"><span data-stu-id="d0920-107">Send this message explicitly or by using the [**ListView\_SetItemIndexState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemindexstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d0920-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0920-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0920-109">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d0920-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0920-110">Puntero a una estructura [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) para el elemento.</span><span class="sxs-lookup"><span data-stu-id="d0920-110">A pointer to an [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) structure for the item.</span></span> <span data-ttu-id="d0920-111">El proceso de llamada es responsable de la asignación de esta estructura y de la configuración de los miembros.</span><span class="sxs-lookup"><span data-stu-id="d0920-111">The calling process is responsible for allocating this structure and setting the members.</span></span>

</dd> <dt>

<span data-ttu-id="d0920-112">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d0920-112">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0920-113">Puntero a una estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="d0920-113">A pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span> <span data-ttu-id="d0920-114">El proceso de llamada es responsable de la asignación de memoria para la estructura.</span><span class="sxs-lookup"><span data-stu-id="d0920-114">The calling process is responsible for allocating memory for the structure.</span></span> <span data-ttu-id="d0920-115">Establezca el miembro **State** en una o varias (como una combinación bit a bit) de las marcas de [los Estados de los elementos](list-view-item-states.md) de la vista de lista.</span><span class="sxs-lookup"><span data-stu-id="d0920-115">Set the **state** member to one or more (as a bitwise combination) of the [List-View Item States](list-view-item-states.md) flags.</span></span> <span data-ttu-id="d0920-116">Establezca el miembro **stateMask** de la estructura para indicar los bits válidos del miembro **State** .</span><span class="sxs-lookup"><span data-stu-id="d0920-116">Set the **stateMask** member of the structure to indicate the valid bits of the **state** member.</span></span> <span data-ttu-id="d0920-117">Para obtener más información, vea el miembro **stateMask** de la estructura **LVITEM** .</span><span class="sxs-lookup"><span data-stu-id="d0920-117">For more information, see the **stateMask** member of the **LVITEM** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0920-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0920-118">Return value</span></span>

<span data-ttu-id="d0920-119">Devuelve uno de los siguientes valores de tipo **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d0920-119">Returns one of the following values of type **HRESULT**.</span></span>



| <span data-ttu-id="d0920-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d0920-120">Return code</span></span>                                                                                  | <span data-ttu-id="d0920-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0920-121">Description</span></span>                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="d0920-122"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="d0920-122"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="d0920-123">No se pudo establecer el estado.</span><span class="sxs-lookup"><span data-stu-id="d0920-123">The state could not be set.</span></span><br/>                            |
| <dl> <span data-ttu-id="d0920-124"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="d0920-124"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="d0920-125">El control de vista de lista no estaba listo para la operación.</span><span class="sxs-lookup"><span data-stu-id="d0920-125">The list-view control was not ready for the operation.</span></span><br/> |
| <dl> <span data-ttu-id="d0920-126"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="d0920-126"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="d0920-127">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d0920-127">The operation was successful.</span></span><br/>                          |



 

## <a name="requirements"></a><span data-ttu-id="d0920-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0920-128">Requirements</span></span>



| <span data-ttu-id="d0920-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0920-129">Requirement</span></span> | <span data-ttu-id="d0920-130">Value</span><span class="sxs-lookup"><span data-stu-id="d0920-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d0920-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0920-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d0920-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d0920-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d0920-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0920-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d0920-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d0920-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d0920-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0920-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0920-136"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0920-136"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





