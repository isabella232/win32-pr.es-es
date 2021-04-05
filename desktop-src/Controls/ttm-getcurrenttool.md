---
title: Mensaje de TTM_GETCURRENTTOOL (commctrl. h)
description: Recupera la información de la herramienta actual en un control de información sobre herramientas.
ms.assetid: acb254cf-064c-4ed8-b488-a3138b648405
keywords:
- TTM_GETCURRENTTOOL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_GETCURRENTTOOL
- TTM_GETCURRENTTOOLA
- TTM_GETCURRENTTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa6218bcb4ad9aa43c7ffba0d332786956d9a62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996414"
---
# <a name="ttm_getcurrenttool-message"></a><span data-ttu-id="cb26b-104">TTM \_ GETCURRENTTOOL</span><span class="sxs-lookup"><span data-stu-id="cb26b-104">TTM\_GETCURRENTTOOL message</span></span>

<span data-ttu-id="cb26b-105">Recupera la información de la herramienta actual en un control de información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="cb26b-105">Retrieves the information for the current tool in a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="cb26b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb26b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb26b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cb26b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cb26b-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="cb26b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cb26b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb26b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb26b-110">Puntero a una estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que recibe información sobre la herramienta actual.</span><span class="sxs-lookup"><span data-stu-id="cb26b-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that receives information about the current tool.</span></span> <span data-ttu-id="cb26b-111">Si este valor es **null**, el valor devuelto indica la existencia de la herramienta actual sin recuperar realmente la información de la herramienta.</span><span class="sxs-lookup"><span data-stu-id="cb26b-111">If this value is **NULL**, the return value indicates the existence of the current tool without actually retrieving the tool information.</span></span> <span data-ttu-id="cb26b-112">Si este valor no es **null**, el miembro **cbSize** de la estructura **TOOLINFO** se debe rellenar antes de enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="cb26b-112">If this value is not **NULL**, the **cbSize** member of the **TOOLINFO** structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb26b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb26b-113">Return value</span></span>

<span data-ttu-id="cb26b-114">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="cb26b-114">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="cb26b-115">Si *lParam* es **null**, devuelve un valor distinto de cero si existe una herramienta actual o cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="cb26b-115">If *lParam* is **NULL**, returns nonzero if a current tool exists, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb26b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb26b-116">Requirements</span></span>



| <span data-ttu-id="cb26b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb26b-117">Requirement</span></span> | <span data-ttu-id="cb26b-118">Value</span><span class="sxs-lookup"><span data-stu-id="cb26b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb26b-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb26b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cb26b-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cb26b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cb26b-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb26b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cb26b-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cb26b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cb26b-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cb26b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb26b-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb26b-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="cb26b-125">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="cb26b-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cb26b-126">**TTM \_ GETCURRENTTOOLW** (Unicode) y **TTM \_ GETCURRENTTOOLA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="cb26b-126">**TTM\_GETCURRENTTOOLW** (Unicode) and **TTM\_GETCURRENTTOOLA** (ANSI)</span></span><br/>     |



 

 





