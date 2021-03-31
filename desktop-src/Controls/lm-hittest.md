---
title: Mensaje de LM_HITTEST (commctrl. h)
description: Determina si el usuario hizo clic en el vínculo especificado.
ms.assetid: a84c0388-26e7-4eda-9c6c-c5f64142d67a
keywords:
- LM_HITTEST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c497800369203ac8ea7484371e1038ba15d6cc68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905008"
---
# <a name="lm_hittest-message"></a><span data-ttu-id="0fcd7-104">\_Mensaje LM HITTEST</span><span class="sxs-lookup"><span data-stu-id="0fcd7-104">LM\_HITTEST message</span></span>

<span data-ttu-id="0fcd7-105">Determina si el usuario hizo clic en el vínculo especificado.</span><span class="sxs-lookup"><span data-stu-id="0fcd7-105">Determines whether the user clicked the specified link.</span></span>

## <a name="parameters"></a><span data-ttu-id="0fcd7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0fcd7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fcd7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0fcd7-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0fcd7-108">Debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="0fcd7-108">Must be **NULL**.</span></span></dd> <dt>

<span data-ttu-id="0fcd7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0fcd7-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0fcd7-110">Puntero a una estructura <a href="/windows/win32/api/commctrl/ns-commctrl-lhittestinfo">**LHITTESTINFO**</a> que se va a rellenar con información sobre el vínculo en el que el usuario hizo clic, si existe.</span><span class="sxs-lookup"><span data-stu-id="0fcd7-110">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-lhittestinfo">**LHITTESTINFO**</a> structure to be filled with information about the link the user clicked, if any exists.</span></span> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fcd7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0fcd7-111">Return value</span></span>

<span data-ttu-id="0fcd7-112">Devuelve **true** si el usuario hizo clic en un vínculo; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="0fcd7-112">Returns **TRUE** if user clicked on a link, otherwise returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fcd7-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0fcd7-113">Remarks</span></span>

<span data-ttu-id="0fcd7-114">Si el mensaje de **LM \_ HITTEST** se realiza correctamente, el sistema rellena en el [**. iLink**](/windows/win32/api/commctrl/ns-commctrl-litem) y en el **. szID**.</span><span class="sxs-lookup"><span data-stu-id="0fcd7-114">If the **LM\_HITTEST** message succeeds, the system fills in [**LITEM.iLink**](/windows/win32/api/commctrl/ns-commctrl-litem) and **LITEM.szID**.</span></span> <span data-ttu-id="0fcd7-115">Si se produce un error en el mensaje **LM \_ HITTEST** , no suponga que la **información de la** tarea es válida.</span><span class="sxs-lookup"><span data-stu-id="0fcd7-115">If the **LM\_HITTEST** message fails, do not assume that any information in **LITEM** is valid.</span></span>

> [!Note]  
> <span data-ttu-id="0fcd7-116">Para usar esta API, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="0fcd7-116">To use this API, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="0fcd7-117">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0fcd7-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0fcd7-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fcd7-118">Requirements</span></span>



| <span data-ttu-id="0fcd7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fcd7-119">Requirement</span></span> | <span data-ttu-id="0fcd7-120">Value</span><span class="sxs-lookup"><span data-stu-id="0fcd7-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0fcd7-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0fcd7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0fcd7-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0fcd7-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0fcd7-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0fcd7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0fcd7-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0fcd7-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0fcd7-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0fcd7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fcd7-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fcd7-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





