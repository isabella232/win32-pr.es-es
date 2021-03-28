---
description: Establece el tamaño y la posición de la pantalla de un control Appbar.
ms.assetid: b3c56278-b9a2-4e08-bf98-7b3e4c8bd082
title: Mensaje de ABM_SETPOS (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6886249f42638745ca038aa1f216ddc995f0e7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540595"
---
# <a name="abm_setpos-message"></a><span data-ttu-id="fa296-103">ABN \_ SETPOS</span><span class="sxs-lookup"><span data-stu-id="fa296-103">ABM\_SETPOS message</span></span>

<span data-ttu-id="fa296-104">Establece el tamaño y la posición de la pantalla de un control Appbar.</span><span class="sxs-lookup"><span data-stu-id="fa296-104">Sets the size and screen position of an appbar.</span></span> <span data-ttu-id="fa296-105">El mensaje especifica un borde de pantalla y el rectángulo delimitador del Appbar.</span><span class="sxs-lookup"><span data-stu-id="fa296-105">The message specifies a screen edge and the bounding rectangle for the appbar.</span></span> <span data-ttu-id="fa296-106">El sistema puede ajustar el rectángulo delimitador para que el Appbar no interfiera con la barra de tareas de Windows ni con ningún otro appbars.</span><span class="sxs-lookup"><span data-stu-id="fa296-106">The system may adjust the bounding rectangle so that the appbar does not interfere with the Windows taskbar or any other appbars.</span></span>


```C++
SHAppBarMessage(ABM_SETPOS, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="fa296-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fa296-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa296-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="fa296-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="fa296-109">Puntero a una estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="fa296-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="fa296-110">El miembro **uEdge** especifica un borde de pantalla y el miembro **RC** contiene el rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="fa296-110">The **uEdge** member specifies a screen edge, and the **rc** member contains the bounding rectangle.</span></span> <span data-ttu-id="fa296-111">Cuando la función [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) devuelve, **RC** contiene el rectángulo delimitador aprobado.</span><span class="sxs-lookup"><span data-stu-id="fa296-111">When the [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) function returns, **rc** contains the approved bounding rectangle.</span></span> <span data-ttu-id="fa296-112">Debe especificar los miembros **cbSize**, **hWnd**, **uEdge** y **RC** al enviar este mensaje. se omiten todos los demás miembros.</span><span class="sxs-lookup"><span data-stu-id="fa296-112">You must specify the **cbSize**, **hWnd**, **uEdge**, and **rc** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa296-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fa296-113">Return value</span></span>

<span data-ttu-id="fa296-114">Siempre devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="fa296-114">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa296-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fa296-115">Remarks</span></span>

<span data-ttu-id="fa296-116">Este mensaje hace que el sistema envíe el mensaje de notificación [**ABN \_ POSCHANGED**](abn-poschanged.md) a todos los appbars.</span><span class="sxs-lookup"><span data-stu-id="fa296-116">This message causes the system to send the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message to all appbars.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa296-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa296-117">Requirements</span></span>



| <span data-ttu-id="fa296-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa296-118">Requirement</span></span> | <span data-ttu-id="fa296-119">Value</span><span class="sxs-lookup"><span data-stu-id="fa296-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fa296-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa296-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fa296-121">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="fa296-121">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fa296-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa296-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fa296-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fa296-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fa296-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fa296-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa296-125"><dt>ShellAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa296-125"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




