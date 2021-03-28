---
description: Se envía a la función CPlApplet de una aplicación del panel de control cuando se cierra la aplicación de control del panel de control. La aplicación de control envía el mensaje una vez por cada cuadro de diálogo que admita la aplicación.
title: Mensaje de CPL_STOP (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4f632b91-8200-42a3-90cc-a98889704ca4
api_name:
- CPL_STOP
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 78f8926d85b35b8cf5e55188c6cd76b014b3c4c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984330"
---
# <a name="cpl_stop-message"></a><span data-ttu-id="d5c19-104">CPL \_ detener mensaje</span><span class="sxs-lookup"><span data-stu-id="d5c19-104">CPL\_STOP message</span></span>

<span data-ttu-id="d5c19-105">Se envía a la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de una aplicación del panel de control cuando se cierra la aplicación de control del panel de control.</span><span class="sxs-lookup"><span data-stu-id="d5c19-105">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application when the controlling application of the Control Panel closes.</span></span> <span data-ttu-id="d5c19-106">La aplicación de control envía el mensaje una vez por cada cuadro de diálogo que admita la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d5c19-106">The controlling application sends the message once for each dialog box that the application supports.</span></span>

## <a name="parameters"></a><span data-ttu-id="d5c19-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5c19-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5c19-108">*uAppNum*</span><span class="sxs-lookup"><span data-stu-id="d5c19-108">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="d5c19-109">Número del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d5c19-109">The dialog box number.</span></span>

</dd> <dt>

<span data-ttu-id="d5c19-110">*lData*</span><span class="sxs-lookup"><span data-stu-id="d5c19-110">*lData*</span></span> 
</dt> <dd>

<span data-ttu-id="d5c19-111">Valor que la aplicación del panel de control cargó en el miembro **lpData** de la estructura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) o [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) para el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d5c19-111">The value that the Control Panel application loaded into the **lpData** member of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) or [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) structure for the dialog box.</span></span> <span data-ttu-id="d5c19-112">La aplicación carga el miembro **lpData** como respuesta al mensaje [**CPL \_ inquire**](cpl-inquire.md) o [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) .</span><span class="sxs-lookup"><span data-stu-id="d5c19-112">The application loads the **lpData** member in response to the [**CPL\_INQUIRE**](cpl-inquire.md) or [**CPL\_NEWINQUIRE**](cpl-newinquire.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5c19-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5c19-113">Return value</span></span>

<span data-ttu-id="d5c19-114">Si la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) procesa este mensaje correctamente, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="d5c19-114">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5c19-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5c19-115">Remarks</span></span>

<span data-ttu-id="d5c19-116">En respuesta a este mensaje, una aplicación del panel de control debe realizar la limpieza para el cuadro de diálogo especificado.</span><span class="sxs-lookup"><span data-stu-id="d5c19-116">In response to this message, a Control Panel application must perform cleanup for the given dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5c19-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5c19-117">Requirements</span></span>



| <span data-ttu-id="d5c19-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5c19-118">Requirement</span></span> | <span data-ttu-id="d5c19-119">Value</span><span class="sxs-lookup"><span data-stu-id="d5c19-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d5c19-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5c19-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d5c19-121">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d5c19-121">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d5c19-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5c19-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d5c19-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d5c19-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d5c19-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5c19-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5c19-125"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5c19-125"><dt>Cpl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5c19-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5c19-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5c19-127">**salir de CPL \_**</span><span class="sxs-lookup"><span data-stu-id="d5c19-127">**CPL\_EXIT**</span></span>](cpl-exit.md)
</dt> <dt>

[<span data-ttu-id="d5c19-128">**CPL \_ GETCOUNT**</span><span class="sxs-lookup"><span data-stu-id="d5c19-128">**CPL\_GETCOUNT**</span></span>](cpl-getcount.md)
</dt> </dl>

 

 
