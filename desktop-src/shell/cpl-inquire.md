---
description: Se envía a la función CPlApplet de una aplicación del panel de control para solicitar información sobre un cuadro de diálogo que la aplicación admite.
title: Mensaje de CPL_INQUIRE (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: daca87b7-f1ee-40f4-95d2-3150b595151e
api_name:
- CPL_INQUIRE
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8f4c75a2610dab9e94a97eb7920c9de43cf44efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153919"
---
# <a name="cpl_inquire-message"></a><span data-ttu-id="08111-103">CPL \_ mensaje de consulta</span><span class="sxs-lookup"><span data-stu-id="08111-103">CPL\_INQUIRE message</span></span>

<span data-ttu-id="08111-104">Se envía a la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de una aplicación del panel de control para solicitar información sobre un cuadro de diálogo que la aplicación admite.</span><span class="sxs-lookup"><span data-stu-id="08111-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to request information about a dialog box that the application supports.</span></span>

## <a name="parameters"></a><span data-ttu-id="08111-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08111-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08111-106">*uAppNum*</span><span class="sxs-lookup"><span data-stu-id="08111-106">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="08111-107">Número del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="08111-107">The dialog box number.</span></span> <span data-ttu-id="08111-108">Este número debe estar en el intervalo comprendido entre cero y uno menos que el valor devuelto en respuesta al mensaje [**CPL \_ GETCOUNT**](cpl-getcount.md) (CPL \_ getCount – 1).</span><span class="sxs-lookup"><span data-stu-id="08111-108">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="08111-109">*lpcpli*</span><span class="sxs-lookup"><span data-stu-id="08111-109">*lpcpli*</span></span> 
</dt> <dd>

<span data-ttu-id="08111-110">Dirección de una estructura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) .</span><span class="sxs-lookup"><span data-stu-id="08111-110">The address of a [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) structure.</span></span> <span data-ttu-id="08111-111">La aplicación debe rellenar esta estructura con los identificadores de recursos para el icono, el nombre corto, la descripción y cualquier valor definido por el usuario asociado al cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="08111-111">The application must fill this structure with resource identifiers for the icon, short name, description, and any user-defined value associated with the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08111-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08111-112">Return value</span></span>

<span data-ttu-id="08111-113">Si la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) procesa este mensaje correctamente, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="08111-113">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="08111-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="08111-114">Remarks</span></span>

<span data-ttu-id="08111-115">El panel de control envía el mensaje **CPL de \_ consulta** una vez para cada cuadro de diálogo admitido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="08111-115">The Control Panel sends the **CPL\_INQUIRE** message once for each dialog box supported by your application.</span></span> <span data-ttu-id="08111-116">El panel de control también envía un mensaje [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) para cada cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="08111-116">The Control Panel also sends a [**CPL\_NEWINQUIRE**](cpl-newinquire.md) message for each dialog box.</span></span> <span data-ttu-id="08111-117">Estos mensajes se envían inmediatamente después del mensaje [**CPL \_ GETCOUNT**](cpl-getcount.md) .</span><span class="sxs-lookup"><span data-stu-id="08111-117">These messages are sent immediately after the [**CPL\_GETCOUNT**](cpl-getcount.md) message.</span></span> <span data-ttu-id="08111-118">Sin embargo, el sistema no garantiza el orden en el que se envían los mensajes **CPL \_ inquire** y **CPL \_ NEWINQUIRE** .</span><span class="sxs-lookup"><span data-stu-id="08111-118">However, the system does not guarantee the order in which the **CPL\_INQUIRE** and **CPL\_NEWINQUIRE** messages are sent.</span></span>

<span data-ttu-id="08111-119">Puede realizar la inicialización del cuadro de diálogo cuando reciba **CPL \_ consulta**.</span><span class="sxs-lookup"><span data-stu-id="08111-119">You can perform initialization for the dialog box when you receive **CPL\_INQUIRE**.</span></span> <span data-ttu-id="08111-120">Si tiene que asignar memoria, hágalo en respuesta al mensaje [**CPL \_ init**](cpl-init.md) .</span><span class="sxs-lookup"><span data-stu-id="08111-120">If you must allocate memory, do so in response to the [**CPL\_INIT**](cpl-init.md) message.</span></span>

<span data-ttu-id="08111-121">El mensaje [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) devuelve información en un formulario que el sistema no puede almacenar en caché.</span><span class="sxs-lookup"><span data-stu-id="08111-121">The [**CPL\_NEWINQUIRE**](cpl-newinquire.md) message returns information in a form that the system cannot cache.</span></span> <span data-ttu-id="08111-122">Por esta razón, la mayoría de las funciones de [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) deben procesar **CPL \_ inquire** y omitir **CPL \_ NEWINQUIRE**.</span><span class="sxs-lookup"><span data-stu-id="08111-122">For this reason, most [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) functions should process **CPL\_INQUIRE** and ignore **CPL\_NEWINQUIRE**.</span></span>

<span data-ttu-id="08111-123">Las únicas aplicaciones que deben usar [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) son aquellas que necesitan cambiar su icono o mostrar cadenas en función del estado del equipo.</span><span class="sxs-lookup"><span data-stu-id="08111-123">The only applications that should use [**CPL\_NEWINQUIRE**](cpl-newinquire.md) are those that need to change their icon or display strings based on the state of the computer.</span></span> <span data-ttu-id="08111-124">En este caso, el controlador de CPL de la **\_ consulta** debe especificar el valor de CPL \_ Dynamic \_ res para los miembros **idIcon**, **idName** o **idInfo** de la estructura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) , en lugar de especificar un identificador de recursos válido.</span><span class="sxs-lookup"><span data-stu-id="08111-124">In this case, your **CPL\_INQUIRE** handler should specify the CPL\_DYNAMIC\_RES value for the **idIcon**, **idName**, or **idInfo** members of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) structure, rather than specifying a valid resource identifier.</span></span> <span data-ttu-id="08111-125">Esto hace que el panel de control envíe el mensaje **CPL \_ NEWINQUIRE** cada vez que necesite el icono y las cadenas de presentación, lo que le permite especificar información según el estado actual del equipo.</span><span class="sxs-lookup"><span data-stu-id="08111-125">This causes the Control Panel to send the **CPL\_NEWINQUIRE** message each time it needs the icon and display strings, allowing you to specify information based on the current state of the computer.</span></span> <span data-ttu-id="08111-126">Esto es significativamente más lento que el uso de la información almacenada en caché.</span><span class="sxs-lookup"><span data-stu-id="08111-126">This is significantly slower than using cached information.</span></span>

## <a name="requirements"></a><span data-ttu-id="08111-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08111-127">Requirements</span></span>



| <span data-ttu-id="08111-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="08111-128">Requirement</span></span> | <span data-ttu-id="08111-129">Value</span><span class="sxs-lookup"><span data-stu-id="08111-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="08111-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08111-130">Minimum supported client</span></span><br/> | <span data-ttu-id="08111-131">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="08111-131">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="08111-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08111-132">Minimum supported server</span></span><br/> | <span data-ttu-id="08111-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="08111-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="08111-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="08111-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="08111-135"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="08111-135"><dt>Cpl.h</dt></span></span> </dl> |



 

 
