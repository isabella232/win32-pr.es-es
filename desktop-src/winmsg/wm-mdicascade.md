---
description: Una aplicación envía el mensaje de MDICASCADE de WM \_ a una ventana de cliente de la interfaz de múltiples documentos (MDI) para organizar todas sus ventanas secundarias en un formato en cascada.
ms.assetid: 33d04859-4220-40a6-be46-74a812a44ca8
title: Mensaje de WM_MDICASCADE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6208ce924ab6185399f3f673a435e1fbaca2741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360239"
---
# <a name="wm_mdicascade-message"></a><span data-ttu-id="0a69c-103">Mensaje de MDICASCADE de WM \_</span><span class="sxs-lookup"><span data-stu-id="0a69c-103">WM\_MDICASCADE message</span></span>

<span data-ttu-id="0a69c-104">Una aplicación envía el mensaje de **\_ MDICASCADE de WM** a una ventana de cliente de la interfaz de múltiples documentos (MDI) para organizar todas sus ventanas secundarias en un formato en cascada.</span><span class="sxs-lookup"><span data-stu-id="0a69c-104">An application sends the **WM\_MDICASCADE** message to a multiple-document interface (MDI) client window to arrange all its child windows in a cascade format.</span></span>


```C++
#define WM_MDICASCADE                   0x0227
```



## <a name="parameters"></a><span data-ttu-id="0a69c-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a69c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a69c-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0a69c-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0a69c-107">Comportamiento en cascada.</span><span class="sxs-lookup"><span data-stu-id="0a69c-107">The cascade behavior.</span></span> <span data-ttu-id="0a69c-108">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="0a69c-108">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="0a69c-109">Value</span><span class="sxs-lookup"><span data-stu-id="0a69c-109">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="0a69c-110">Significado</span><span class="sxs-lookup"><span data-stu-id="0a69c-110">Meaning</span></span>                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span id="MDITILE_SKIPDISABLED"></span><span id="mditile_skipdisabled"></span><dl> <span data-ttu-id="0a69c-111"><dt>**MDITILE \_ SKIPDISABLED**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="0a69c-111"><dt>**MDITILE\_SKIPDISABLED**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="0a69c-112">Impide que las ventanas secundarias MDI deshabilitadas se puedan poner en cascada.</span><span class="sxs-lookup"><span data-stu-id="0a69c-112">Prevents disabled MDI child windows from being cascaded.</span></span> <br/> |
| <span id="MDITILE_ZORDER"></span><span id="mditile_zorder"></span><dl> <span data-ttu-id="0a69c-113"><dt>**MDITILE \_ ZORDER**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="0a69c-113"><dt>**MDITILE\_ZORDER**</dt> <dt>0x0004</dt></span></span> </dl>                   | <span data-ttu-id="0a69c-114">Organiza las ventanas en orden Z.</span><span class="sxs-lookup"><span data-stu-id="0a69c-114">Arranges the windows in Z order.</span></span><br/>                          |



 

</dd> <dt>

<span data-ttu-id="0a69c-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0a69c-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0a69c-116">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="0a69c-116">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a69c-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0a69c-117">Return value</span></span>

<span data-ttu-id="0a69c-118">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="0a69c-118">Type: **BOOL**</span></span>

<span data-ttu-id="0a69c-119">Si el mensaje se realiza correctamente, el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="0a69c-119">If the message succeeds, the return value is **TRUE**.</span></span>

<span data-ttu-id="0a69c-120">Si se produce un error en el mensaje, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="0a69c-120">If the message fails, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a69c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a69c-121">Requirements</span></span>



| <span data-ttu-id="0a69c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a69c-122">Requirement</span></span> | <span data-ttu-id="0a69c-123">Value</span><span class="sxs-lookup"><span data-stu-id="0a69c-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a69c-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a69c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0a69c-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0a69c-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0a69c-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a69c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0a69c-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0a69c-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0a69c-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0a69c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a69c-129"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a69c-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a69c-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a69c-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="0a69c-131">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="0a69c-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0a69c-132">**MDIICONARRANGE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="0a69c-132">**WM\_MDIICONARRANGE**</span></span>](wm-mdiiconarrange.md)
</dt> <dt>

[<span data-ttu-id="0a69c-133">**MDITILE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="0a69c-133">**WM\_MDITILE**</span></span>](wm-mditile.md)
</dt> <dt>

<span data-ttu-id="0a69c-134">**Vista**</span><span class="sxs-lookup"><span data-stu-id="0a69c-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0a69c-135">Interfaz de varios documentos</span><span class="sxs-lookup"><span data-stu-id="0a69c-135">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




