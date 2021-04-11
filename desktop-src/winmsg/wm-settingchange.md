---
description: Un mensaje que se envía a todas las ventanas de nivel superior cuando la función SystemParametersInfo cambia una configuración de todo el sistema o cuando la configuración de Directiva ha cambiado.
ms.assetid: 77174e06-a25b-440a-9e9c-4fd5979c433c
title: Mensaje de WM_SETTINGCHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1c3d1360b5e4cc5de2dbd23b09b8f2ad034948f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279017"
---
# <a name="wm_settingchange-message"></a><span data-ttu-id="fc3dc-103">Mensaje de SETTINGCHANGE de WM \_</span><span class="sxs-lookup"><span data-stu-id="fc3dc-103">WM\_SETTINGCHANGE message</span></span>

<span data-ttu-id="fc3dc-104">Un mensaje que se envía a todas las ventanas de nivel superior cuando la función [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) cambia una configuración de todo el sistema o cuando la configuración de Directiva ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="fc3dc-104">A message that is sent to all top-level windows when the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function changes a system-wide setting or when policy settings have changed.</span></span>

<span data-ttu-id="fc3dc-105">Las aplicaciones deben enviar **WM \_ SETTINGCHANGE** a todas las ventanas de nivel superior cuando realizan cambios en los parámetros del sistema.</span><span class="sxs-lookup"><span data-stu-id="fc3dc-105">Applications should send **WM\_SETTINGCHANGE** to all top-level windows when they make changes to system parameters.</span></span> <span data-ttu-id="fc3dc-106">(Este mensaje no se puede enviar directamente a una ventana). Para enviar el mensaje de **\_ SETTINGCHANGE de WM** a todas las ventanas de nivel superior, use la función [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) con el parámetro *hWnd* establecido en la **\_ difusión HWND**.</span><span class="sxs-lookup"><span data-stu-id="fc3dc-106">(This message cannot be sent directly to a window.) To send the **WM\_SETTINGCHANGE** message to all top-level windows, use the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function with the *hwnd* parameter set to **HWND\_BROADCAST**.</span></span>

