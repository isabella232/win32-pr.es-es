---
title: Constantes de WINBIO_EVENT (Winbio \_ Types. h)
description: Especifique los tipos de notificaciones de eventos del proveedor de servicios que se van a supervisar.
ms.assetid: 73805413-a8d9-4682-aa21-7032451d750a
topic_type:
- apiref
api_name:
- WINBIO_EVENT_FP_UNCLAIMED
- WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 182a4ffe254e946f1b8deca2c5034e665a58f7ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533861"
---
# <a name="winbio_event-constants"></a><span data-ttu-id="f3324-103">\_Constantes de evento WINBIO</span><span class="sxs-lookup"><span data-stu-id="f3324-103">WINBIO\_EVENT Constants</span></span>

<span data-ttu-id="f3324-104">Se pueden usar las siguientes constantes en la función [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) para especificar los tipos de notificaciones de eventos del proveedor de servicios que se van a supervisar.</span><span class="sxs-lookup"><span data-stu-id="f3324-104">The following constants can be used in the [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) function to specify the types of service provider event notifications to monitor.</span></span>



| <span data-ttu-id="f3324-105">Constante</span><span class="sxs-lookup"><span data-stu-id="f3324-105">Constant</span></span>                                                                                                                                                                                                                        | <span data-ttu-id="f3324-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3324-106">Description</span></span>                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span><dl> <span data-ttu-id="f3324-107"><dt>**\_evento WINBIO \_ FP no \_ reclamado**</dt></span><span class="sxs-lookup"><span data-stu-id="f3324-107"><dt>**WINBIO\_EVENT\_FP\_UNCLAIMED**</dt></span></span> </dl>                             | <span data-ttu-id="f3324-108">El sensor ha detectado un dedo deslizante que no ha solicitado la aplicación o que la ventana tiene el foco actualmente.</span><span class="sxs-lookup"><span data-stu-id="f3324-108">The sensor detected a finger swipe that was not requested by the application or by the window that currently has focus.</span></span> <span data-ttu-id="f3324-109">El Plataforma de biometría de Windows llama a la función de devolución de llamada para indicar que se ha producido un deslizamiento de dedo pero no intenta identificar la huella digital.</span><span class="sxs-lookup"><span data-stu-id="f3324-109">The Windows Biometric Framework calls into your callback function to indicate that a finger swipe has occurred but does not try to identify the fingerprint.</span></span><br/> |
| <span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span><dl> <span data-ttu-id="f3324-110"><dt>**\_identificación no \_ \_ reclamada del evento WINBIO FP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f3324-110"><dt>**WINBIO\_EVENT\_FP\_UNCLAIMED\_IDENTIFY**</dt></span></span> </dl> | <span data-ttu-id="f3324-111">El sensor ha detectado un dedo deslizante que no ha solicitado la aplicación o que la ventana tiene el foco actualmente.</span><span class="sxs-lookup"><span data-stu-id="f3324-111">The sensor detected a finger swipe that was not requested by the application or by the window that currently has focus.</span></span> <span data-ttu-id="f3324-112">El Plataforma de biometría de Windows intenta identificar la huella digital y pasa el resultado de ese proceso a la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="f3324-112">The Windows Biometric Framework attempts to identify the fingerprint and passes the result of that process to your callback function.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="f3324-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3324-113">Requirements</span></span>



| <span data-ttu-id="f3324-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3324-114">Requirement</span></span> | <span data-ttu-id="f3324-115">Value</span><span class="sxs-lookup"><span data-stu-id="f3324-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3324-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3324-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f3324-117">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="f3324-117">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="f3324-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3324-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f3324-119">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f3324-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f3324-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f3324-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3324-121"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f3324-121"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3324-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3324-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3324-123">Constantes de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="f3324-123">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





