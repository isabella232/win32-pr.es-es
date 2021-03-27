---
description: Se envía para notificar a CPlApplet que el usuario ha elegido el icono asociado a un cuadro de diálogo determinado. CPlApplet debe mostrar el cuadro de diálogo correspondiente y realizar las tareas especificadas por el usuario.
title: Mensaje de CPL_STARTWPARMS (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 04ac5117-39c9-4d3f-b32d-8f8d2b515be1
api_name:
- CPL_STARTWPARMS
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 790779c1c45acbc211fe36e28b2e55d5ae2e60da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000985"
---
# <a name="cpl_startwparms-message"></a><span data-ttu-id="cdc6f-104">CPL \_ STARTWPARMS Message</span><span class="sxs-lookup"><span data-stu-id="cdc6f-104">CPL\_STARTWPARMS message</span></span>

<span data-ttu-id="cdc6f-105">Se envía para notificar a [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) que el usuario ha elegido el icono asociado a un cuadro de diálogo determinado.</span><span class="sxs-lookup"><span data-stu-id="cdc6f-105">Sent to notify [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) that the user has chosen the icon associated with a given dialog box.</span></span> <span data-ttu-id="cdc6f-106">**CPlApplet** debe mostrar el cuadro de diálogo correspondiente y realizar las tareas especificadas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="cdc6f-106">**CPlApplet** should display the corresponding dialog box and carry out any user-specified tasks.</span></span>

## <a name="parameters"></a><span data-ttu-id="cdc6f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cdc6f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdc6f-108">*uAppNum*</span><span class="sxs-lookup"><span data-stu-id="cdc6f-108">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="cdc6f-109">Número del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="cdc6f-109">The dialog box number.</span></span> <span data-ttu-id="cdc6f-110">Este número debe estar en el intervalo comprendido entre cero y uno menos que el valor devuelto en respuesta al mensaje [**CPL \_ GETCOUNT**](cpl-getcount.md) (CPL \_ getCount – 1).</span><span class="sxs-lookup"><span data-stu-id="cdc6f-110">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="cdc6f-111">*lpszExtra*</span><span class="sxs-lookup"><span data-stu-id="cdc6f-111">*lpszExtra*</span></span> 
</dt> <dd>

<span data-ttu-id="cdc6f-112">Cadena con instrucciones adicionales para la ejecución.</span><span class="sxs-lookup"><span data-stu-id="cdc6f-112">A string with additional directions for execution.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdc6f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cdc6f-113">Return value</span></span>

<span data-ttu-id="cdc6f-114">Devuelve **true** si se ha controlado el mensaje o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="cdc6f-114">Returns **TRUE** if the message was handled, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdc6f-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cdc6f-115">Remarks</span></span>

<span data-ttu-id="cdc6f-116">**CPL \_ STARTWPARMS** es similar a [**CPL \_ DBLCLK**](cpl-dblclk.md) , pero le permite pasar una cadena a [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) en lugar de un **int**. Puede utilizar esta cadena como una manera flexible de proporcionar instrucciones detalladas para la ejecución.</span><span class="sxs-lookup"><span data-stu-id="cdc6f-116">**CPL\_STARTWPARMS** is similar to [**CPL\_DBLCLK**](cpl-dblclk.md) but allows you to pass a string to [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) instead of an **int**. You can use this string as a flexible way to provide detailed directions for execution.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdc6f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdc6f-117">Requirements</span></span>



| <span data-ttu-id="cdc6f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdc6f-118">Requirement</span></span> | <span data-ttu-id="cdc6f-119">Value</span><span class="sxs-lookup"><span data-stu-id="cdc6f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cdc6f-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cdc6f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cdc6f-121">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="cdc6f-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="cdc6f-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cdc6f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cdc6f-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cdc6f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cdc6f-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cdc6f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdc6f-125"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdc6f-125"><dt>Cpl.h</dt></span></span> </dl> |



 

 
