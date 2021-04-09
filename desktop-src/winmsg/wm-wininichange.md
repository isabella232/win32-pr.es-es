---
description: Una aplicación envía el mensaje de WININICHANGE de WM \_ a todas las ventanas de nivel superior después de hacer un cambio en el archivo de WIN.INI. La función SystemParametersInfo envía este mensaje después de que una aplicación utilice la función para cambiar una configuración en WIN.INI.
ms.assetid: 402f8d71-ad52-486d-be26-8b41a3f22045
title: Mensaje de WM_WININICHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b8db6c4794a8c1a572f61028d32eaeaf578d0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001107"
---
# <a name="wm_wininichange-message"></a><span data-ttu-id="37b3b-104">Mensaje de WININICHANGE de WM \_</span><span class="sxs-lookup"><span data-stu-id="37b3b-104">WM\_WININICHANGE message</span></span>

<span data-ttu-id="37b3b-105">Una aplicación envía el mensaje de **\_ WININICHANGE de WM** a todas las ventanas de nivel superior después de hacer un cambio en el archivo de WIN.INI.</span><span class="sxs-lookup"><span data-stu-id="37b3b-105">An application sends the **WM\_WININICHANGE** message to all top-level windows after making a change to the WIN.INI file.</span></span> <span data-ttu-id="37b3b-106">La función [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) envía este mensaje después de que una aplicación utilice la función para cambiar una configuración en WIN.INI.</span><span class="sxs-lookup"><span data-stu-id="37b3b-106">The [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function sends this message after an application uses the function to change a setting in WIN.INI.</span></span>

> [!Note]  
> <span data-ttu-id="37b3b-107">El mensaje de **\_ WININICHANGE de WM** solo se proporciona para ofrecer compatibilidad con versiones anteriores del sistema.</span><span class="sxs-lookup"><span data-stu-id="37b3b-107">The **WM\_WININICHANGE** message is provided only for compatibility with earlier versions of the system.</span></span> <span data-ttu-id="37b3b-108">Las aplicaciones deben usar el mensaje de [**\_ SETTINGCHANGE de WM**](wm-settingchange.md) .</span><span class="sxs-lookup"><span data-stu-id="37b3b-108">Applications should use the [**WM\_SETTINGCHANGE**](wm-settingchange.md) message.</span></span>

 

<span data-ttu-id="37b3b-109">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="37b3b-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_WININICHANGE                 0x001A
```



## <a name="parameters"></a><span data-ttu-id="37b3b-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37b3b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37b3b-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="37b3b-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37b3b-112">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="37b3b-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="37b3b-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="37b3b-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37b3b-114">Un puntero a una cadena que contiene el nombre del parámetro del sistema que se cambió.</span><span class="sxs-lookup"><span data-stu-id="37b3b-114">A pointer to a string containing the name of the system parameter that was changed.</span></span> <span data-ttu-id="37b3b-115">Por ejemplo, esta cadena puede ser el nombre de una clave del registro o el nombre de una sección del archivo de Win.ini.</span><span class="sxs-lookup"><span data-stu-id="37b3b-115">For example, this string can be the name of a registry key or the name of a section in the Win.ini file.</span></span> <span data-ttu-id="37b3b-116">Este parámetro no es especialmente útil para determinar qué parámetro del sistema ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="37b3b-116">This parameter is not particularly useful in determining which system parameter changed.</span></span> <span data-ttu-id="37b3b-117">Por ejemplo, cuando la cadena es un nombre de registro, normalmente solo indica el nodo hoja del registro, no la ruta de acceso completa.</span><span class="sxs-lookup"><span data-stu-id="37b3b-117">For example, when the string is a registry name, it typically indicates only the leaf node in the registry, not the whole path.</span></span> <span data-ttu-id="37b3b-118">Además, algunas aplicaciones envían este mensaje con *lParam* establecido en **null**.</span><span class="sxs-lookup"><span data-stu-id="37b3b-118">In addition, some applications send this message with *lParam* set to **NULL**.</span></span> <span data-ttu-id="37b3b-119">En general, cuando reciba este mensaje, debe comprobar y volver a cargar cualquier configuración de parámetros del sistema utilizada por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="37b3b-119">In general, when you receive this message, you should check and reload any system parameter settings that are used by your application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37b3b-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37b3b-120">Return value</span></span>

<span data-ttu-id="37b3b-121">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="37b3b-121">Type: **LRESULT**</span></span>

<span data-ttu-id="37b3b-122">Si procesa este mensaje, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="37b3b-122">If you process this message, return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="37b3b-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="37b3b-123">Remarks</span></span>

<span data-ttu-id="37b3b-124">Para enviar el mensaje de **\_ WININICHANGE de WM** a todas las ventanas de nivel superior, use la función [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) con el parámetro *hWnd* establecido en la **\_ difusión HWND**.</span><span class="sxs-lookup"><span data-stu-id="37b3b-124">To send the **WM\_WININICHANGE** message to all top-level windows, use the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the *hWnd* parameter set to **HWND\_BROADCAST**.</span></span>

<span data-ttu-id="37b3b-125">En su lugar, las llamadas a funciones que cambian WIN.INI pueden estar asignadas al registro.</span><span class="sxs-lookup"><span data-stu-id="37b3b-125">Calls to functions that change WIN.INI may be mapped to the registry instead.</span></span> <span data-ttu-id="37b3b-126">Esta asignación se produce cuando WIN.INI y la sección que se va a cambiar se especifican en el registro con la siguiente clave:</span><span class="sxs-lookup"><span data-stu-id="37b3b-126">This mapping occurs when WIN.INI and the section being changed are specified in the registry under the following key:</span></span>

<span data-ttu-id="37b3b-127">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ IniFileMapping**</span><span class="sxs-lookup"><span data-stu-id="37b3b-127">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\IniFileMapping**</span></span>

<span data-ttu-id="37b3b-128">El cambio en la ubicación de almacenamiento no tiene ningún efecto en el comportamiento de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="37b3b-128">The change in the storage location has no effect on the behavior of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="37b3b-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37b3b-129">Requirements</span></span>



| <span data-ttu-id="37b3b-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="37b3b-130">Requirement</span></span> | <span data-ttu-id="37b3b-131">Value</span><span class="sxs-lookup"><span data-stu-id="37b3b-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37b3b-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37b3b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="37b3b-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="37b3b-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="37b3b-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37b3b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="37b3b-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="37b3b-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="37b3b-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37b3b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="37b3b-137"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="37b3b-137"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37b3b-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="37b3b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37b3b-139">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="37b3b-139">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 
