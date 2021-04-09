---
description: Los registros de WinHTTP se pueden utilizar para ayudar a solucionar problemas de las aplicaciones WSDAPI. Esto resulta útil cuando se produce un error de intercambio de metadatos o cuando se produce un error en la negociación SSL/TLS.
ms.assetid: 75ba330d-afcd-4d8f-93c7-a1b9f80dd050
title: Captura de registros de WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378801e97b2eef8c1ea0c40a5973844d75a94e02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155989"
---
# <a name="capturing-winhttp-logs"></a><span data-ttu-id="16578-104">Captura de registros de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="16578-104">Capturing WinHTTP Logs</span></span>

<span data-ttu-id="16578-105">Los registros de [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) se pueden utilizar para ayudar a solucionar problemas de las aplicaciones WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="16578-105">[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) logs can be used to help troubleshoot WSDAPI applications.</span></span> <span data-ttu-id="16578-106">Esto resulta útil cuando se produce un error de intercambio de metadatos o cuando se produce un error en la negociación SSL/TLS.</span><span class="sxs-lookup"><span data-stu-id="16578-106">This is helpful when metadata exchange fails or when SSL/TLS negotiation fails.</span></span>

<span data-ttu-id="16578-107">Este procedimiento muestra cómo capturar los registros de WinHTTP en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="16578-107">This procedure shows how to capture WinHTTP logs on the client PC.</span></span> <span data-ttu-id="16578-108">La aplicación cliente basada en WSDAPI no debe estar en ejecución cuando el registro está habilitado.</span><span class="sxs-lookup"><span data-stu-id="16578-108">The WSDAPI-based client application must not be running when logging is enabled.</span></span> <span data-ttu-id="16578-109">Si la aplicación cliente se está ejecutando cuando el registro está habilitado, el cliente o el equipo deben reiniciarse antes de WS-Discovery y el tráfico de intercambio de metadatos aparecerá en los registros de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="16578-109">If the client application is running when logging is enabled, the client and/or the PC must be restarted before WS-Discovery and metadata exchange traffic will appear in the WinHTTP logs.</span></span>

<span data-ttu-id="16578-110">**Para capturar registros de WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="16578-110">**To capture WinHTTP logs**</span></span>

1.  <span data-ttu-id="16578-111">Abra una ventana de símbolo del sistema con privilegios elevados en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="16578-111">Open an elevated command prompt window on the client PC.</span></span>
2.  <span data-ttu-id="16578-112">Ejecute el siguiente comando: **netsh WinHTTP Set Tracing Trace-File-prefix = "C: \\ temp \\ DPWS" LEVEL = verbose Format = ANSI State = Enabled Max-Trace-File-size = 1073741824**</span><span class="sxs-lookup"><span data-stu-id="16578-112">Run the following command: **netsh winhttp set tracing trace-file-prefix="C:\\Temp\\dpws" level=verbose format=ansi state=enabled max-trace-file-size=1073741824**</span></span>

    <span data-ttu-id="16578-113">Este comando habilita el registro de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="16578-113">This command enables WinHTTP logging.</span></span> <span data-ttu-id="16578-114">Todos los archivos de registro se almacenarán en el \\ directorio C: Temp y los nombres de archivo comenzarán con el prefijo DPWS.</span><span class="sxs-lookup"><span data-stu-id="16578-114">All log files will be stored in the C:\\Temp directory, and the filenames will begin with the dpws prefix.</span></span> <span data-ttu-id="16578-115">Se almacenarán al menos 1 GB de archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="16578-115">At most 1 GB of log files will be stored.</span></span>

