---
title: Mensaje de TVM_GETISEARCHSTRING (commctrl. h)
description: Recupera la cadena de búsqueda incremental para un control de vista de árbol.
ms.assetid: 71f9a9b6-e124-4655-80fc-dd23f441496d
keywords:
- TVM_GETISEARCHSTRING controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_GETISEARCHSTRING
- TVM_GETISEARCHSTRINGA
- TVM_GETISEARCHSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa968d78a1a99dd3b1eb90055cf2c1d2de51db86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151045"
---
# <a name="tvm_getisearchstring-message"></a><span data-ttu-id="98769-104">\_Mensaje de GETISEARCHSTRING TVM</span><span class="sxs-lookup"><span data-stu-id="98769-104">TVM\_GETISEARCHSTRING message</span></span>

<span data-ttu-id="98769-105">Recupera la cadena de búsqueda incremental para un control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="98769-105">Retrieves the incremental search string for a tree-view control.</span></span> <span data-ttu-id="98769-106">El control de vista de árbol utiliza la cadena de búsqueda incremental para seleccionar un elemento en función de los caracteres especificados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="98769-106">The tree-view control uses the incremental search string to select an item based on characters typed by the user.</span></span> <span data-ttu-id="98769-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetISearchString de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getisearchstring) .</span><span class="sxs-lookup"><span data-stu-id="98769-107">You can send this message explicitly or by using the [**TreeView\_GetISearchString**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getisearchstring) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="98769-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98769-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98769-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="98769-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="98769-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="98769-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="98769-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="98769-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98769-112">Puntero al búfer que recibe la cadena de búsqueda incremental.</span><span class="sxs-lookup"><span data-stu-id="98769-112">Pointer to the buffer that receives the incremental search string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98769-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98769-113">Return value</span></span>

<span data-ttu-id="98769-114">Devuelve el número de caracteres de la cadena de búsqueda incremental.</span><span class="sxs-lookup"><span data-stu-id="98769-114">Returns the number of characters in the incremental search string.</span></span>

## <a name="remarks"></a><span data-ttu-id="98769-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98769-115">Remarks</span></span>

<span data-ttu-id="98769-116">**Advertencia de seguridad:** El uso incorrecto de este mensaje podría poner en peligro la seguridad del programa.</span><span class="sxs-lookup"><span data-stu-id="98769-116">**Security Warning:** Using this message incorrectly might compromise the security of your program.</span></span> <span data-ttu-id="98769-117">Debe asignar un búfer suficientemente grande para contener la cadena.</span><span class="sxs-lookup"><span data-stu-id="98769-117">You must allocate a large enough buffer to hold the string.</span></span> <span data-ttu-id="98769-118">En primer lugar, llame al mensaje que pasa **null** en *lParam*.</span><span class="sxs-lookup"><span data-stu-id="98769-118">First call the message passing **NULL** in *lParam*.</span></span> <span data-ttu-id="98769-119">Esto devuelve el número de caracteres, excluidos los **valores NULL**, que son necesarios.</span><span class="sxs-lookup"><span data-stu-id="98769-119">This returns the number of characters, excluding **NULL**, that are required.</span></span> <span data-ttu-id="98769-120">A continuación, llame al mensaje una segunda vez para recuperar la cadena.</span><span class="sxs-lookup"><span data-stu-id="98769-120">Then call the message a second time to retrieve the string.</span></span> <span data-ttu-id="98769-121">Debe revisar las [consideraciones de seguridad: controles de Microsoft Windows](sec-comctls.md) antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="98769-121">You should review [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="98769-122">Si el control de vista de árbol no está en modo de búsqueda incremental, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="98769-122">If the tree-view control is not in incremental search mode, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="98769-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98769-123">Requirements</span></span>



| <span data-ttu-id="98769-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="98769-124">Requirement</span></span> | <span data-ttu-id="98769-125">Value</span><span class="sxs-lookup"><span data-stu-id="98769-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="98769-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98769-126">Minimum supported client</span></span><br/> | <span data-ttu-id="98769-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="98769-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="98769-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98769-128">Minimum supported server</span></span><br/> | <span data-ttu-id="98769-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="98769-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="98769-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98769-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="98769-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="98769-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="98769-132">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="98769-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="98769-133">**TVM \_ GETISEARCHSTRINGW** (Unicode) y **TVM \_ GETISEARCHSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="98769-133">**TVM\_GETISEARCHSTRINGW** (Unicode) and **TVM\_GETISEARCHSTRINGA** (ANSI)</span></span><br/> |



 

 





