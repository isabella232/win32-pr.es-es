---
description: Notifica al sistema que se ha activado un Appbar. Un Appbar debe llamar a este mensaje en respuesta al mensaje de activación de WM \_ .
ms.assetid: 16011302-7c2d-4c34-9953-51cceb96e4b3
title: Mensaje de ABM_ACTIVATE (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94a44bcc33efcd3d1a9af5e7e2abca33893e9fe9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153928"
---
# <a name="abm_activate-message"></a><span data-ttu-id="f2325-104">ABN \_ Activar mensaje</span><span class="sxs-lookup"><span data-stu-id="f2325-104">ABM\_ACTIVATE message</span></span>

<span data-ttu-id="f2325-105">Notifica al sistema que se ha activado un Appbar.</span><span class="sxs-lookup"><span data-stu-id="f2325-105">Notifies the system that an appbar has been activated.</span></span> <span data-ttu-id="f2325-106">Un Appbar debe llamar a este mensaje en respuesta al mensaje de [**\_ activación de WM**](/windows/desktop/inputdev/wm-activate) .</span><span class="sxs-lookup"><span data-stu-id="f2325-106">An appbar should call this message in response to the [**WM\_ACTIVATE**](/windows/desktop/inputdev/wm-activate) message.</span></span>


```C++

SHAppBarMessage(ABM_ACTIVATE, pabd); 

            
```



## <a name="parameters"></a><span data-ttu-id="f2325-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2325-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2325-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="f2325-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="f2325-109">Puntero a una estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que identifica el Appbar que se va a activar.</span><span class="sxs-lookup"><span data-stu-id="f2325-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that identifies the appbar to activate.</span></span> <span data-ttu-id="f2325-110">Debe especificar los miembros **cbSize** y **hWnd** al enviar este mensaje; se omiten todos los demás miembros.</span><span class="sxs-lookup"><span data-stu-id="f2325-110">You must specify the **cbSize** and **hWnd** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2325-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2325-111">Return value</span></span>

<span data-ttu-id="f2325-112">Siempre devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="f2325-112">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2325-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2325-113">Remarks</span></span>

<span data-ttu-id="f2325-114">Este mensaje se omite si el miembro **hWnd** de la estructura a la que apunta *pabd* identifica un Appbar de ocultación automáticamente.</span><span class="sxs-lookup"><span data-stu-id="f2325-114">This message is ignored if the **hWnd** member of the structure pointed to by *pabd* identifies an autohide appbar.</span></span> <span data-ttu-id="f2325-115">El sistema establece automáticamente el orden z para la ocultación automática de appbars.</span><span class="sxs-lookup"><span data-stu-id="f2325-115">The system automatically sets the z-order for autohide appbars.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2325-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2325-116">Requirements</span></span>



| <span data-ttu-id="f2325-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2325-117">Requirement</span></span> | <span data-ttu-id="f2325-118">Value</span><span class="sxs-lookup"><span data-stu-id="f2325-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2325-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2325-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f2325-120">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f2325-120">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f2325-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2325-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f2325-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f2325-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f2325-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2325-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2325-124"><dt>ShellAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2325-124"><dt>Shellapi.h</dt></span></span> </dl> |



 

