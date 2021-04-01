---
title: Mensaje de HDM_HITTEST (commctrl. h)
description: Comprueba un punto para determinar qué elemento de encabezado, si existe, está en el punto especificado.
ms.assetid: ff866bd1-9f2a-457c-921d-549610ab9088
keywords:
- HDM_HITTEST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b6634396dbd5ecd4510a4f7341fc6380dbb0ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150553"
---
# <a name="hdm_hittest-message"></a><span data-ttu-id="0008d-104">HDM \_ mensaje HITTEST</span><span class="sxs-lookup"><span data-stu-id="0008d-104">HDM\_HITTEST message</span></span>

<span data-ttu-id="0008d-105">Comprueba un punto para determinar qué elemento de encabezado, si existe, está en el punto especificado.</span><span class="sxs-lookup"><span data-stu-id="0008d-105">Tests a point to determine which header item, if any, is at the specified point.</span></span>

## <a name="parameters"></a><span data-ttu-id="0008d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0008d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0008d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0008d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0008d-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="0008d-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0008d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0008d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0008d-110">Puntero a una estructura [**HDHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-hdhittestinfo) que contiene la posición que se va a probar y recibe información sobre los resultados de la prueba.</span><span class="sxs-lookup"><span data-stu-id="0008d-110">A pointer to an [**HDHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-hdhittestinfo) structure that contains the position to test and receives information about the results of the test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0008d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0008d-111">Return value</span></span>

<span data-ttu-id="0008d-112">Devuelve el índice del elemento en la posición especificada, si existe, o en 1 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0008d-112">Returns the index of the item at the specified position, if any, or   1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0008d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0008d-113">Requirements</span></span>



| <span data-ttu-id="0008d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0008d-114">Requirement</span></span> | <span data-ttu-id="0008d-115">Value</span><span class="sxs-lookup"><span data-stu-id="0008d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0008d-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0008d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0008d-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0008d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0008d-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0008d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0008d-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0008d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0008d-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0008d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0008d-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0008d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





