---
title: Mensaje de RB_GETBANDINFO (commctrl. h)
description: Recupera información sobre una banda especificada en un control rebar.
ms.assetid: c2a76c91-7d44-4278-823d-bd263520e7a8
keywords:
- RB_GETBANDINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_GETBANDINFO
- RB_GETBANDINFOA
- RB_GETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b87715cf61b4eb2726eab83d500330721f41719f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150656"
---
# <a name="rb_getbandinfo-message"></a><span data-ttu-id="c897a-104">Mensaje de GETBANDINFO de RB \_</span><span class="sxs-lookup"><span data-stu-id="c897a-104">RB\_GETBANDINFO message</span></span>

<span data-ttu-id="c897a-105">Recupera información sobre una banda especificada en un control rebar.</span><span class="sxs-lookup"><span data-stu-id="c897a-105">Retrieves information about a specified band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c897a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c897a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c897a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c897a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c897a-108">Índice de base cero de la banda para la que se recuperará la información.</span><span class="sxs-lookup"><span data-stu-id="c897a-108">Zero-based index of the band for which the information will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="c897a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c897a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c897a-110">Puntero a una estructura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) que recibirá la información de la banda solicitada.</span><span class="sxs-lookup"><span data-stu-id="c897a-110">Pointer to a [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure that will receive the requested band information.</span></span> <span data-ttu-id="c897a-111">Antes de enviar este mensaje, debe establecer el miembro **cbSize** de esta estructura en el tamaño de la estructura **REBARBANDINFO** y establecer el miembro **fMask** en los elementos que desea recuperar.</span><span class="sxs-lookup"><span data-stu-id="c897a-111">Before sending this message, you must set the **cbSize** member of this structure to the size of the **REBARBANDINFO** structure and set the **fMask** member to the items you want to retrieve.</span></span> <span data-ttu-id="c897a-112">Además, debe establecer el miembro **CCH** de la estructura **REBARBANDINFO** en el tamaño del búfer **lpText** cuando \_ se especifica RBBIM Text.</span><span class="sxs-lookup"><span data-stu-id="c897a-112">Additionally, you must set the **cch** member of the **REBARBANDINFO** structure to the size of the **lpText** buffer when RBBIM\_TEXT is specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c897a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c897a-113">Return value</span></span>

<span data-ttu-id="c897a-114">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="c897a-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c897a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c897a-115">Requirements</span></span>



| <span data-ttu-id="c897a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c897a-116">Requirement</span></span> | <span data-ttu-id="c897a-117">Value</span><span class="sxs-lookup"><span data-stu-id="c897a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c897a-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c897a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c897a-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c897a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c897a-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c897a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c897a-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c897a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c897a-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c897a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c897a-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c897a-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="c897a-124">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="c897a-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c897a-125">**RB \_ GETBANDINFOW** (Unicode) y **RB \_ GETBANDINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c897a-125">**RB\_GETBANDINFOW** (Unicode) and **RB\_GETBANDINFOA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="c897a-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="c897a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c897a-127">**\_SETBANDINFO RB**</span><span class="sxs-lookup"><span data-stu-id="c897a-127">**RB\_SETBANDINFO**</span></span>](rb-setbandinfo.md)
</dt> </dl>

 

 





