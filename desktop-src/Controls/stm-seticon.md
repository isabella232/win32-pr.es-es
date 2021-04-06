---
title: Mensaje de STM_SETICON (Winuser. h)
description: Una aplicación envía el \_ mensaje STM SETICON para asociar un icono a un control de icono.
ms.assetid: 105b0667-8e23-47ed-9fb1-0792a22d7100
keywords:
- STM_SETICON controles de mensajes de Windows
topic_type:
- apiref
api_name:
- STM_SETICON
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9c7e2a007c1f866a1c73b3a1c1a55b157add47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078924"
---
# <a name="stm_seticon-message"></a><span data-ttu-id="f5ce2-104">\_Mensaje SETICON de STM</span><span class="sxs-lookup"><span data-stu-id="f5ce2-104">STM\_SETICON message</span></span>

<span data-ttu-id="f5ce2-105">Una aplicación envía el mensaje **STM \_ SETICON** para asociar un icono a un control de icono.</span><span class="sxs-lookup"><span data-stu-id="f5ce2-105">An application sends the **STM\_SETICON** message to associate an icon with an icon control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f5ce2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f5ce2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5ce2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f5ce2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5ce2-108">Identificador del icono que se va a asociar al control de icono.</span><span class="sxs-lookup"><span data-stu-id="f5ce2-108">Handle to the icon to associate with the icon control.</span></span>

</dd> <dt>

<span data-ttu-id="f5ce2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f5ce2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5ce2-110">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f5ce2-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5ce2-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f5ce2-111">Return value</span></span>

<span data-ttu-id="f5ce2-112">El valor devuelto es un identificador del icono asociado anteriormente al control de icono o cero si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="f5ce2-112">The return value is a handle to the icon previously associated with the icon control, or zero if an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5ce2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5ce2-113">Requirements</span></span>



| <span data-ttu-id="f5ce2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5ce2-114">Requirement</span></span> | <span data-ttu-id="f5ce2-115">Value</span><span class="sxs-lookup"><span data-stu-id="f5ce2-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5ce2-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5ce2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f5ce2-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f5ce2-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f5ce2-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5ce2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f5ce2-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f5ce2-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f5ce2-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5ce2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5ce2-121"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f5ce2-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5ce2-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5ce2-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="f5ce2-123">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="f5ce2-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f5ce2-124">**STM \_ GETICON**</span><span class="sxs-lookup"><span data-stu-id="f5ce2-124">**STM\_GETICON**</span></span>](stm-geticon.md)
</dt> <dt>

<span data-ttu-id="f5ce2-125">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="f5ce2-125">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="f5ce2-126">**LoadIcon**</span><span class="sxs-lookup"><span data-stu-id="f5ce2-126">**LoadIcon**</span></span>](/windows/desktop/api/winuser/nf-winuser-loadicona)
</dt> </dl>

 

