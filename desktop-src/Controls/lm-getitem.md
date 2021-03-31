---
title: Mensaje de LM_GETITEM (commctrl. h)
description: Recupera los Estados y atributos de un elemento.
ms.assetid: 75381f28-04d7-4a5c-bc0e-4cc74a06553f
keywords:
- LM_GETITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LM_GETITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbb0e05f896df00f3762c53e6f5f62119cb3645f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149913"
---
# <a name="lm_getitem-message"></a><span data-ttu-id="439a6-104">\_Mensaje GETITEM de LM</span><span class="sxs-lookup"><span data-stu-id="439a6-104">LM\_GETITEM message</span></span>

<span data-ttu-id="439a6-105">Recupera los Estados y atributos de un elemento.</span><span class="sxs-lookup"><span data-stu-id="439a6-105">Retrieves the states and attributes of an item.</span></span>

## <a name="parameters"></a><span data-ttu-id="439a6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="439a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="439a6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="439a6-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="439a6-108">Debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="439a6-108">Must be **NULL**.</span></span> </dd> <dt>

<span data-ttu-id="439a6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="439a6-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="439a6-110">Puntero <a href="/windows/win32/api/commctrl/ns-commctrl-litem">a una estructura de la</a> que se va a rellenar información sobre el elemento.</span><span class="sxs-lookup"><span data-stu-id="439a6-110">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-litem">LITEM</a> structure to be filled with information about the item.</span></span> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="439a6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="439a6-111">Return value</span></span>

<span data-ttu-id="439a6-112">Devuelve **true** si el mensaje se obtiene correctamente al obtener los valores y atributos especificados.</span><span class="sxs-lookup"><span data-stu-id="439a6-112">Returns **TRUE** if the message succeeds in getting the values and attributes specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="439a6-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="439a6-113">Remarks</span></span>

<span data-ttu-id="439a6-114">Con el mensaje de mensaje de error de **\_ LM** , solo se puede tener acceso a los vínculos a través del índice numérico devuelto en el miembro **iLink** [**de la**](/windows/win32/api/commctrl/ns-commctrl-litem).</span><span class="sxs-lookup"><span data-stu-id="439a6-114">With the **LM\_GETITEM** message, links can only be accessed through the numeric index returned in the **iLink** member of [**LITEM**](/windows/win32/api/commctrl/ns-commctrl-litem).</span></span> <span data-ttu-id="439a6-115">No se admite el acceso al vínculo a través del nombre de identificador devuelto en **szID** .</span><span class="sxs-lookup"><span data-stu-id="439a6-115">Accessing the link through the ID name returned in **szID** is not supported.</span></span>

> [!Note]  
> <span data-ttu-id="439a6-116">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="439a6-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="439a6-117">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="439a6-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="439a6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="439a6-118">Requirements</span></span>



| <span data-ttu-id="439a6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="439a6-119">Requirement</span></span> | <span data-ttu-id="439a6-120">Value</span><span class="sxs-lookup"><span data-stu-id="439a6-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="439a6-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="439a6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="439a6-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="439a6-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="439a6-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="439a6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="439a6-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="439a6-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="439a6-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="439a6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="439a6-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="439a6-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





