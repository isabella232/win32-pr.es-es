---
description: Registra un nuevo Appbar y especifica el identificador de mensaje que el sistema debe usar para enviar mensajes de notificación. Un Appbar debe enviar este mensaje antes de enviar cualquier otro mensaje de Appbar.
ms.assetid: 1da9db13-6fdc-44b3-9985-de32d572675a
title: Mensaje de ABM_NEW (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fad11e6712d0afd0c1a5e9de07fd3d690800db13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808882"
---
# <a name="abm_new-message"></a><span data-ttu-id="0afa9-104">ABN \_ nuevo mensaje</span><span class="sxs-lookup"><span data-stu-id="0afa9-104">ABM\_NEW message</span></span>

<span data-ttu-id="0afa9-105">Registra un nuevo Appbar y especifica el identificador de mensaje que el sistema debe usar para enviar mensajes de notificación.</span><span class="sxs-lookup"><span data-stu-id="0afa9-105">Registers a new appbar and specifies the message identifier that the system should use to send it notification messages.</span></span> <span data-ttu-id="0afa9-106">Un Appbar debe enviar este mensaje antes de enviar cualquier otro mensaje de Appbar.</span><span class="sxs-lookup"><span data-stu-id="0afa9-106">An appbar should send this message before sending any other appbar messages.</span></span>


```C++
fRegistered = (BOOL) SHAppBarMessage(ABM_NEW, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="0afa9-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0afa9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0afa9-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="0afa9-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="0afa9-109">Puntero a una estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que contiene el identificador de la ventana de la nueva Appbar y el identificador de mensaje.</span><span class="sxs-lookup"><span data-stu-id="0afa9-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that contains the new appbar's window handle and message identifier.</span></span> <span data-ttu-id="0afa9-110">Debe especificar los miembros **cbSize**, **hWnd** y **uCallbackMessage** al enviar este mensaje; se omiten todos los demás miembros.</span><span class="sxs-lookup"><span data-stu-id="0afa9-110">You must specify the **cbSize**, **hWnd**, and **uCallbackMessage** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0afa9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0afa9-111">Return value</span></span>

<span data-ttu-id="0afa9-112">Devuelve **true** si es correcto, o **false** si se produce un error o si el Appbar ya está registrado.</span><span class="sxs-lookup"><span data-stu-id="0afa9-112">Returns **TRUE** if successful, or **FALSE** if an error occurs or if the appbar is already registered.</span></span>

## <a name="requirements"></a><span data-ttu-id="0afa9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0afa9-113">Requirements</span></span>



| <span data-ttu-id="0afa9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0afa9-114">Requirement</span></span> | <span data-ttu-id="0afa9-115">Value</span><span class="sxs-lookup"><span data-stu-id="0afa9-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0afa9-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0afa9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0afa9-117">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="0afa9-117">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0afa9-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0afa9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0afa9-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0afa9-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0afa9-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0afa9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0afa9-121"><dt>ShellAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="0afa9-121"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




