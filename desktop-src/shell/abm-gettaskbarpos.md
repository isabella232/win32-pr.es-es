---
description: Recupera el rectángulo delimitador de la barra de tareas de Windows.
ms.assetid: 8072bb2d-05e6-4baa-a7f4-1377b94fdd45
title: Mensaje de ABM_GETTASKBARPOS (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb678b6e7ade1f148d2deb4b0de6c8953f019d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540598"
---
# <a name="abm_gettaskbarpos-message"></a><span data-ttu-id="71d5d-103">ABN \_ GETTASKBARPOS</span><span class="sxs-lookup"><span data-stu-id="71d5d-103">ABM\_GETTASKBARPOS message</span></span>

<span data-ttu-id="71d5d-104">Recupera el rectángulo delimitador de la barra de tareas de Windows.</span><span class="sxs-lookup"><span data-stu-id="71d5d-104">Retrieves the bounding rectangle of the Windows taskbar.</span></span>


```C++
fResult = (BOOL) SHAppBarMessage(ABM_GETTASKBARPOS, pabd);
```



## <a name="parameters"></a><span data-ttu-id="71d5d-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71d5d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71d5d-106">*pabd*</span><span class="sxs-lookup"><span data-stu-id="71d5d-106">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="71d5d-107">Puntero a una estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) cuyo miembro **RC** recibe el rectángulo delimitador, en coordenadas de pantalla, de la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="71d5d-107">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure whose **rc** member receives the bounding rectangle, in screen coordinates, of the taskbar.</span></span> <span data-ttu-id="71d5d-108">Debe especificar el **cbSize** al enviar este mensaje; se omiten todos los demás miembros.</span><span class="sxs-lookup"><span data-stu-id="71d5d-108">You must specify the **cbSize** when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71d5d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71d5d-109">Return value</span></span>

<span data-ttu-id="71d5d-110">Devuelve **true si es** correcto; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="71d5d-110">Returns **TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="71d5d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71d5d-111">Remarks</span></span>

<span data-ttu-id="71d5d-112">Tenga en cuenta que esto solo se aplica a la barra de tareas del sistema.</span><span class="sxs-lookup"><span data-stu-id="71d5d-112">Note that this applies only to the system taskbar.</span></span> <span data-ttu-id="71d5d-113">También pueden estar presentes otros objetos, especialmente las barras de herramientas que se proporcionan con software de terceros.</span><span class="sxs-lookup"><span data-stu-id="71d5d-113">Other objects, particularly toolbars supplied with third-party software, also can be present.</span></span> <span data-ttu-id="71d5d-114">Como resultado, es posible que parte del área de pantalla no incluida en la barra de tareas de Windows no esté visible para el usuario.</span><span class="sxs-lookup"><span data-stu-id="71d5d-114">As a result, some of the screen area not covered by the Windows taskbar might not be visible to the user.</span></span> <span data-ttu-id="71d5d-115">Para recuperar el área de la pantalla que no está incluida en la barra de tareas y en otras barras de la aplicación, use la función [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="71d5d-115">To retrieve the area of the screen not covered by both the taskbar and other app bars the working area available to your application , use the [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="71d5d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71d5d-116">Requirements</span></span>



| <span data-ttu-id="71d5d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="71d5d-117">Requirement</span></span> | <span data-ttu-id="71d5d-118">Value</span><span class="sxs-lookup"><span data-stu-id="71d5d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="71d5d-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71d5d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="71d5d-120">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="71d5d-120">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="71d5d-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71d5d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="71d5d-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="71d5d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="71d5d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71d5d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="71d5d-124"><dt>ShellAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="71d5d-124"><dt>Shellapi.h</dt></span></span> </dl> |



 

