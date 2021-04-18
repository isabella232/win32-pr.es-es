---
title: Mensaje de CBEM_INSERTITEM (commctrl. h)
description: Inserta un nuevo elemento en un control ComboBoxEx.
ms.assetid: c99db676-204d-44c9-aaa3-81b70fe2cf44
keywords:
- CBEM_INSERTITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CBEM_INSERTITEM
- CBEM_INSERTITEMA
- CBEM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23e6cb26a575472e53703d65e407a94a024dcfac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658393"
---
# <a name="cbem_insertitem-message"></a><span data-ttu-id="1ab85-104">CBEM \_ INSERTITEM Message</span><span class="sxs-lookup"><span data-stu-id="1ab85-104">CBEM\_INSERTITEM message</span></span>

<span data-ttu-id="1ab85-105">Inserta un nuevo elemento en un control ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="1ab85-105">Inserts a new item in a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1ab85-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ab85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ab85-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1ab85-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1ab85-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1ab85-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1ab85-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ab85-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ab85-110">Puntero a una estructura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) que contiene información sobre el elemento que se va a insertar.</span><span class="sxs-lookup"><span data-stu-id="1ab85-110">A pointer to a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure that contains information about the item to be inserted.</span></span> <span data-ttu-id="1ab85-111">Cuando se envía el mensaje, se debe establecer el miembro **iItem** para indicar el índice basado en cero en el que se va a insertar el elemento.</span><span class="sxs-lookup"><span data-stu-id="1ab85-111">When the message is sent, the **iItem** member must be set to indicate the zero-based index at which to insert the item.</span></span> <span data-ttu-id="1ab85-112">Para insertar un elemento al final de la lista, establezca el miembro **iItem** en-1.</span><span class="sxs-lookup"><span data-stu-id="1ab85-112">To insert an item at the end of the list, set the **iItem** member to -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ab85-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ab85-113">Return value</span></span>

<span data-ttu-id="1ab85-114">Devuelve el índice en el que se insertó el nuevo elemento si se realiza correctamente, o-1 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1ab85-114">Returns the index at which the new item was inserted if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ab85-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ab85-115">Requirements</span></span>



| <span data-ttu-id="1ab85-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ab85-116">Requirement</span></span> | <span data-ttu-id="1ab85-117">Value</span><span class="sxs-lookup"><span data-stu-id="1ab85-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab85-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ab85-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1ab85-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1ab85-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1ab85-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ab85-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1ab85-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1ab85-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1ab85-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1ab85-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ab85-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ab85-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="1ab85-124">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="1ab85-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1ab85-125">**CBEM \_ INSERTITEMW** (Unicode) y **CBEM \_ INSERTITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1ab85-125">**CBEM\_INSERTITEMW** (Unicode) and **CBEM\_INSERTITEMA** (ANSI)</span></span><br/>           |



 

 





