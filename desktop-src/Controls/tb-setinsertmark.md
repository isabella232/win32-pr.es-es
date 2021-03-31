---
title: Mensaje de TB_SETINSERTMARK (commctrl. h)
description: Establece la marca de inserción actual de la barra de herramientas.
ms.assetid: 9a576fca-89cf-4db5-9840-35bfa56af89e
keywords:
- TB_SETINSERTMARK controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f65ba83d13cbb45f54833725a46de61a5f0444c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149887"
---
# <a name="tb_setinsertmark-message"></a><span data-ttu-id="63651-104">\_Mensaje SETINSERTMARK TB</span><span class="sxs-lookup"><span data-stu-id="63651-104">TB\_SETINSERTMARK message</span></span>

<span data-ttu-id="63651-105">Establece la marca de inserción actual de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="63651-105">Sets the current insertion mark for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="63651-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63651-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63651-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="63651-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="63651-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="63651-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="63651-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="63651-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63651-110">Puntero a una estructura [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) que contiene la marca de inserción.</span><span class="sxs-lookup"><span data-stu-id="63651-110">Pointer to a [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) structure that contains the insertion mark.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63651-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63651-111">Return value</span></span>

<span data-ttu-id="63651-112">No se utiliza el valor devuelto para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="63651-112">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="63651-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63651-113">Requirements</span></span>



| <span data-ttu-id="63651-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="63651-114">Requirement</span></span> | <span data-ttu-id="63651-115">Value</span><span class="sxs-lookup"><span data-stu-id="63651-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63651-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63651-116">Minimum supported client</span></span><br/> | <span data-ttu-id="63651-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="63651-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="63651-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63651-118">Minimum supported server</span></span><br/> | <span data-ttu-id="63651-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="63651-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="63651-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63651-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="63651-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="63651-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63651-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="63651-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63651-123">**TB \_ GETINSERTMARK**</span><span class="sxs-lookup"><span data-stu-id="63651-123">**TB\_GETINSERTMARK**</span></span>](tb-getinsertmark.md)
</dt> </dl>

 

 





