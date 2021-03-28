---
description: Se envía a la función CPlApplet de una aplicación del panel de control para recuperar el número de cuadros de diálogo admitidos por la aplicación.
title: Mensaje de CPL_GETCOUNT (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6b88b56c-aad7-4144-ab95-15d7eef21861
api_name:
- CPL_GETCOUNT
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3bf8980fa29841d3c5341daeeccf26cea05db80c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540547"
---
# <a name="cpl_getcount-message"></a><span data-ttu-id="daca3-103">CPL \_ mensaje GETCOUNT</span><span class="sxs-lookup"><span data-stu-id="daca3-103">CPL\_GETCOUNT message</span></span>

<span data-ttu-id="daca3-104">Se envía a la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de una aplicación del panel de control para recuperar el número de cuadros de diálogo admitidos por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="daca3-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to retrieve the number of dialog boxes supported by the application.</span></span>

## <a name="parameters"></a><span data-ttu-id="daca3-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="daca3-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="daca3-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="daca3-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="daca3-107">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="daca3-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="daca3-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="daca3-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="daca3-109">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="daca3-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="daca3-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="daca3-110">Return value</span></span>

<span data-ttu-id="daca3-111">La función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) devuelve el número de cuadros de diálogo que admite la aplicación del panel de control.</span><span class="sxs-lookup"><span data-stu-id="daca3-111">The [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function returns the number of dialog boxes that the Control Panel application supports.</span></span>

## <a name="remarks"></a><span data-ttu-id="daca3-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="daca3-112">Remarks</span></span>

<span data-ttu-id="daca3-113">Este mensaje se envía inmediatamente después del mensaje [**CPL \_ init**](cpl-init.md) .</span><span class="sxs-lookup"><span data-stu-id="daca3-113">This message is sent immediately after the [**CPL\_INIT**](cpl-init.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="daca3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="daca3-114">Requirements</span></span>



| <span data-ttu-id="daca3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="daca3-115">Requirement</span></span> | <span data-ttu-id="daca3-116">Value</span><span class="sxs-lookup"><span data-stu-id="daca3-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="daca3-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="daca3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="daca3-118">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="daca3-118">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="daca3-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="daca3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="daca3-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="daca3-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="daca3-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="daca3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="daca3-122"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="daca3-122"><dt>Cpl.h</dt></span></span> </dl> |



 

 
