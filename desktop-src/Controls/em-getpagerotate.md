---
title: Mensaje EM_GETPAGEROTATE (RichEdit. h)
description: Obtiene el diseño de texto de un control Rich Edit de Microsoft.
ms.assetid: 0efb112e-ad51-4ebb-9037-3aee3ab9ad1d
keywords:
- EM_GETPAGEROTATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETPAGEROTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad7bc7cd3c77ae88cd4c8710e14b4472e57407ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492485"
---
# <a name="em_getpagerotate-message"></a><span data-ttu-id="ebdde-104">\_Mensaje GETPAGEROTATE em</span><span class="sxs-lookup"><span data-stu-id="ebdde-104">EM\_GETPAGEROTATE message</span></span>

<span data-ttu-id="ebdde-105">\[**Em \_ GETPAGEROTATE** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="ebdde-105">\[**EM\_GETPAGEROTATE** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ebdde-106">En versiones posteriores podría modificarse o no estar disponible.\]</span><span class="sxs-lookup"><span data-stu-id="ebdde-106">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="ebdde-107">Obtiene el diseño de texto de un control Rich Edit de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ebdde-107">Gets the text layout for a Microsoft Rich Edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ebdde-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ebdde-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebdde-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ebdde-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ebdde-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ebdde-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ebdde-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ebdde-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ebdde-112">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ebdde-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebdde-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ebdde-113">Return value</span></span>

<span data-ttu-id="ebdde-114">Obtiene el diseño del texto actual.</span><span class="sxs-lookup"><span data-stu-id="ebdde-114">Gets the current text layout.</span></span> <span data-ttu-id="ebdde-115">Para obtener una lista de posibles valores de diseño de texto, consulte [**em \_ SETPAGEROTATE**](em-setpagerotate.md).</span><span class="sxs-lookup"><span data-stu-id="ebdde-115">For a list of possible text layout values, see [**EM\_SETPAGEROTATE**](em-setpagerotate.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ebdde-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebdde-116">Requirements</span></span>



| <span data-ttu-id="ebdde-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebdde-117">Requirement</span></span> | <span data-ttu-id="ebdde-118">Value</span><span class="sxs-lookup"><span data-stu-id="ebdde-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ebdde-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ebdde-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ebdde-120">Solo aplicaciones de escritorio de Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="ebdde-120">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ebdde-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ebdde-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ebdde-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ebdde-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ebdde-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ebdde-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebdde-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebdde-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebdde-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="ebdde-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebdde-126">**\_SETPAGEROTATE em**</span><span class="sxs-lookup"><span data-stu-id="ebdde-126">**EM\_SETPAGEROTATE**</span></span>](em-setpagerotate.md)
</dt> </dl>

 

 