3.  <span data-ttu-id="16578-116">Si el proceso que usa WinHTTP en el cliente ya se está ejecutando, reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="16578-116">If the process using WinHTTP on the client is already running, restart the computer.</span></span> <span data-ttu-id="16578-117">Por ejemplo, si se usan las API de [detección de funciones](/previous-versions/windows/desktop/fundisc/fd-portal) , el equipo debe reiniciarse.</span><span class="sxs-lookup"><span data-stu-id="16578-117">For example, if the [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) APIs are being used, the computer must be restarted.</span></span> <span data-ttu-id="16578-118">Las API de detección de funciones llaman a WinHTTP desde dentro de un host de servicio, que puede haberse iniciado ya cuando se habilitó el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="16578-118">The Function Discovery APIs call WinHTTP from inside a service host, which may have already started when tracing was enabled.</span></span>
4.  <span data-ttu-id="16578-119">Inicie la aplicación cliente basada en WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="16578-119">Start the WSDAPI-based client application.</span></span> <span data-ttu-id="16578-120">Se puede usar la aplicación que se está depurando o el cliente de depuración WSD.</span><span class="sxs-lookup"><span data-stu-id="16578-120">The application being debugged or the WSD Debug Client can be used.</span></span>
5.  <span data-ttu-id="16578-121">Reproduzca el error de aplicación.</span><span class="sxs-lookup"><span data-stu-id="16578-121">Reproduce the application failure.</span></span>
6.  <span data-ttu-id="16578-122">Finalice la aplicación cliente basada en WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="16578-122">Terminate the WSDAPI-based client application.</span></span>
7.  <span data-ttu-id="16578-123">Si el proceso que usa WinHTTP no finaliza con la aplicación cliente, reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="16578-123">If the process using WinHTTP is not terminated with the client application, restart the computer.</span></span> <span data-ttu-id="16578-124">Por ejemplo, si se usan las API de [detección de funciones](/previous-versions/windows/desktop/fundisc/fd-portal) , el equipo debe reiniciarse.</span><span class="sxs-lookup"><span data-stu-id="16578-124">For example, if the [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) APIs are being used, the computer must be restarted.</span></span>
8.  <span data-ttu-id="16578-125">Ejecute el siguiente comando: **netsh WinHTTP Set Tracing state = disabled**</span><span class="sxs-lookup"><span data-stu-id="16578-125">Run the following command: **netsh winhttp set tracing state=disabled**</span></span>

    <span data-ttu-id="16578-126">Este comando deshabilita el registro de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="16578-126">This command disables WinHTTP logging.</span></span>

9.  <span data-ttu-id="16578-127">Inspeccione los registros de DPWS en C: \\ temp y compruebe que se enviaron las solicitudes y los mensajes necesarios.</span><span class="sxs-lookup"><span data-stu-id="16578-127">Inspect the DPWS logs in C:\\Temp and verify that the required requests and messages were sent.</span></span>
10. <span data-ttu-id="16578-128">Si se usa la comunicación de canal seguro (HTTPS), compruebe si hay errores de SSL/TLS.</span><span class="sxs-lookup"><span data-stu-id="16578-128">If secure channel (HTTPS) communication is being used, check for SSL/TLS failures.</span></span>

<span data-ttu-id="16578-129">Una vez capturados los registros de WinHTTP, se pueden examinar los registros para buscar la causa de un error de la aplicación WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="16578-129">Once WinHTTP logs have been captured, the logs can be examined to look for the cause of a WSDAPI application failure.</span></span> <span data-ttu-id="16578-130">Tenga en cuenta que el editor de texto que se usa para ver estos registros debe ejecutarse como administrador.</span><span class="sxs-lookup"><span data-stu-id="16578-130">Note that the text editor used to view these logs must be run as Administrator.</span></span> <span data-ttu-id="16578-131">Para obtener más información, consulte [uso del registro de WinHTTP para comprobar el tráfico Get](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="16578-131">For more information, see [Using WinHTTP Logging to Verify Get Traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="16578-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="16578-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16578-133">WinHTTP</span><span class="sxs-lookup"><span data-stu-id="16578-133">WinHTTP</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[<span data-ttu-id="16578-134">Uso del registro de WinHTTP para comprobar el tráfico Get</span><span class="sxs-lookup"><span data-stu-id="16578-134">Using WinHTTP Logging to Verify Get Traffic</span></span>](using-winhttp-logging-to-verify-get-traffic.md)
</dt>
</dl>
