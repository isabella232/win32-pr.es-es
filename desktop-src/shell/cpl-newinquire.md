---
description: 'CPL_NEWINQUIRE mensaje: se envía a la función CPlApplet de una aplicación Panel de control para solicitar información sobre un cuadro de diálogo compatible con la aplicación.'
title: CPL_NEWINQUIRE mensaje (Cpl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: af52889c-7180-4690-8ed1-a0eb0a9dff35
api_name:
- CPL_NEWINQUIRE
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 90c5adf31c01fbab1b62aafd0714d165092f4e23
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104443"
---
# <a name="cpl_newinquire-message"></a><span data-ttu-id="92767-103">Mensaje \_ NEWINQUIRE de CPL</span><span class="sxs-lookup"><span data-stu-id="92767-103">CPL\_NEWINQUIRE message</span></span>

<span data-ttu-id="92767-104">Se envía a la [**función CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de una aplicación Panel de control para solicitar información sobre un cuadro de diálogo compatible con la aplicación.</span><span class="sxs-lookup"><span data-stu-id="92767-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to request information about a dialog box that the application supports.</span></span>

## <a name="parameters"></a><span data-ttu-id="92767-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92767-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92767-106">*uAppNum*</span><span class="sxs-lookup"><span data-stu-id="92767-106">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="92767-107">Número del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="92767-107">The dialog box number.</span></span> <span data-ttu-id="92767-108">Este número debe estar en el intervalo de cero a uno menos que el valor devuelto en respuesta al mensaje [**\_ GETCOUNT**](cpl-getcount.md) de CPL (CPL \_ GETCOUNT – 1).</span><span class="sxs-lookup"><span data-stu-id="92767-108">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="92767-109">*lpncpli*</span><span class="sxs-lookup"><span data-stu-id="92767-109">*lpncpli*</span></span> 
</dt> <dd>

<span data-ttu-id="92767-110">Dirección de una [**estructura NEWCPLINFO.**](/windows/win32/api/cpl/ns-cpl-newcplinfoa)</span><span class="sxs-lookup"><span data-stu-id="92767-110">The address of a [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) structure.</span></span> <span data-ttu-id="92767-111">La Panel de control debe rellenar esta estructura con información sobre el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="92767-111">The Control Panel application should fill this structure with information about the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92767-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92767-112">Return value</span></span>

<span data-ttu-id="92767-113">Si la [**función CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) procesa este mensaje correctamente, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="92767-113">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="92767-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="92767-114">Remarks</span></span>

<span data-ttu-id="92767-115">Para mejorar el rendimiento, la mayoría de las aplicaciones deben omitir **CPL \_ NEWINQUIRE y** procesar el [**mensaje CPL \_ INQUIRE en**](cpl-inquire.md) su lugar.</span><span class="sxs-lookup"><span data-stu-id="92767-115">For better performance, most applications should ignore **CPL\_NEWINQUIRE** and process the [**CPL\_INQUIRE**](cpl-inquire.md) message instead.</span></span>

<span data-ttu-id="92767-116">El Panel de control envía el **mensaje \_ NEWINQUIRE** de CPL una vez para cada cuadro de diálogo compatible con la aplicación.</span><span class="sxs-lookup"><span data-stu-id="92767-116">The Control Panel sends the **CPL\_NEWINQUIRE** message once for each dialog box supported by your application.</span></span> <span data-ttu-id="92767-117">El Panel de control también envía un [**mensaje CPL \_ INQUIRE**](cpl-inquire.md) para cada cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="92767-117">The Control Panel also sends a [**CPL\_INQUIRE**](cpl-inquire.md) message for each dialog box.</span></span> <span data-ttu-id="92767-118">Estos mensajes se envían inmediatamente después del [**mensaje \_ GETCOUNT de CPL.**](cpl-getcount.md)</span><span class="sxs-lookup"><span data-stu-id="92767-118">These messages are sent immediately after the [**CPL\_GETCOUNT**](cpl-getcount.md) message.</span></span> <span data-ttu-id="92767-119">Sin embargo, el sistema no garantiza el orden en el que se envían los mensajes **CPL \_ INQUIRE** y **CPL \_ NEWINQUIRE.**</span><span class="sxs-lookup"><span data-stu-id="92767-119">However, the system does not guarantee the order in which the **CPL\_INQUIRE** and **CPL\_NEWINQUIRE** messages are sent.</span></span>

<span data-ttu-id="92767-120">Puede realizar la inicialización del cuadro de diálogo cuando reciba [**CPL \_ INQUIRE**](cpl-inquire.md).</span><span class="sxs-lookup"><span data-stu-id="92767-120">You can perform initialization for the dialog box when you receive [**CPL\_INQUIRE**](cpl-inquire.md).</span></span> <span data-ttu-id="92767-121">Si debe asignar memoria, debe hacerlo en respuesta al [**mensaje \_ INIT de CPL.**](cpl-init.md)</span><span class="sxs-lookup"><span data-stu-id="92767-121">If you must allocate memory, do so in response to the [**CPL\_INIT**](cpl-init.md) message.</span></span>

<span data-ttu-id="92767-122">[**CPL \_ INQUIRE**](cpl-inquire.md) es el mensaje preferido.</span><span class="sxs-lookup"><span data-stu-id="92767-122">[**CPL\_INQUIRE**](cpl-inquire.md) is the preferred message.</span></span> <span data-ttu-id="92767-123">Esto se debe a **que CPL \_ NEWINQUIRE** devuelve información de forma que el sistema no puede almacenar en caché.</span><span class="sxs-lookup"><span data-stu-id="92767-123">This is because **CPL\_NEWINQUIRE** returns information in a form that the system cannot cache.</span></span> <span data-ttu-id="92767-124">Por lo tanto, las aplicaciones que procesan **CPL \_ NEWINQUIRE** deben cargarse cada vez que el Panel de control necesita la información, lo que da lugar a una reducción significativa del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="92767-124">Consequently, applications that process **CPL\_NEWINQUIRE** must be loaded each time the Control Panel needs the information, resulting in a significant reduction in performance.</span></span>

<span data-ttu-id="92767-125">Las únicas aplicaciones que deben **usar CPL \_ NEWINQUIRE** son aquellas que necesitan cambiar su icono o mostrar cadenas en función del estado del equipo.</span><span class="sxs-lookup"><span data-stu-id="92767-125">The only applications that should use **CPL\_NEWINQUIRE** are those that need to change their icon or display strings based on the state of the computer.</span></span> <span data-ttu-id="92767-126">En este caso, el controlador [**CPL \_ INQUIRE**](cpl-inquire.md) debe especificar el valor de CPL DYNAMIC RES para los miembros idIcon , idName o idInfo de la estructura \_ \_ [**CPLINFO,**](/windows/win32/api/cpl/ns-cpl-cplinfo)    en lugar de especificar un identificador de recurso válido.</span><span class="sxs-lookup"><span data-stu-id="92767-126">In this case, your [**CPL\_INQUIRE**](cpl-inquire.md) handler should specify the CPL\_DYNAMIC\_RES value for the **idIcon**, **idName**, or **idInfo** members of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) structure, rather than specifying a valid resource identifier.</span></span> <span data-ttu-id="92767-127">Esto hace que el Panel de control envíe el mensaje **\_ NEWINQUIRE** de CPL cada vez que necesite el icono y las cadenas de presentación, lo que le permite especificar información basada en el estado actual del equipo.</span><span class="sxs-lookup"><span data-stu-id="92767-127">This causes the Control Panel to send the **CPL\_NEWINQUIRE** message each time it needs the icon and display strings, allowing you to specify information based on the current state of the computer.</span></span> <span data-ttu-id="92767-128">Por supuesto, esto es significativamente más lento que usar la información almacenada en caché.</span><span class="sxs-lookup"><span data-stu-id="92767-128">Of course, this is significantly slower than using cached information.</span></span>

## <a name="requirements"></a><span data-ttu-id="92767-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92767-129">Requirements</span></span>



| <span data-ttu-id="92767-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="92767-130">Requirement</span></span> | <span data-ttu-id="92767-131">Valor</span><span class="sxs-lookup"><span data-stu-id="92767-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="92767-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92767-132">Minimum supported client</span></span><br/> | <span data-ttu-id="92767-133">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="92767-133">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="92767-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92767-134">Minimum supported server</span></span><br/> | <span data-ttu-id="92767-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="92767-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="92767-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92767-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="92767-137"><dt>Cpl.h</dt></span><span class="sxs-lookup"><span data-stu-id="92767-137"><dt>Cpl.h</dt></span></span> </dl> |



 

 
