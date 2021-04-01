---
title: Mensaje de TB_REPLACEBITMAP (commctrl. h)
description: Reemplaza un mapa de bits existente por un nuevo mapa de bits.
ms.assetid: abad5c7a-ebdd-46b5-a465-fe64ff8eb127
keywords:
- TB_REPLACEBITMAP controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_REPLACEBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0216d73f70f9bef8230d7e725834d63d60012798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905449"
---
# <a name="tb_replacebitmap-message"></a><span data-ttu-id="45e02-104">\_Mensaje REPLACEBITMAP TB</span><span class="sxs-lookup"><span data-stu-id="45e02-104">TB\_REPLACEBITMAP message</span></span>

<span data-ttu-id="45e02-105">Reemplaza un mapa de bits existente por un nuevo mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="45e02-105">Replaces an existing bitmap with a new bitmap.</span></span>

## <a name="parameters"></a><span data-ttu-id="45e02-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45e02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45e02-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="45e02-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="45e02-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="45e02-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="45e02-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="45e02-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="45e02-110">Puntero a una estructura [**TBREPLACEBITMAP**](/windows/desktop/api/Commctrl/ns-commctrl-tbreplacebitmap) que contiene la información del mapa de bits que se va a reemplazar y el nuevo mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="45e02-110">Pointer to a [**TBREPLACEBITMAP**](/windows/desktop/api/Commctrl/ns-commctrl-tbreplacebitmap) structure that contains the information of the bitmap to be replaced and the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45e02-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45e02-111">Return value</span></span>

<span data-ttu-id="45e02-112">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="45e02-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="45e02-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45e02-113">Requirements</span></span>



| <span data-ttu-id="45e02-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="45e02-114">Requirement</span></span> | <span data-ttu-id="45e02-115">Value</span><span class="sxs-lookup"><span data-stu-id="45e02-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="45e02-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45e02-116">Minimum supported client</span></span><br/> | <span data-ttu-id="45e02-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="45e02-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="45e02-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45e02-118">Minimum supported server</span></span><br/> | <span data-ttu-id="45e02-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="45e02-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="45e02-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="45e02-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="45e02-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="45e02-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





