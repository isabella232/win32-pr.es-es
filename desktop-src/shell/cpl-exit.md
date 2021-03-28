---
description: Se envía una vez a la función CPlApplet de una aplicación del panel de control antes de que se libere el archivo DLL que contiene la aplicación del panel de control.
ms.assetid: 1afcb0d3-41a7-4fd8-9561-d96e1e8f0ddb
title: Mensaje de CPL_EXIT (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0adea6c4b05ee752829634f7478df2ac651e69f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275241"
---
# <a name="cpl_exit-message"></a><span data-ttu-id="98fb5-103">CPL \_ mensaje de salida</span><span class="sxs-lookup"><span data-stu-id="98fb5-103">CPL\_EXIT message</span></span>

<span data-ttu-id="98fb5-104">Se envía una vez a la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de una aplicación del panel de control antes de que se libere el archivo DLL que contiene la aplicación del panel de control.</span><span class="sxs-lookup"><span data-stu-id="98fb5-104">Sent once to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application before the DLL containing the Control Panel application is released.</span></span>

## <a name="parameters"></a><span data-ttu-id="98fb5-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98fb5-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98fb5-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="98fb5-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="98fb5-107">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="98fb5-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="98fb5-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="98fb5-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="98fb5-109">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="98fb5-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98fb5-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98fb5-110">Return value</span></span>

<span data-ttu-id="98fb5-111">Si la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) procesa este mensaje correctamente, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="98fb5-111">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="98fb5-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98fb5-112">Remarks</span></span>

<span data-ttu-id="98fb5-113">Este mensaje se envía después de enviar el último mensaje de [**\_ detención de CPL**](cpl-stop.md) .</span><span class="sxs-lookup"><span data-stu-id="98fb5-113">This message is sent after the last [**CPL\_STOP**](cpl-stop.md) message is sent.</span></span>

<span data-ttu-id="98fb5-114">En respuesta a este mensaje, una aplicación del panel de control debe liberar cualquier memoria que haya asignado y realizar la limpieza de nivel global.</span><span class="sxs-lookup"><span data-stu-id="98fb5-114">In response to this message, a Control Panel application must free any memory that it has allocated and perform global-level cleanup.</span></span>

## <a name="requirements"></a><span data-ttu-id="98fb5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98fb5-115">Requirements</span></span>



| <span data-ttu-id="98fb5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="98fb5-116">Requirement</span></span> | <span data-ttu-id="98fb5-117">Value</span><span class="sxs-lookup"><span data-stu-id="98fb5-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="98fb5-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98fb5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="98fb5-119">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="98fb5-119">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="98fb5-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98fb5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="98fb5-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="98fb5-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="98fb5-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98fb5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="98fb5-123"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="98fb5-123"><dt>Cpl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98fb5-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="98fb5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98fb5-125">**FreeLibrary**</span><span class="sxs-lookup"><span data-stu-id="98fb5-125">**FreeLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> </dl>

 

 
