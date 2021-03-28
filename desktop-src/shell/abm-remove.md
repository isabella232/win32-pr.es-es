---
description: Anula el registro de una Appbar quitando la lista interna del sistema. El sistema ya no envía mensajes de notificación al Appbar o impide que otras aplicaciones utilicen el área de pantalla utilizada por el Appbar.
title: Mensaje de ABM_REMOVE (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3da73a52-3dbb-4133-a9bd-86540e1c4154
api_name:
- ABM_REMOVE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7f4530869b9f68772c28fefd6130ff8e4b6ffbec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907735"
---
# <a name="abm_remove-message"></a><span data-ttu-id="6e093-104">ABN \_ quitar mensaje</span><span class="sxs-lookup"><span data-stu-id="6e093-104">ABM\_REMOVE message</span></span>

<span data-ttu-id="6e093-105">Anula el registro de una Appbar quitando la lista interna del sistema.</span><span class="sxs-lookup"><span data-stu-id="6e093-105">Unregisters an appbar by removing it from the system's internal list.</span></span> <span data-ttu-id="6e093-106">El sistema ya no envía mensajes de notificación al Appbar o impide que otras aplicaciones utilicen el área de pantalla utilizada por el Appbar.</span><span class="sxs-lookup"><span data-stu-id="6e093-106">The system no longer sends notification messages to the appbar or prevents other applications from using the screen area used by the appbar.</span></span>


```C++
                SHAppBarMessage(ABM_REMOVE, pabd); 
            
```



## <a name="parameters"></a><span data-ttu-id="6e093-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e093-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e093-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="6e093-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="6e093-109">Puntero a una estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que contiene el identificador de la Appbar cuyo registro se va a anular.</span><span class="sxs-lookup"><span data-stu-id="6e093-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that contains the handle to the appbar to unregister.</span></span> <span data-ttu-id="6e093-110">Debe especificar los miembros **cbSize** y **hWnd** al enviar este mensaje; se omiten todos los demás miembros.</span><span class="sxs-lookup"><span data-stu-id="6e093-110">You must specify the **cbSize** and **hWnd** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e093-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e093-111">Return value</span></span>

<span data-ttu-id="6e093-112">Siempre devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="6e093-112">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e093-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6e093-113">Remarks</span></span>

<span data-ttu-id="6e093-114">Este mensaje hace que el sistema envíe el mensaje de notificación [**ABN \_ POSCHANGED**](abn-poschanged.md) a todos los appbars.</span><span class="sxs-lookup"><span data-stu-id="6e093-114">This message causes the system to send the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message to all appbars.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e093-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e093-115">Requirements</span></span>



| <span data-ttu-id="6e093-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e093-116">Requirement</span></span> | <span data-ttu-id="6e093-117">Value</span><span class="sxs-lookup"><span data-stu-id="6e093-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6e093-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e093-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6e093-119">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="6e093-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6e093-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e093-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6e093-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6e093-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6e093-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e093-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e093-123"><dt>ShellAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e093-123"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




