---
title: Mensaje de RB_GETRECT (commctrl. h)
description: Recupera el rectángulo delimitador de una banda determinada en un control rebar.
ms.assetid: e272b090-1e4d-4cff-87f0-557ad8116e7e
keywords:
- RB_GETRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b9d5de00b638a3767df461595ff01316b23183
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274527"
---
# <a name="rb_getrect-message"></a><span data-ttu-id="8af07-104">Mensaje de GETRECT de RB \_</span><span class="sxs-lookup"><span data-stu-id="8af07-104">RB\_GETRECT message</span></span>

<span data-ttu-id="8af07-105">Recupera el rectángulo delimitador de una banda determinada en un control rebar.</span><span class="sxs-lookup"><span data-stu-id="8af07-105">Retrieves the bounding rectangle for a given band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8af07-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8af07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8af07-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8af07-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8af07-108">Índice de base cero de una banda del control rebar.</span><span class="sxs-lookup"><span data-stu-id="8af07-108">Zero-based index of a band in the rebar control.</span></span>

</dd> <dt>

<span data-ttu-id="8af07-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8af07-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8af07-110">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recibirá los límites de la banda rebar.</span><span class="sxs-lookup"><span data-stu-id="8af07-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the bounds of the rebar band.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8af07-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8af07-111">Return value</span></span>

<span data-ttu-id="8af07-112">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="8af07-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8af07-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8af07-113">Requirements</span></span>



| <span data-ttu-id="8af07-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8af07-114">Requirement</span></span> | <span data-ttu-id="8af07-115">Value</span><span class="sxs-lookup"><span data-stu-id="8af07-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8af07-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8af07-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8af07-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8af07-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8af07-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8af07-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8af07-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8af07-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8af07-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8af07-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8af07-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8af07-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

