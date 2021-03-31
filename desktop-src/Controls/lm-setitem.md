---
title: Mensaje de LM_SETITEM (commctrl. h)
description: Establece los Estados y los atributos de un elemento.
ms.assetid: 02a68a31-2541-480e-b768-449d40e5e9e0
keywords:
- LM_SETITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LM_SETITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11888a76b11ccec7e8e659ca3a33bb23a71667ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149911"
---
# <a name="lm_setitem-message"></a><span data-ttu-id="5f232-104">\_Mensaje SETITEM de LM</span><span class="sxs-lookup"><span data-stu-id="5f232-104">LM\_SETITEM message</span></span>

<span data-ttu-id="5f232-105">Establece los Estados y los atributos de un elemento.</span><span class="sxs-lookup"><span data-stu-id="5f232-105">Sets the states and attributes of an item.</span></span>

## <a name="parameters"></a><span data-ttu-id="5f232-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f232-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f232-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5f232-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5f232-108">Debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="5f232-108">Must be **NULL**.</span></span> </dd> <dt>

<span data-ttu-id="5f232-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f232-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5f232-110">Puntero <a href="/windows/win32/api/commctrl/ns-commctrl-litem">a una estructura de un</a> valor que contiene los nuevos Estados y atributos que se desean para el vínculo.</span><span class="sxs-lookup"><span data-stu-id="5f232-110">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-litem">LITEM</a> structure containing the new states and attributes desired for the link.</span></span> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f232-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f232-111">Return value</span></span>

<span data-ttu-id="5f232-112">Devuelve **true** si el mensaje se establece correctamente en el establecimiento de los valores y los atributos especificados.</span><span class="sxs-lookup"><span data-stu-id="5f232-112">Returns **TRUE** if the message succeeds in setting the values and attributes specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f232-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f232-113">Remarks</span></span>

<span data-ttu-id="5f232-114">Con el mensaje de mensaje de error de [**\_ LM**](lm-getitem.md) , solo se puede tener acceso a los vínculos a través del índice numérico devuelto en el miembro **iLink** [**de la**](/windows/win32/api/commctrl/ns-commctrl-litem).</span><span class="sxs-lookup"><span data-stu-id="5f232-114">With the [**LM\_GETITEM**](lm-getitem.md) message, links can only be accessed through the numeric index returned in the **iLink** member of [**LITEM**](/windows/win32/api/commctrl/ns-commctrl-litem).</span></span> <span data-ttu-id="5f232-115">No se admite el acceso al vínculo a través del nombre de identificador devuelto en **szID** .</span><span class="sxs-lookup"><span data-stu-id="5f232-115">Accessing the link through the ID name returned in **szID** is not supported.</span></span>

> [!Note]  
> <span data-ttu-id="5f232-116">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comctl32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="5f232-116">To use this message, you must provide a manifest specifying Comctl32.dll version 6.0.</span></span> <span data-ttu-id="5f232-117">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5f232-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5f232-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f232-118">Requirements</span></span>



| <span data-ttu-id="5f232-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f232-119">Requirement</span></span> | <span data-ttu-id="5f232-120">Value</span><span class="sxs-lookup"><span data-stu-id="5f232-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f232-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f232-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5f232-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5f232-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5f232-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f232-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5f232-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5f232-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5f232-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f232-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f232-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f232-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





