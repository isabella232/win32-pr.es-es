---
title: Mensaje de TB_INSERTMARKHITTEST (commctrl. h)
description: Recupera la información de la marca de inserción para un punto de una barra de herramientas.
ms.assetid: 65c64fd0-f089-4b1a-84e5-1a3e10aa7f5e
keywords:
- TB_INSERTMARKHITTEST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5237d5a13250c3eb95bfe741415a9da245585c78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079196"
---
# <a name="tb_insertmarkhittest-message"></a><span data-ttu-id="43e37-104">\_Mensaje INSERTMARKHITTEST TB</span><span class="sxs-lookup"><span data-stu-id="43e37-104">TB\_INSERTMARKHITTEST message</span></span>

<span data-ttu-id="43e37-105">Recupera la información de la marca de inserción para un punto de una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="43e37-105">Retrieves the insertion mark information for a point in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="43e37-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="43e37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43e37-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="43e37-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43e37-108">Puntero a una estructura de [**punto**](/previous-versions//dd162805(v=vs.85)) que contiene las coordenadas de la prueba de posicionamiento, en relación con el área cliente de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="43e37-108">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that contains the hit test coordinates, relative to the client area of the toolbar.</span></span>

</dd> <dt>

<span data-ttu-id="43e37-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="43e37-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43e37-110">Puntero a una estructura [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) que recibe la información de la marca de inserción.</span><span class="sxs-lookup"><span data-stu-id="43e37-110">Pointer to a [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) structure that receives the insertion mark information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43e37-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="43e37-111">Return value</span></span>

<span data-ttu-id="43e37-112">Devuelve un valor distinto de cero si el punto es una marca de inserción o cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="43e37-112">Returns nonzero if the point is an insertion mark, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="43e37-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43e37-113">Requirements</span></span>



| <span data-ttu-id="43e37-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="43e37-114">Requirement</span></span> | <span data-ttu-id="43e37-115">Value</span><span class="sxs-lookup"><span data-stu-id="43e37-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43e37-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43e37-116">Minimum supported client</span></span><br/> | <span data-ttu-id="43e37-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="43e37-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="43e37-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43e37-118">Minimum supported server</span></span><br/> | <span data-ttu-id="43e37-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="43e37-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="43e37-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="43e37-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="43e37-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="43e37-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

