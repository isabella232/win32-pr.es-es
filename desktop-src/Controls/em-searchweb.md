---
title: Mensaje de EM_SEARCHWEB (commctrl. h)
description: Abre el explorador y realiza una búsqueda web con el texto seleccionado como término de búsqueda.
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- EM_SEARCHWEB controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SEARCHWEB
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e83c18db47d18648797ee3d58fe12567af941b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905479"
---
# <a name="em_searchweb-message"></a><span data-ttu-id="5f31b-104">\_Mensaje SEARCHWEB em</span><span class="sxs-lookup"><span data-stu-id="5f31b-104">EM\_SEARCHWEB message</span></span>

<span data-ttu-id="5f31b-105">Abre el explorador y realiza una búsqueda web con el texto seleccionado como término de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="5f31b-105">Opens the browser and performs a web search with the selected text as the search term.</span></span>

## <a name="parameters"></a><span data-ttu-id="5f31b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f31b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f31b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5f31b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f31b-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5f31b-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5f31b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f31b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f31b-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5f31b-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f31b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f31b-111">Return value</span></span>

<span data-ttu-id="5f31b-112">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="5f31b-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f31b-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f31b-113">Remarks</span></span>

<span data-ttu-id="5f31b-114">Si la característica "Buscar en la web" está deshabilitada mediante el mensaje [**em \_ ENABLESEARCHWEB**](em-enablesearchweb.md) , este mensaje no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="5f31b-114">If the "Search the web" feature is disabled using the [**EM\_ENABLESEARCHWEB**](em-enablesearchweb.md) message, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f31b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f31b-115">Requirements</span></span>



| <span data-ttu-id="5f31b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f31b-116">Requirement</span></span> | <span data-ttu-id="5f31b-117">Value</span><span class="sxs-lookup"><span data-stu-id="5f31b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f31b-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f31b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5f31b-119">Solo aplicaciones de escritorio de Windows 10 y 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="5f31b-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5f31b-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f31b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5f31b-121">Solo aplicaciones de escritorio de Windows Server 2019 \[\]</span><span class="sxs-lookup"><span data-stu-id="5f31b-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5f31b-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f31b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f31b-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f31b-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f31b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f31b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f31b-125">**\_ENABLESEARCHWEB em**</span><span class="sxs-lookup"><span data-stu-id="5f31b-125">**EM\_ENABLESEARCHWEB**</span></span>](em-enablesearchweb.md)
</dt> </dl>

 

 





