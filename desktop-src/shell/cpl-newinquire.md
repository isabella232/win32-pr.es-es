---
description: Se envía a la función CPlApplet de una aplicación del panel de control para solicitar información sobre un cuadro de diálogo que la aplicación admite.
title: Mensaje de CPL_NEWINQUIRE (CPL. h)
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
ms.openlocfilehash: 72992d4ea867bc091c29feaa99cc1a22c2a02b2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984334"
---
# <a name="cpl_newinquire-message"></a><span data-ttu-id="97ab6-103">CPL \_ NEWINQUIRE Message</span><span class="sxs-lookup"><span data-stu-id="97ab6-103">CPL\_NEWINQUIRE message</span></span>

<span data-ttu-id="97ab6-104">Se envía a la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de una aplicación del panel de control para solicitar información sobre un cuadro de diálogo que la aplicación admite.</span><span class="sxs-lookup"><span data-stu-id="97ab6-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to request information about a dialog box that the application supports.</span></span>

## <a name="parameters"></a><span data-ttu-id="97ab6-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="97ab6-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97ab6-106">*uAppNum*</span><span class="sxs-lookup"><span data-stu-id="97ab6-106">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="97ab6-107">Número del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="97ab6-107">The dialog box number.</span></span> <span data-ttu-id="97ab6-108">Este número debe estar en el intervalo comprendido entre cero y uno menos que el valor devuelto en respuesta al mensaje [**CPL \_ GETCOUNT**](cpl-getcount.md) (CPL \_ getCount – 1).</span><span class="sxs-lookup"><span data-stu-id="97ab6-108">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="97ab6-109">*lpncpli*</span><span class="sxs-lookup"><span data-stu-id="97ab6-109">*lpncpli*</span></span> 
</dt> <dd>

<span data-ttu-id="97ab6-110">Dirección de una estructura [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) .</span><span class="sxs-lookup"><span data-stu-id="97ab6-110">The address of a [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) structure.</span></span> <span data-ttu-id="97ab6-111">La aplicación del panel de control debe llenar esta estructura con información sobre el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="97ab6-111">The Control Panel application should fill this structure with information about the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97ab6-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="97ab6-112">Return value</span></span>

<span data-ttu-id="97ab6-113">Si la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) procesa este mensaje correctamente, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="97ab6-113">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="97ab6-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="97ab6-114">Remarks</span></span>

