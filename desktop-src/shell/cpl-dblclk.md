---
description: Se envía a la función CPlApplet de una aplicación del panel de control cuando el usuario hace doble clic en el icono de un cuadro de diálogo admitido por la aplicación.
title: Mensaje de CPL_DBLCLK (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 68d74372-2fc2-45ed-8f77-574b943d28fa
api_name:
- CPL_DBLCLK
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d6c67204c7b4fae5275e50d428a0371af4cf2e2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997229"
---
# <a name="cpl_dblclk-message"></a><span data-ttu-id="2548d-103">CPL \_ DBLCLK Message</span><span class="sxs-lookup"><span data-stu-id="2548d-103">CPL\_DBLCLK message</span></span>

<span data-ttu-id="2548d-104">Se envía a la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de una aplicación del panel de control cuando el usuario hace doble clic en el icono de un cuadro de diálogo admitido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2548d-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application when the user double-clicks the icon of a dialog box supported by the application.</span></span>

## <a name="parameters"></a><span data-ttu-id="2548d-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2548d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2548d-106">*uAppNum*</span><span class="sxs-lookup"><span data-stu-id="2548d-106">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="2548d-107">Número del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2548d-107">The dialog box number.</span></span> <span data-ttu-id="2548d-108">Este número debe estar en el intervalo comprendido entre cero y uno menos que el valor devuelto en respuesta al mensaje [**CPL \_ GETCOUNT**](cpl-getcount.md) (CPL \_ getCount – 1).</span><span class="sxs-lookup"><span data-stu-id="2548d-108">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="2548d-109">*lData*</span><span class="sxs-lookup"><span data-stu-id="2548d-109">*lData*</span></span> 
</dt> <dd>

<span data-ttu-id="2548d-110">Valor que la aplicación del panel de control cargó en el miembro **lpData** de la estructura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) o [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) para el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2548d-110">The value that the Control Panel application loaded into the **lpData** member of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) or [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) structure for the dialog box.</span></span> <span data-ttu-id="2548d-111">La aplicación carga el miembro **lpData** como respuesta al mensaje [**CPL \_ inquire**](cpl-inquire.md) o [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) .</span><span class="sxs-lookup"><span data-stu-id="2548d-111">The application loads the **lpData** member in response to the [**CPL\_INQUIRE**](cpl-inquire.md) or [**CPL\_NEWINQUIRE**](cpl-newinquire.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2548d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2548d-112">Return value</span></span>

<span data-ttu-id="2548d-113">Si la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) procesa este mensaje correctamente, el valor devuelto es cero; de lo contrario, es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="2548d-113">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, the return value is zero; otherwise, it is nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2548d-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2548d-114">Remarks</span></span>

<span data-ttu-id="2548d-115">En respuesta a este mensaje, una aplicación del panel de control debe mostrar el cuadro de diálogo correspondiente.</span><span class="sxs-lookup"><span data-stu-id="2548d-115">In response to this message, a Control Panel application must display the corresponding dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="2548d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2548d-116">Requirements</span></span>



| <span data-ttu-id="2548d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2548d-117">Requirement</span></span> | <span data-ttu-id="2548d-118">Value</span><span class="sxs-lookup"><span data-stu-id="2548d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2548d-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2548d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2548d-120">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="2548d-120">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2548d-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2548d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2548d-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2548d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2548d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2548d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2548d-124"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2548d-124"><dt>Cpl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2548d-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="2548d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2548d-126">**CPL \_ Select**</span><span class="sxs-lookup"><span data-stu-id="2548d-126">**CPL\_SELECT**</span></span>](cpl-select.md)
</dt> </dl>

 

 
