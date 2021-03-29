---
title: Funciones de devolución de llamada de aplicación cliente
description: Dos tipos de firmas de devolución de llamada.
ms.assetid: 5569BFF3-9EEC-42E6-8F63-0C569C68FA74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371edd162c4cbd1332764c7b3e9e70bf114270e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419003"
---
# <a name="client-application-callback-functions"></a><span data-ttu-id="446db-103">Funciones de devolución de llamada de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="446db-103">Client Application Callback Functions</span></span>

<span data-ttu-id="446db-104">El Plataforma de biometría de Windows admite dos tipos de firmas de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="446db-104">The Windows Biometric Framework supports two types of callback signatures.</span></span> <span data-ttu-id="446db-105">A partir de Windows 8, se admite la siguiente devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="446db-105">Beginning with Windows 8, the following callback is supported.</span></span> <span data-ttu-id="446db-106">Se recomienda implementar esta devolución de llamada para todas las aplicaciones nuevas.</span><span class="sxs-lookup"><span data-stu-id="446db-106">We recommend that you implement this callback for all new applications.</span></span> <span data-ttu-id="446db-107">No obstante, esta devolución de llamada no se puede usar en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="446db-107">This callback cannot, however, be used in Windows 7.</span></span>



| <span data-ttu-id="446db-108">Devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="446db-108">Callback</span></span>                                                                                     | <span data-ttu-id="446db-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="446db-109">Description</span></span>                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="446db-110">**\_devolución de \_ llamada de finalización ASINCRÓNICA de PWINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="446db-110">**PWINBIO\_ASYNC\_COMPLETION\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_async_completion_callback)<br/> | <span data-ttu-id="446db-111">Notifica a la aplicación cliente que se ha completado una operación asincrónica iniciada mediante [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession) o [**WinBioAsyncOpenFramework**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopenframework) .</span><span class="sxs-lookup"><span data-stu-id="446db-111">Notifies the client application that an asynchronous operation started by using [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession) or [**WinBioAsyncOpenFramework**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopenframework) has completed.</span></span><br/> |



 

<span data-ttu-id="446db-112">Las siguientes funciones de devolución de llamada se introdujeron en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="446db-112">The following callback functions were introduced in Windows 7.</span></span> <span data-ttu-id="446db-113">Se recomienda no implementarlas para las nuevas aplicaciones destinadas a Windows 8 y sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="446db-113">We recommend that you do not implement them for new applications that target Windows 8 and later operating systems.</span></span>



| <span data-ttu-id="446db-114">Devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="446db-114">Callback</span></span>                                                                                 | <span data-ttu-id="446db-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="446db-115">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="446db-116">**devolución de llamada de \_ captura PWINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="446db-116">**PWINBIO\_CAPTURE\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_capture_callback)<br/>                | <span data-ttu-id="446db-117">Devuelve los resultados de la función [**WinBioCaptureSampleWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesamplewithcallback) asincrónica.</span><span class="sxs-lookup"><span data-stu-id="446db-117">Returns results from the asynchronous [**WinBioCaptureSampleWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesamplewithcallback) function.</span></span><br/> |
| [<span data-ttu-id="446db-118">**\_devolución de \_ llamada de captura de inscripción de PWINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="446db-118">**PWINBIO\_ENROLL\_CAPTURE\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_enroll_capture_callback)<br/> | <span data-ttu-id="446db-119">Devuelve los resultados de la función [**WinBioEnrollCaptureWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback) asincrónica.</span><span class="sxs-lookup"><span data-stu-id="446db-119">Returns results from the asynchronous [**WinBioEnrollCaptureWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback) function.</span></span><br/> |
| [<span data-ttu-id="446db-120">**devolución de llamada de \_ evento PWINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="446db-120">**PWINBIO\_EVENT\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_event_callback)<br/>                    | <span data-ttu-id="446db-121">Devuelve los resultados de la función [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) asincrónica.</span><span class="sxs-lookup"><span data-stu-id="446db-121">Returns results from the asynchronous [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) function.</span></span><br/>           |
| [<span data-ttu-id="446db-122">**PWINBIO \_ identificar \_ devolución de llamada**</span><span class="sxs-lookup"><span data-stu-id="446db-122">**PWINBIO\_IDENTIFY\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_identify_callback)<br/>              | <span data-ttu-id="446db-123">Devuelve los resultados de la función [**WinBioIdentifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioidentifywithcallback) asincrónica.</span><span class="sxs-lookup"><span data-stu-id="446db-123">Returns results from the asynchronous [**WinBioIdentifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioidentifywithcallback) function.</span></span><br/>           |
| [<span data-ttu-id="446db-124">**PWINBIO \_ Buscar \_ devolución de llamada del sensor \_**</span><span class="sxs-lookup"><span data-stu-id="446db-124">**PWINBIO\_LOCATE\_SENSOR\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_locate_sensor_callback)<br/>   | <span data-ttu-id="446db-125">Devuelve los resultados de la función [**WinBioLocateSensorWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback) asincrónica.</span><span class="sxs-lookup"><span data-stu-id="446db-125">Returns results from the asynchronous [**WinBioLocateSensorWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback) function.</span></span><br/>   |
| [<span data-ttu-id="446db-126">**PWINBIO \_ comprobar \_ devolución de llamada**</span><span class="sxs-lookup"><span data-stu-id="446db-126">**PWINBIO\_VERIFY\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_verify_callback)<br/>                  | <span data-ttu-id="446db-127">Devuelve los resultados de la función [**WinBioVerifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback) asincrónica.</span><span class="sxs-lookup"><span data-stu-id="446db-127">Returns results from the asynchronous [**WinBioVerifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback) function.</span></span><br/>               |



 

## <a name="related-topics"></a><span data-ttu-id="446db-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="446db-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="446db-129">Referencia de la aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="446db-129">Client Application Reference</span></span>](client-application-reference.md)
</dt> </dl>

 

 





