---
title: Novedades de WER
description: En esta página se resumen las nuevas características de Informe de errores de Windows (WER) de cada versión.
ms.assetid: 6cdd6c64-ba67-40dc-9942-0371320f1881
keywords:
- Informe de errores de Windows Informe de errores de Windows, novedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526776de3c5f88400e7cfae7ed9b9717318c223d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104358811"
---
# <a name="whats-new-in-wer"></a><span data-ttu-id="f0c71-104">Novedades de WER</span><span class="sxs-lookup"><span data-stu-id="f0c71-104">What's New in WER</span></span>

<span data-ttu-id="f0c71-105">En esta página se resumen las nuevas características de Informe de errores de Windows (WER) de cada versión.</span><span class="sxs-lookup"><span data-stu-id="f0c71-105">This page summarizes the new features of Windows Error Reporting (WER) for each release.</span></span>

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="f0c71-106">Windows 7 y Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f0c71-106">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="f0c71-107">En la lista siguiente se resumen las nuevas características de WER para Windows 7 y Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="f0c71-107">The following list summarizes the new WER features for Windows 7 and Windows Server 2008 R2.</span></span>

-   <span data-ttu-id="f0c71-108">Agrega la capacidad de producir una excepción que omite todos los controladores de excepciones y, por tanto, finaliza la aplicación inmediatamente e invoca Informe de errores de Windows.</span><span class="sxs-lookup"><span data-stu-id="f0c71-108">Adds the ability to raise an exception that bypasses all exception handlers thus terminating the application immediately and invoking Windows Error Reporting.</span></span> <span data-ttu-id="f0c71-109">Para obtener más información, consulte la función [**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f0c71-109">For details, see the [**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85)) function.</span></span>
-   <span data-ttu-id="f0c71-110">Agrega la capacidad de registrar un controlador de excepciones fuera de proceso al que WER llama cuando se produce un bloqueo para recopilar el nombre del evento, los parámetros de informes y las opciones de inicio de depuración.</span><span class="sxs-lookup"><span data-stu-id="f0c71-110">Adds the ability to register an out-of-process exception handler that WER calls when a crash occurs to collect the event name, reporting parameters, and debug launching options.</span></span> <span data-ttu-id="f0c71-111">Para obtener más información, consulte la función [**WerRegisterRuntimeExceptionModule**](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule) .</span><span class="sxs-lookup"><span data-stu-id="f0c71-111">For details, see the [**WerRegisterRuntimeExceptionModule**](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule) function.</span></span>

<span data-ttu-id="f0c71-112">Funciones que se agregaron:</span><span class="sxs-lookup"><span data-stu-id="f0c71-112">Functions that were added:</span></span>

-   [<span data-ttu-id="f0c71-113">**OutOfProcessExceptionEventCallback**</span><span class="sxs-lookup"><span data-stu-id="f0c71-113">**OutOfProcessExceptionEventCallback**</span></span>](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_event)
-   [<span data-ttu-id="f0c71-114">**OutOfProcessExceptionEventSignatureCallback**</span><span class="sxs-lookup"><span data-stu-id="f0c71-114">**OutOfProcessExceptionEventSignatureCallback**</span></span>](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_event_signature)
-   [<span data-ttu-id="f0c71-115">**OutOfProcessExceptionEventDebuggerLaunchCallback**</span><span class="sxs-lookup"><span data-stu-id="f0c71-115">**OutOfProcessExceptionEventDebuggerLaunchCallback**</span></span>](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_debugger_launch)
-   <span data-ttu-id="f0c71-116">[**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f0c71-116">[**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85))</span></span>
-   [<span data-ttu-id="f0c71-117">**WerRegisterRuntimeExceptionModule**</span><span class="sxs-lookup"><span data-stu-id="f0c71-117">**WerRegisterRuntimeExceptionModule**</span></span>](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule)
-   [<span data-ttu-id="f0c71-118">**WerUnregisterRuntimeExceptionModule**</span><span class="sxs-lookup"><span data-stu-id="f0c71-118">**WerUnregisterRuntimeExceptionModule**</span></span>](/windows/desktop/api/Werapi/nf-werapi-werunregisterruntimeexceptionmodule)

<span data-ttu-id="f0c71-119">Estructuras agregadas:</span><span class="sxs-lookup"><span data-stu-id="f0c71-119">Structures that were added:</span></span>

-   [<span data-ttu-id="f0c71-120">**\_información de \_ excepción en tiempo de ejecución de Wer \_**</span><span class="sxs-lookup"><span data-stu-id="f0c71-120">**WER\_RUNTIME\_EXCEPTION\_INFORMATION**</span></span>](/windows/desktop/api/Werapi/ns-werapi-wer_runtime_exception_information)

## <a name="windows-server-2008-and-windows-vista-sp1"></a><span data-ttu-id="f0c71-121">Windows Server 2008 y Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="f0c71-121">Windows Server 2008 and Windows Vista SP1</span></span>

<span data-ttu-id="f0c71-122">En la lista siguiente se resumen las nuevas características de WER para Windows Server 2008 y Windows Vista con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f0c71-122">The following list summarizes the new features of WER for Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

-   <span data-ttu-id="f0c71-123">WER puede configurarse para que los volcados de modo de usuario completos se recopilen y almacenen localmente después de que una aplicación de modo de usuario se bloquee (no se admiten las aplicaciones que realizan sus propios informes de bloqueo personalizados, incluidas las aplicaciones .NET).</span><span class="sxs-lookup"><span data-stu-id="f0c71-123">WER can be configured so that full user-mode dumps are collected and stored locally after a user-mode application crashes (applications that do their own custom crash reporting, including .NET applications are not supported).</span></span> <span data-ttu-id="f0c71-124">Para obtener más información, consulte [recopilación de volcados de User-Mode](collecting-user-mode-dumps.md).</span><span class="sxs-lookup"><span data-stu-id="f0c71-124">For more information, see [Collecting User-Mode Dumps](collecting-user-mode-dumps.md).</span></span>

## <a name="windows-vista"></a><span data-ttu-id="f0c71-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f0c71-125">Windows Vista</span></span>

<span data-ttu-id="f0c71-126">En la lista siguiente se resumen las nuevas características de Informe de errores de Windows (WER) para Windows Vista:</span><span class="sxs-lookup"><span data-stu-id="f0c71-126">The following list summarizes the new features of Windows Error Reporting (WER) for Windows Vista:</span></span>

-   <span data-ttu-id="f0c71-127">WER se ha extendido más allá de los bloqueos de supervisión y los procesos que no responden.</span><span class="sxs-lookup"><span data-stu-id="f0c71-127">WER has been extended beyond monitoring crashes and unresponsive processes.</span></span> <span data-ttu-id="f0c71-128">WER incluye compatibilidad con muchos nuevos tipos de eventos no críticos, como problemas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="f0c71-128">WER includes support for many new types of non-critical events, such as performance issues.</span></span> <span data-ttu-id="f0c71-129">Esto permite a los desarrolladores obtener más información sobre las experiencias que tienen sus clientes con las aplicaciones que han desarrollado.</span><span class="sxs-lookup"><span data-stu-id="f0c71-129">This enables developers to learn more about the experiences their customers have with the applications they have developed.</span></span>
-   <span data-ttu-id="f0c71-130">Las nuevas funciones proporcionan a los desarrolladores la flexibilidad necesaria para crear, personalizar y enviar informes de problemas.</span><span class="sxs-lookup"><span data-stu-id="f0c71-130">New functions give developers the flexibility in creating, customizing, and submitting problem reports.</span></span> <span data-ttu-id="f0c71-131">Para obtener más información, vea [funciones wer](wer-functions.md).</span><span class="sxs-lookup"><span data-stu-id="f0c71-131">For more information, see [WER Functions](wer-functions.md).</span></span>
-   <span data-ttu-id="f0c71-132">Los [servicios en línea de calidad de Windows](https://www.microsoft.com/?ref=go) mejorados proporcionan a los desarrolladores acceso a la información de problemas que los clientes envían para sus aplicaciones y un mecanismo para ofrecer soluciones a estos clientes.</span><span class="sxs-lookup"><span data-stu-id="f0c71-132">The improved [Windows Quality Online Services](https://www.microsoft.com/?ref=go) provides developers with access to the problem information that customers are submitting for their applications, and a mechanism to deliver solutions to these customers.</span></span>
-   <span data-ttu-id="f0c71-133">Las funciones introducidas por la [recuperación de aplicaciones y](/windows/desktop/Recovery/application-recovery-and-restart-portal) el [Administrador](/windows/desktop/RstMgr/restart-manager-portal) de reinicio y reinicio permiten a las aplicaciones recuperar información automáticamente y reiniciarse en caso de un error crítico.</span><span class="sxs-lookup"><span data-stu-id="f0c71-133">The functions introduced by [Application Recovery and Restart](/windows/desktop/Recovery/application-recovery-and-restart-portal) and [Restart Manager](/windows/desktop/RstMgr/restart-manager-portal) enable applications to automatically recover information and restart in the event of a critical failure.</span></span> <span data-ttu-id="f0c71-134">Los desarrolladores pueden usar estas características en sus aplicaciones para mejorar significativamente la experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="f0c71-134">Developers can use these features in their applications to significantly improve their user experience.</span></span>
-   <span data-ttu-id="f0c71-135">**Informes de problemas y soluciones en Windows Vista o en el centro de actividades de Windows 7** es la ubicación central para que los usuarios interactúen con wer.</span><span class="sxs-lookup"><span data-stu-id="f0c71-135">**Problem Reports and Solutions on Windows Vista or the Action Center on Windows 7** is the central location for users to interact with WER.</span></span> <span data-ttu-id="f0c71-136">Los usuarios pueden buscar nuevas soluciones, administrar su historial de informes, ver los detalles de un informe de problemas y administrar la configuración de informes, incluida la habilitación de WER para buscar soluciones automáticamente sin interrumpir al usuario.</span><span class="sxs-lookup"><span data-stu-id="f0c71-136">Users can check for new solutions, manage their reporting history, view the details of a problem report, and manage reporting settings including enabling WER to check for solutions automatically without interrupting the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0c71-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f0c71-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0c71-138">Informe de errores de Windows</span><span class="sxs-lookup"><span data-stu-id="f0c71-138">Windows Error Reporting</span></span>](windows-error-reporting.md)
</dt> </dl>

 

 