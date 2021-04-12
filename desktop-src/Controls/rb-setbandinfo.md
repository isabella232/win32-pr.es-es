---
title: Mensaje de RB_SETBANDINFO (commctrl. h)
description: Establece las características de una banda existente en un control rebar.
ms.assetid: 00021c35-612d-4278-b10c-6e9f1f45a543
keywords:
- RB_SETBANDINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_SETBANDINFO
- RB_SETBANDINFOA
- RB_SETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92e81377a40f8b6054f5d8cfae16837621b77b61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491758"
---
# <a name="rb_setbandinfo-message"></a><span data-ttu-id="b8384-104">Mensaje de SETBANDINFO de RB \_</span><span class="sxs-lookup"><span data-stu-id="b8384-104">RB\_SETBANDINFO message</span></span>

<span data-ttu-id="b8384-105">Establece las características de una banda existente en un control rebar.</span><span class="sxs-lookup"><span data-stu-id="b8384-105">Sets characteristics of an existing band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b8384-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8384-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8384-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b8384-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8384-108">Índice de base cero de la banda que va a recibir la nueva configuración.</span><span class="sxs-lookup"><span data-stu-id="b8384-108">Zero-based index of the band to receive the new settings.</span></span>

</dd> <dt>

<span data-ttu-id="b8384-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8384-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8384-110">Puntero a una estructura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) que define la banda que se va a modificar y la nueva configuración.</span><span class="sxs-lookup"><span data-stu-id="b8384-110">Pointer to a [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure that defines the band to be modified and the new settings.</span></span> <span data-ttu-id="b8384-111">Antes de enviar este mensaje, debe establecer el miembro **cbSize** de esta estructura en la estructura **sizeof**(REBARBANDINFO).</span><span class="sxs-lookup"><span data-stu-id="b8384-111">Before sending this message, you must set the **cbSize** member of this structure to the **sizeof**(REBARBANDINFO) structure.</span></span> <span data-ttu-id="b8384-112">Además, debe establecer el miembro **CCH** de la estructura **REBARBANDINFO** en el tamaño del búfer **lpText** cuando \_ se especifica RBBIM Text.</span><span class="sxs-lookup"><span data-stu-id="b8384-112">Additionally, you must set the **cch** member of the **REBARBANDINFO** structure to the size of the **lpText** buffer when RBBIM\_TEXT is specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8384-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b8384-113">Return value</span></span>

<span data-ttu-id="b8384-114">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="b8384-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8384-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8384-115">Requirements</span></span>



| <span data-ttu-id="b8384-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8384-116">Requirement</span></span> | <span data-ttu-id="b8384-117">Value</span><span class="sxs-lookup"><span data-stu-id="b8384-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8384-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8384-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b8384-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b8384-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b8384-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8384-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b8384-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b8384-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b8384-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b8384-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8384-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8384-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="b8384-124">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="b8384-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b8384-125">**RB \_ SETBANDINFOW** (Unicode) y **RB \_ SETBANDINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b8384-125">**RB\_SETBANDINFOW** (Unicode) and **RB\_SETBANDINFOA** (ANSI)</span></span><br/>             |



 

 