<span data-ttu-id="97ab6-115">Para mejorar el rendimiento, la mayoría de las aplicaciones deben omitir **CPL \_ NEWINQUIRE** y procesar el mensaje CPL de la [**\_ consulta**](cpl-inquire.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="97ab6-115">For better performance, most applications should ignore **CPL\_NEWINQUIRE** and process the [**CPL\_INQUIRE**](cpl-inquire.md) message instead.</span></span>

<span data-ttu-id="97ab6-116">El panel de control envía el mensaje **CPL \_ NEWINQUIRE** una vez para cada cuadro de diálogo admitido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="97ab6-116">The Control Panel sends the **CPL\_NEWINQUIRE** message once for each dialog box supported by your application.</span></span> <span data-ttu-id="97ab6-117">El panel de control también envía un mensaje de [**CPL \_ consulta**](cpl-inquire.md) para cada cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="97ab6-117">The Control Panel also sends a [**CPL\_INQUIRE**](cpl-inquire.md) message for each dialog box.</span></span> <span data-ttu-id="97ab6-118">Estos mensajes se envían inmediatamente después del mensaje [**CPL \_ GETCOUNT**](cpl-getcount.md) .</span><span class="sxs-lookup"><span data-stu-id="97ab6-118">These messages are sent immediately after the [**CPL\_GETCOUNT**](cpl-getcount.md) message.</span></span> <span data-ttu-id="97ab6-119">Sin embargo, el sistema no garantiza el orden en el que se envían los mensajes **CPL \_ inquire** y **CPL \_ NEWINQUIRE** .</span><span class="sxs-lookup"><span data-stu-id="97ab6-119">However, the system does not guarantee the order in which the **CPL\_INQUIRE** and **CPL\_NEWINQUIRE** messages are sent.</span></span>

<span data-ttu-id="97ab6-120">Puede realizar la inicialización del cuadro de diálogo cuando reciba [**CPL \_ consulta**](cpl-inquire.md).</span><span class="sxs-lookup"><span data-stu-id="97ab6-120">You can perform initialization for the dialog box when you receive [**CPL\_INQUIRE**](cpl-inquire.md).</span></span> <span data-ttu-id="97ab6-121">Si tiene que asignar memoria, hágalo en respuesta al mensaje [**CPL \_ init**](cpl-init.md) .</span><span class="sxs-lookup"><span data-stu-id="97ab6-121">If you must allocate memory, do so in response to the [**CPL\_INIT**](cpl-init.md) message.</span></span>

<span data-ttu-id="97ab6-122">[**CPL \_ La consulta**](cpl-inquire.md) es el mensaje preferido.</span><span class="sxs-lookup"><span data-stu-id="97ab6-122">[**CPL\_INQUIRE**](cpl-inquire.md) is the preferred message.</span></span> <span data-ttu-id="97ab6-123">Esto se debe a que **CPL \_ NEWINQUIRE** devuelve información en un formato que el sistema no puede almacenar en caché.</span><span class="sxs-lookup"><span data-stu-id="97ab6-123">This is because **CPL\_NEWINQUIRE** returns information in a form that the system cannot cache.</span></span> <span data-ttu-id="97ab6-124">Por lo tanto, las aplicaciones que procesan **CPL \_ NEWINQUIRE** se deben cargar cada vez que el panel de control necesite la información, lo que produce una reducción significativa del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="97ab6-124">Consequently, applications that process **CPL\_NEWINQUIRE** must be loaded each time the Control Panel needs the information, resulting in a significant reduction in performance.</span></span>

<span data-ttu-id="97ab6-125">Las únicas aplicaciones que deben usar **CPL \_ NEWINQUIRE** son aquellas que necesitan cambiar su icono o mostrar cadenas en función del estado del equipo.</span><span class="sxs-lookup"><span data-stu-id="97ab6-125">The only applications that should use **CPL\_NEWINQUIRE** are those that need to change their icon or display strings based on the state of the computer.</span></span> <span data-ttu-id="97ab6-126">En este caso, el controlador de CPL de la [**\_ consulta**](cpl-inquire.md) debe especificar el valor de CPL \_ Dynamic \_ res para los miembros **idIcon**, **idName** o **idInfo** de la estructura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) , en lugar de especificar un identificador de recursos válido.</span><span class="sxs-lookup"><span data-stu-id="97ab6-126">In this case, your [**CPL\_INQUIRE**](cpl-inquire.md) handler should specify the CPL\_DYNAMIC\_RES value for the **idIcon**, **idName**, or **idInfo** members of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) structure, rather than specifying a valid resource identifier.</span></span> <span data-ttu-id="97ab6-127">Esto hace que el panel de control envíe el mensaje **CPL \_ NEWINQUIRE** cada vez que necesite el icono y las cadenas de presentación, lo que le permite especificar información según el estado actual del equipo.</span><span class="sxs-lookup"><span data-stu-id="97ab6-127">This causes the Control Panel to send the **CPL\_NEWINQUIRE** message each time it needs the icon and display strings, allowing you to specify information based on the current state of the computer.</span></span> <span data-ttu-id="97ab6-128">Por supuesto, esto es significativamente más lento que el uso de la información almacenada en caché.</span><span class="sxs-lookup"><span data-stu-id="97ab6-128">Of course, this is significantly slower than using cached information.</span></span>

## <a name="requirements"></a><span data-ttu-id="97ab6-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97ab6-129">Requirements</span></span>



| <span data-ttu-id="97ab6-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="97ab6-130">Requirement</span></span> | <span data-ttu-id="97ab6-131">Value</span><span class="sxs-lookup"><span data-stu-id="97ab6-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="97ab6-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97ab6-132">Minimum supported client</span></span><br/> | <span data-ttu-id="97ab6-133">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="97ab6-133">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="97ab6-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97ab6-134">Minimum supported server</span></span><br/> | <span data-ttu-id="97ab6-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="97ab6-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="97ab6-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="97ab6-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="97ab6-137"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="97ab6-137"><dt>Cpl.h</dt></span></span> </dl> |



 

 