<span data-ttu-id="fc3dc-107">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="fc3dc-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_WININICHANGE                 0x001A
#define WM_SETTINGCHANGE                WM_WININICHANGE
```



## <a name="parameters"></a><span data-ttu-id="fc3dc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fc3dc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc3dc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fc3dc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc3dc-110">Cuando el sistema envía este mensaje como resultado de una llamada [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) , el parámetro *wParam* es el valor del parámetro *uiAction* que se pasa a la función **SystemParametersInfo** .</span><span class="sxs-lookup"><span data-stu-id="fc3dc-110">When the system sends this message as a result of a [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) call, the *wParam* parameter is the value of the *uiAction* parameter passed to the **SystemParametersInfo** function.</span></span> <span data-ttu-id="fc3dc-111">Para obtener una lista de valores, vea **SystemParametersInfo**.</span><span class="sxs-lookup"><span data-stu-id="fc3dc-111">For a list of values, see **SystemParametersInfo**.</span></span>

<span data-ttu-id="fc3dc-112">Cuando el sistema envía este mensaje como resultado de un cambio en la configuración de la Directiva, este parámetro indica el tipo de directiva que se ha aplicado.</span><span class="sxs-lookup"><span data-stu-id="fc3dc-112">When the system sends this message as a result of a change in policy settings, this parameter indicates the type of policy that was applied.</span></span> <span data-ttu-id="fc3dc-113">Este valor es 1 si se ha aplicado la Directiva de equipo o cero si se ha aplicado la Directiva de usuario.</span><span class="sxs-lookup"><span data-stu-id="fc3dc-113">This value is 1 if computer policy was applied or zero if user policy was applied.</span></span>

<span data-ttu-id="fc3dc-114">Cuando el sistema envía este mensaje como resultado de un cambio en la configuración regional, este parámetro es cero.</span><span class="sxs-lookup"><span data-stu-id="fc3dc-114">When the system sends this message as a result of a change in locale settings, this parameter is zero.</span></span>

<span data-ttu-id="fc3dc-115">Cuando una aplicación envía este mensaje, este parámetro debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="fc3dc-115">When an application sends this message, this parameter must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fc3dc-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fc3dc-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc3dc-117">Cuando el sistema envía este mensaje como resultado de una llamada [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) , *lParam* es un puntero a una cadena que indica el área que contiene el parámetro del sistema que se ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="fc3dc-117">When the system sends this message as a result of a [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) call, *lParam* is a pointer to a string that indicates the area containing the system parameter that was changed.</span></span> <span data-ttu-id="fc3dc-118">Normalmente, este parámetro no indica qué parámetro del sistema concreto cambió.</span><span class="sxs-lookup"><span data-stu-id="fc3dc-118">This parameter does not usually indicate which specific system parameter changed.</span></span> <span data-ttu-id="fc3dc-119">(Tenga en cuenta que algunas aplicaciones envían este mensaje con *lParam* establecido en **null**). En general, cuando reciba este mensaje, debe comprobar y volver a cargar cualquier configuración de parámetros del sistema utilizada por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fc3dc-119">(Note that some applications send this message with *lParam* set to **NULL**.) In general, when you receive this message, you should check and reload any system parameter settings that are used by your application.</span></span>

<span data-ttu-id="fc3dc-120">Esta cadena puede ser el nombre de una clave del registro o el nombre de una sección del archivo de Win.ini.</span><span class="sxs-lookup"><span data-stu-id="fc3dc-120">This string can be the name of a registry key or the name of a section in the Win.ini file.</span></span> <span data-ttu-id="fc3dc-121">Cuando la cadena es un nombre de registro, normalmente solo indica el nodo hoja del registro, no la ruta de acceso completa.</span><span class="sxs-lookup"><span data-stu-id="fc3dc-121">When the string is a registry name, it typically indicates only the leaf node in the registry, not the full path.</span></span>

<span data-ttu-id="fc3dc-122">Cuando el sistema envía este mensaje como resultado de un cambio en la configuración de la Directiva, este parámetro señala a la cadena "Policy".</span><span class="sxs-lookup"><span data-stu-id="fc3dc-122">When the system sends this message as a result of a change in policy settings, this parameter points to the string "Policy".</span></span>

<span data-ttu-id="fc3dc-123">Cuando el sistema envía este mensaje como resultado de un cambio en la configuración regional, este parámetro señala a la cadena "intl".</span><span class="sxs-lookup"><span data-stu-id="fc3dc-123">When the system sends this message as a result of a change in locale settings, this parameter points to the string "intl".</span></span>

<span data-ttu-id="fc3dc-124">Para aplicar un cambio en las variables de entorno del sistema o del usuario, difunda este mensaje con *lParam* establecido en la cadena "Environment".</span><span class="sxs-lookup"><span data-stu-id="fc3dc-124">To effect a change in the environment variables for the system or the user, broadcast this message with *lParam* set to the string "Environment".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc3dc-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fc3dc-125">Return value</span></span>

<span data-ttu-id="fc3dc-126">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="fc3dc-126">Type: **LRESULT**</span></span>

<span data-ttu-id="fc3dc-127">Si procesa este mensaje, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="fc3dc-127">If you process this message, return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc3dc-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fc3dc-128">Remarks</span></span>

<span data-ttu-id="fc3dc-129">El parámetro *lParam* indica qué métrica del sistema ha cambiado, por ejemplo, "ConvertibleSlateMode" si el indicador ConvertibleSlateMode se ha modificado o "SystemDockMode" si el indicador acoplado está activado.</span><span class="sxs-lookup"><span data-stu-id="fc3dc-129">The *lParam* parameter indicates which system metric has changed, for example, "ConvertibleSlateMode" if the CONVERTIBLESLATEMODE indicator was toggled or "SystemDockMode" if the DOCKED indicator was toggled.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc3dc-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc3dc-130">Requirements</span></span>



| <span data-ttu-id="fc3dc-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc3dc-131">Requirement</span></span> | <span data-ttu-id="fc3dc-132">Value</span><span class="sxs-lookup"><span data-stu-id="fc3dc-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc3dc-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc3dc-133">Minimum supported client</span></span><br/> | <span data-ttu-id="fc3dc-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fc3dc-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fc3dc-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc3dc-135">Minimum supported server</span></span><br/> | <span data-ttu-id="fc3dc-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fc3dc-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fc3dc-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fc3dc-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc3dc-138"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fc3dc-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc3dc-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc3dc-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc3dc-140">Eventos de Directiva</span><span class="sxs-lookup"><span data-stu-id="fc3dc-140">Policy Events</span></span>](/previous-versions/windows/desktop/Policy/policy-events)
</dt> <dt>

[<span data-ttu-id="fc3dc-141">**SendMessageTimeout**</span><span class="sxs-lookup"><span data-stu-id="fc3dc-141">**SendMessageTimeout**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta)
</dt> <dt>

[<span data-ttu-id="fc3dc-142">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="fc3dc-142">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 
