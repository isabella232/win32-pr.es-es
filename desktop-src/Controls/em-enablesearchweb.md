---
title: Mensaje de EM_ENABLESEARCHWEB (CommCtrl. h)
description: Habilita o deshabilita la característica "Buscar en la web" y la entrada del menú contextual.
ms.assetid: 9393f03e-0719-458b-8122-616df738c417
keywords:
- EM_ENABLESEARCHWEB controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_ENABLESEARCHWEB
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdb2638476027f0a7fe2bb1a66a3a00a330e28c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996650"
---
# <a name="em_enablesearchweb-message"></a><span data-ttu-id="e31cc-104">\_Mensaje ENABLESEARCHWEB em</span><span class="sxs-lookup"><span data-stu-id="e31cc-104">EM\_ENABLESEARCHWEB message</span></span>

<span data-ttu-id="e31cc-105">Habilita o deshabilita la característica "Buscar en la web" y la entrada del menú contextual.</span><span class="sxs-lookup"><span data-stu-id="e31cc-105">Enables or disables the "Search the web" feature and context menu entry.</span></span>

## <a name="parameters"></a><span data-ttu-id="e31cc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e31cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e31cc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e31cc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e31cc-108">Un valor de **true** indica que la característica "Buscar en la web" está habilitada y un valor de **false** indica que está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="e31cc-108">A value of **TRUE** indicates the "Search the web" feature is enabled, and a value of **FALSE** indicates it is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="e31cc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e31cc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e31cc-110">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="e31cc-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e31cc-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e31cc-111">Return value</span></span>

<span data-ttu-id="e31cc-112">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e31cc-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e31cc-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e31cc-113">Remarks</span></span>

<span data-ttu-id="e31cc-114">Si deshabilita "Buscar en la web" con este mensaje, el [**mensaje \_ SEARCHWEB em**](em-searchweb.md) no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="e31cc-114">If you disable "Search the web" using this message, the [**EM\_SEARCHWEB**](em-searchweb.md) message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="e31cc-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e31cc-115">Requirements</span></span>



| <span data-ttu-id="e31cc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e31cc-116">Requirement</span></span> | <span data-ttu-id="e31cc-117">Value</span><span class="sxs-lookup"><span data-stu-id="e31cc-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e31cc-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e31cc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e31cc-119">Solo aplicaciones de escritorio de Windows 10 y 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="e31cc-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e31cc-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e31cc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e31cc-121">Solo aplicaciones de escritorio de Windows Server 2019 \[\]</span><span class="sxs-lookup"><span data-stu-id="e31cc-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e31cc-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e31cc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e31cc-123"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e31cc-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e31cc-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="e31cc-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="e31cc-125">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="e31cc-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e31cc-126">**\_SEARCHWEB em**</span><span class="sxs-lookup"><span data-stu-id="e31cc-126">**EM\_SEARCHWEB**</span></span>](em-searchweb.md)
</dt> </dl>

 

 





