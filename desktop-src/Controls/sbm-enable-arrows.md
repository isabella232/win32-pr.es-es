---
title: Mensaje de SBM_ENABLE_ARROWS (Winuser. h)
description: Una aplicación envía el \_ mensaje de \_ flechas habilitar SBM para habilitar o deshabilitar una o ambas flechas de un control de barra de desplazamiento.
ms.assetid: 9646826a-3a7c-490b-822d-7511e4ef2262
keywords:
- SBM_ENABLE_ARROWS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SBM_ENABLE_ARROWS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78895b43ec7908172a6164917b33ac8549088db4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996807"
---
# <a name="sbm_enable_arrows-message"></a><span data-ttu-id="34cc1-104">\_Mensaje de flechas habilitadas de SBM \_</span><span class="sxs-lookup"><span data-stu-id="34cc1-104">SBM\_ENABLE\_ARROWS message</span></span>

<span data-ttu-id="34cc1-105">Una aplicación envía el mensaje de **\_ \_ flechas habilitar SBM** para habilitar o deshabilitar una o ambas flechas de un control de barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="34cc1-105">An application sends the **SBM\_ENABLE\_ARROWS** message to enable or disable one or both arrows of a scroll bar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="34cc1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="34cc1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34cc1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="34cc1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="34cc1-108">Especifica si las flechas de la barra de desplazamiento están habilitadas o deshabilitadas e indica qué flechas están habilitadas o deshabilitadas.</span><span class="sxs-lookup"><span data-stu-id="34cc1-108">Specifies whether the scroll bar arrows are enabled or disabled and indicates which arrows are enabled or disabled.</span></span> <span data-ttu-id="34cc1-109">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="34cc1-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="34cc1-110">Valor</span><span class="sxs-lookup"><span data-stu-id="34cc1-110">Value</span></span>                                                                                                                                                                   | <span data-ttu-id="34cc1-111">Significado</span><span class="sxs-lookup"><span data-stu-id="34cc1-111">Meaning</span></span>                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="ESB_DISABLE_BOTH"></span><span id="esb_disable_both"></span><dl> <span data-ttu-id="34cc1-112"><dt>**ESB \_ deshabilitar \_ ambas**</dt></span><span class="sxs-lookup"><span data-stu-id="34cc1-112"><dt>**ESB\_DISABLE\_BOTH**</dt></span></span> </dl> | <span data-ttu-id="34cc1-113">Deshabilita ambas flechas en una barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="34cc1-113">Disables both arrows on a scroll bar.</span></span><br/>                                                           |
| <span id="ESB_DISABLE_DOWN"></span><span id="esb_disable_down"></span><dl> <span data-ttu-id="34cc1-114"><dt>**deshabilitar ESB \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="34cc1-114"><dt>**ESB\_DISABLE\_DOWN**</dt></span></span> </dl> | <span data-ttu-id="34cc1-115">Deshabilita la flecha hacia abajo de una barra de desplazamiento vertical.</span><span class="sxs-lookup"><span data-stu-id="34cc1-115">Disables the down arrow on a vertical scroll bar.</span></span><br/>                                               |
| <span id="ESB_DISABLE_LTUP"></span><span id="esb_disable_ltup"></span><dl> <span data-ttu-id="34cc1-116"><dt>**ESB \_ Disable \_ LTUP**</dt></span><span class="sxs-lookup"><span data-stu-id="34cc1-116"><dt>**ESB\_DISABLE\_LTUP**</dt></span></span> </dl> | <span data-ttu-id="34cc1-117">Deshabilita la flecha izquierda en una barra de desplazamiento horizontal o en la flecha hacia arriba de una barra de desplazamiento vertical.</span><span class="sxs-lookup"><span data-stu-id="34cc1-117">Disables the left arrow on a horizontal scroll bar or the up arrow on a vertical scroll bar.</span></span><br/>    |
| <span id="ESB_DISABLE_LEFT"></span><span id="esb_disable_left"></span><dl> <span data-ttu-id="34cc1-118"><dt>**\_deshabilitación ESB \_ izquierda**</dt></span><span class="sxs-lookup"><span data-stu-id="34cc1-118"><dt>**ESB\_DISABLE\_LEFT**</dt></span></span> </dl> | <span data-ttu-id="34cc1-119">Deshabilita la flecha izquierda en una barra de desplazamiento horizontal.</span><span class="sxs-lookup"><span data-stu-id="34cc1-119">Disables the left arrow on a horizontal scroll bar.</span></span><br/>                                             |
| <span id="ESB_DISABLE_RTDN"></span><span id="esb_disable_rtdn"></span><dl> <span data-ttu-id="34cc1-120"><dt>**ESB \_ Disable \_ RTDN**</dt></span><span class="sxs-lookup"><span data-stu-id="34cc1-120"><dt>**ESB\_DISABLE\_RTDN**</dt></span></span> </dl> | <span data-ttu-id="34cc1-121">Deshabilita la flecha derecha en una barra de desplazamiento horizontal o en la flecha hacia abajo de una barra de desplazamiento vertical.</span><span class="sxs-lookup"><span data-stu-id="34cc1-121">Disables the right arrow on a horizontal scroll bar or the down arrow on a vertical scroll bar.</span></span><br/> |
| <span id="ESB_DISABLE_UP"></span><span id="esb_disable_up"></span><dl> <span data-ttu-id="34cc1-122"><dt>**deshabilitar ESB \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="34cc1-122"><dt>**ESB\_DISABLE\_UP**</dt></span></span> </dl>       | <span data-ttu-id="34cc1-123">Deshabilita la flecha arriba en una barra de desplazamiento vertical.</span><span class="sxs-lookup"><span data-stu-id="34cc1-123">Disables the up arrow on a vertical scroll bar.</span></span><br/>                                                 |
| <span id="ESB_ENABLE_BOTH"></span><span id="esb_enable_both"></span><dl> <span data-ttu-id="34cc1-124"><dt>**ESB \_ habilitar \_ ambos**</dt></span><span class="sxs-lookup"><span data-stu-id="34cc1-124"><dt>**ESB\_ENABLE\_BOTH**</dt></span></span> </dl>    | <span data-ttu-id="34cc1-125">Habilita ambas flechas en una barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="34cc1-125">Enables both arrows on a scroll bar.</span></span><br/>                                                            |



 

</dd> <dt>

<span data-ttu-id="34cc1-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="34cc1-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="34cc1-127">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="34cc1-127">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34cc1-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="34cc1-128">Return value</span></span>

<span data-ttu-id="34cc1-129">Si el mensaje se realiza correctamente, el valor devuelto es **true**; de lo contrario, es **false**.</span><span class="sxs-lookup"><span data-stu-id="34cc1-129">If the message succeeds, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="34cc1-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34cc1-130">Requirements</span></span>



| <span data-ttu-id="34cc1-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="34cc1-131">Requirement</span></span> | <span data-ttu-id="34cc1-132">Value</span><span class="sxs-lookup"><span data-stu-id="34cc1-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34cc1-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34cc1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="34cc1-134">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="34cc1-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="34cc1-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34cc1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="34cc1-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="34cc1-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="34cc1-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="34cc1-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="34cc1-138"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34cc1-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





