---
description: Difundir a cada ventana después de un evento de cambio de tema. Algunos ejemplos de eventos de cambio de tema son la activación de un tema, la desactivación de un tema o una transición de un tema a otro.
ms.assetid: 1a4051ac-cc6e-4520-ab66-d0a41a8a4c73
title: Mensaje de WM_THEMECHANGED (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bc15ab64126ff8972b858ef43ddd4d92cd62f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809548"
---
# <a name="wm_themechanged-message"></a><span data-ttu-id="ea1b9-104">Mensaje de THEMECHANGED de WM \_</span><span class="sxs-lookup"><span data-stu-id="ea1b9-104">WM\_THEMECHANGED message</span></span>

<span data-ttu-id="ea1b9-105">Difundir a cada ventana después de un evento de cambio de tema.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-105">Broadcast to every window following a theme change event.</span></span> <span data-ttu-id="ea1b9-106">Algunos ejemplos de eventos de cambio de tema son la activación de un tema, la desactivación de un tema o una transición de un tema a otro.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-106">Examples of theme change events are the activation of a theme, the deactivation of a theme, or a transition from one theme to another.</span></span>


```C++
#define WM_THEMECHANGED                 0x031A
```



## <a name="parameters"></a><span data-ttu-id="ea1b9-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ea1b9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea1b9-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea1b9-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea1b9-109">Este parámetro está reservado.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-109">This parameter is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ea1b9-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea1b9-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea1b9-111">Este parámetro está reservado.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-111">This parameter is reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea1b9-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ea1b9-112">Return value</span></span>

<span data-ttu-id="ea1b9-113">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="ea1b9-113">Type: **LRESULT**</span></span>

<span data-ttu-id="ea1b9-114">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-114">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea1b9-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ea1b9-115">Remarks</span></span>

<span data-ttu-id="ea1b9-116">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ea1b9-116">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> [!Note]  
> <span data-ttu-id="ea1b9-117">Este mensaje lo envía el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-117">This message is posted by the operating system.</span></span> <span data-ttu-id="ea1b9-118">Normalmente, las aplicaciones no envían este mensaje.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-118">Applications typically do not send this message.</span></span>

 

<span data-ttu-id="ea1b9-119">Los temas son especificaciones para la apariencia de los controles, de modo que el elemento visual de un control se trata por separado de su funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-119">Themes are specifications for the appearance of controls, so that the visual element of a control is treated separately from its functionality.</span></span>

<span data-ttu-id="ea1b9-120">Para liberar un identificador de tema existente, llame a [**CloseThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata).</span><span class="sxs-lookup"><span data-stu-id="ea1b9-120">To release an existing theme handle, call [**CloseThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata).</span></span> <span data-ttu-id="ea1b9-121">Para adquirir un nuevo identificador de tema, use [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata).</span><span class="sxs-lookup"><span data-stu-id="ea1b9-121">To acquire a new theme handle, use [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata).</span></span>

<span data-ttu-id="ea1b9-122">Después de la difusión **\_ THEMECHANGED de WM** , cualquier controlador de tema existente no es válido.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-122">Following the **WM\_THEMECHANGED** broadcast, any existing theme handles are invalid.</span></span> <span data-ttu-id="ea1b9-123">Una ventana que tenga en cuenta el tema debe liberar y volver a abrir cualquiera de sus identificadores de tema ya existentes cuando reciba el mensaje de **\_ THEMECHANGED de WM** .</span><span class="sxs-lookup"><span data-stu-id="ea1b9-123">A theme-aware window should release and reopen any of its pre-existing theme handles when it receives the **WM\_THEMECHANGED** message.</span></span> <span data-ttu-id="ea1b9-124">Si la función [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata) devuelve un **valor null**, la ventana debe pintarse como desactivada.</span><span class="sxs-lookup"><span data-stu-id="ea1b9-124">If the [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata) function returns **NULL**, the window should paint unthemed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea1b9-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea1b9-125">Requirements</span></span>



| <span data-ttu-id="ea1b9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea1b9-126">Requirement</span></span> | <span data-ttu-id="ea1b9-127">Value</span><span class="sxs-lookup"><span data-stu-id="ea1b9-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea1b9-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea1b9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ea1b9-129">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="ea1b9-129">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ea1b9-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea1b9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ea1b9-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ea1b9-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ea1b9-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea1b9-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea1b9-133"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea1b9-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea1b9-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea1b9-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="ea1b9-135">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="ea1b9-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="ea1b9-136">**CloseThemeData**</span><span class="sxs-lookup"><span data-stu-id="ea1b9-136">**CloseThemeData**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata)
</dt> <dt>

[<span data-ttu-id="ea1b9-137">**IsThemeActive**</span><span class="sxs-lookup"><span data-stu-id="ea1b9-137">**IsThemeActive**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-isthemeactive)
</dt> <dt>

[<span data-ttu-id="ea1b9-138">**OpenThemeData**</span><span class="sxs-lookup"><span data-stu-id="ea1b9-138">**OpenThemeData**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata)
</dt> </dl>

 

 
