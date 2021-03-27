---
description: Notifica al sistema cuando ha cambiado la posición de una Appbar. Un Appbar debe llamar a este mensaje en respuesta al mensaje de WINDOWPOSCHANGED de WM \_ .
ms.assetid: 8ca51f5f-b6cf-4f2c-98f4-69c992679320
title: Mensaje de ABM_WINDOWPOSCHANGED (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29c8ea6fab6960678ad030a0c1817ad5f8aaae29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497050"
---
# <a name="abm_windowposchanged-message"></a><span data-ttu-id="076f3-104">ABN \_ WINDOWPOSCHANGED</span><span class="sxs-lookup"><span data-stu-id="076f3-104">ABM\_WINDOWPOSCHANGED message</span></span>

<span data-ttu-id="076f3-105">Notifica al sistema cuando ha cambiado la posición de una Appbar.</span><span class="sxs-lookup"><span data-stu-id="076f3-105">Notifies the system when an appbar's position has changed.</span></span> <span data-ttu-id="076f3-106">Un Appbar debe llamar a este mensaje en respuesta al mensaje de [**\_ WINDOWPOSCHANGED de WM**](/windows/desktop/winmsg/wm-windowposchanged) .</span><span class="sxs-lookup"><span data-stu-id="076f3-106">An appbar should call this message in response to the [**WM\_WINDOWPOSCHANGED**](/windows/desktop/winmsg/wm-windowposchanged) message.</span></span>


```C++
SHAppBarMessage(ABM_WINDOWPOSCHANGED, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="076f3-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="076f3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="076f3-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="076f3-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="076f3-109">Puntero a una estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que identifica el Appbar que se va a activar.</span><span class="sxs-lookup"><span data-stu-id="076f3-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that identifies the appbar to activate.</span></span> <span data-ttu-id="076f3-110">Debe especificar los miembros **cbSize** y **hWnd** al enviar este mensaje; se omiten todos los demás miembros.</span><span class="sxs-lookup"><span data-stu-id="076f3-110">You must specify the **cbSize** and **hWnd** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="076f3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="076f3-111">Return value</span></span>

<span data-ttu-id="076f3-112">Siempre devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="076f3-112">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="076f3-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="076f3-113">Remarks</span></span>

<span data-ttu-id="076f3-114">Este mensaje se omite si el miembro **hWnd** de la estructura a la que apunta *pabd* identifica un Appbar de ocultación automáticamente.</span><span class="sxs-lookup"><span data-stu-id="076f3-114">This message is ignored if the **hWnd** member of the structure pointed to by *pabd* identifies an autohide appbar.</span></span>

## <a name="requirements"></a><span data-ttu-id="076f3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="076f3-115">Requirements</span></span>



| <span data-ttu-id="076f3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="076f3-116">Requirement</span></span> | <span data-ttu-id="076f3-117">Value</span><span class="sxs-lookup"><span data-stu-id="076f3-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="076f3-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="076f3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="076f3-119">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="076f3-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="076f3-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="076f3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="076f3-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="076f3-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="076f3-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="076f3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="076f3-123"><dt>ShellAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="076f3-123"><dt>Shellapi.h</dt></span></span> </dl> |



 

