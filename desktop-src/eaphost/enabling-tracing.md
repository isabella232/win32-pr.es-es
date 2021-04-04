---
title: Habilitación del seguimiento de EAPHost
description: Puede ayudar a los usuarios a encontrar las causas raíz de los problemas que se producen durante el proceso de autenticación de EAP. La información de depuración puede incluir llamadas API realizadas, llamadas a funciones internas realizadas y transiciones de estado realizadas.
ms.assetid: 5f401101-59aa-4ee8-825a-0b998489eed9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fdee8a5516b218e51f0151e1964885789560d82
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "104078644"
---
# <a name="enabling-eaphost-tracing"></a><span data-ttu-id="21637-104">Habilitación del seguimiento de EAPHost</span><span class="sxs-lookup"><span data-stu-id="21637-104">Enabling EAPHost Tracing</span></span>

<span data-ttu-id="21637-105">Los registros de seguimiento que contienen información de depuración pueden ayudar a los usuarios a encontrar las causas raíz de los problemas que se producen durante el proceso de autenticación de EAP.</span><span class="sxs-lookup"><span data-stu-id="21637-105">Trace logs containing debugging information can assist users in finding the root causes of issues that occur during the EAP authentication process.</span></span> <span data-ttu-id="21637-106">La información de depuración puede incluir llamadas API realizadas, llamadas a funciones internas realizadas y transiciones de estado realizadas.</span><span class="sxs-lookup"><span data-stu-id="21637-106">The debugging information can include API calls performed, internal function calls performed, and state transitions performed.</span></span>

<span data-ttu-id="21637-107">El seguimiento se puede habilitar tanto en el lado cliente como en el lado autenticador.</span><span class="sxs-lookup"><span data-stu-id="21637-107">Tracing can be enabled on both the client side and the authenticator side.</span></span> <span data-ttu-id="21637-108">También se puede habilitar el seguimiento para las llamadas a las API del [servicio de enrutamiento y acceso remoto (RRAS)](/windows/desktop/RRAS/routing-start-page) .</span><span class="sxs-lookup"><span data-stu-id="21637-108">Tracing can also be enabled for calls to the [Routing and Remote Access Service (RRAS)](/windows/desktop/RRAS/routing-start-page) APIs.</span></span> <span data-ttu-id="21637-109">Para obtener más información, vea [seguimiento en el servicio de enrutamiento y acceso remoto](#tracing-on-the-routing-and-remote-access-service).</span><span class="sxs-lookup"><span data-stu-id="21637-109">For more information, see [Tracing on the Routing and Remote Access Service](#tracing-on-the-routing-and-remote-access-service).</span></span>

> [!Note]  
> <span data-ttu-id="21637-110">Los registros de seguimiento solo están disponibles en inglés.</span><span class="sxs-lookup"><span data-stu-id="21637-110">Trace logs are available in English only.</span></span>

 

<span data-ttu-id="21637-111">Cuando el seguimiento de EAPHost está habilitado, la información de registro se almacena en un archivo. ETL en una ubicación especificada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="21637-111">When EAPHost tracing is enabled, logging information is stored in an .etl file in a user-specified location.</span></span> <span data-ttu-id="21637-112">Si se producen errores durante la autenticación de EAP, el seguimiento genera un archivo. ETL que se puede enviar a Microsoft soporte técnico Developer para el análisis de la causa raíz.</span><span class="sxs-lookup"><span data-stu-id="21637-112">If errors occur during EAP authentication, tracing generates an .etl file that can be sent to Microsoft Developer Support for root cause analysis.</span></span> <span data-ttu-id="21637-113">Los asociados que tienen acceso a recursos compartidos de compilación de Microsoft Windows, símbolos y archivos traceformat pueden convertir los archivos. ETL en un archivo de texto sin formato mediante la herramienta **tracerpt** .</span><span class="sxs-lookup"><span data-stu-id="21637-113">Partners that have access to Microsoft windows build shares, symbols, and traceformat files can convert the .etl files into a plain text file using the **tracerpt** tool.</span></span>

<span data-ttu-id="21637-114">Los errores del servidor de directivas de redes (NPS) no se capturan en los registros de EAPHost.</span><span class="sxs-lookup"><span data-stu-id="21637-114">Network policy server (NPS) failures are not captured in the EAPHost logs.</span></span> <span data-ttu-id="21637-115">Si está intentando solucionar un error de NPS, vea el IASSAM. LOG y [IASNAP. ](https://go.microsoft.com/fwlink/p/?linkid=84108) Archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="21637-115">If you are trying to troubleshoot a NPS failure, view the IASSAM.LOG and [IASNAP.LOG](https://go.microsoft.com/fwlink/p/?linkid=84108) files.</span></span>

## <a name="tracing-on-the-client"></a><span data-ttu-id="21637-116">Seguimiento en el cliente</span><span class="sxs-lookup"><span data-stu-id="21637-116">Tracing on the Client</span></span>

<span data-ttu-id="21637-117">Para habilitar el seguimiento en el lado cliente:</span><span class="sxs-lookup"><span data-stu-id="21637-117">To enable tracing on the client side:</span></span>

1.  <span data-ttu-id="21637-118">Abra una ventana del símbolo del sistema con permisos elevados.</span><span class="sxs-lookup"><span data-stu-id="21637-118">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="21637-119">Ejecute el siguiente comando: **Logman** **Start Trace** **EapHostPeer** **-o** **. \\ EapHostPeer. ETL** **-p** **{5F31090B-D990-4e91-B16D-46121D0255AA} 0x4000ffff 0** **-ETS**</span><span class="sxs-lookup"><span data-stu-id="21637-119">Run the following command: **logman** **start trace** **EapHostPeer** **-o** **.\\EapHostPeer.etl** **-p** **{5F31090B-D990-4e91-B16D-46121D0255AA} 0x4000ffff 0** **-ets**</span></span>
3.  <span data-ttu-id="21637-120">Reproduzca el escenario del que desea realizar un seguimiento.</span><span class="sxs-lookup"><span data-stu-id="21637-120">Reproduce the scenario that you want to trace.</span></span>
4.  <span data-ttu-id="21637-121">Ejecute el siguiente comando: **Logman** **Stop** **EapHostPeer** **-ETS**</span><span class="sxs-lookup"><span data-stu-id="21637-121">Run the following command: **logman** **stop** **EapHostPeer** **-ets**</span></span>
5.  <span data-ttu-id="21637-122">Convierta el archivo ETL en texto con el siguiente comando **: tracerpt EapHostPeer. ETL** **– PDB** **&lt; &gt; pdbpath** **-TP** **&lt; tracemessagefilesdirectorypath &gt;** **-o** **EapHostPeer.txt**</span><span class="sxs-lookup"><span data-stu-id="21637-122">Convert the etl file into text using the following command: **tracerpt EapHostPeer.etl** **–pdb** **&lt;pdbpath&gt;** **-tp** **&lt;tracemessagefilesdirectorypath&gt;** **-o** **EapHostPeer.txt**</span></span>
    > [!Note]  
    > <span data-ttu-id="21637-123">Si no tiene acceso a la herramienta tracerpt, evite el último paso y envíe el archivo. ETL a Microsoft soporte técnico Developer.</span><span class="sxs-lookup"><span data-stu-id="21637-123">If you do not have access to the tracerpt tool, avoid the last step and send the .etl file to Microsoft Developer Support.</span></span>

     

## <a name="tracing-on-the-authenticator"></a><span data-ttu-id="21637-124">Seguimiento en el autenticador</span><span class="sxs-lookup"><span data-stu-id="21637-124">Tracing on the Authenticator</span></span>

<span data-ttu-id="21637-125">Para habilitar el seguimiento en el lado del autenticador:</span><span class="sxs-lookup"><span data-stu-id="21637-125">To enable tracing on the authenticator side:</span></span>

1.  <span data-ttu-id="21637-126">Abra una ventana del símbolo del sistema con permisos elevados.</span><span class="sxs-lookup"><span data-stu-id="21637-126">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="21637-127">Ejecute el siguiente comando: **Logman** **Start Trace** **EapHostAuthr** **-o** **. \\ EapHostAuthr. ETL** **-p** **{F6578502-DF4E-4a67-9661-E3A2F05D1D9B} 0x4000ffff 0** **-ETS**</span><span class="sxs-lookup"><span data-stu-id="21637-127">Run the following command: **logman** **start trace** **EapHostAuthr** **-o** **.\\EapHostAuthr.etl** **-p** **{F6578502-DF4E-4a67-9661-E3A2F05D1D9B} 0x4000ffff 0** **-ets**</span></span>
3.  <span data-ttu-id="21637-128">Reproduzca el escenario del que desea realizar un seguimiento.</span><span class="sxs-lookup"><span data-stu-id="21637-128">Reproduce the scenario that you want to trace.</span></span>
4.  <span data-ttu-id="21637-129">Ejecute el siguiente comando: **Logman** **Stop** **EapHostAuthr** **-ETS**</span><span class="sxs-lookup"><span data-stu-id="21637-129">Run the following command: **logman** **stop** **EapHostAuthr** **-ets**</span></span>
5.  <span data-ttu-id="21637-130">Convierta el archivo ETL en texto con el siguiente comando **: tracerpt EapHostAuthr. ETL** **– PDB** **&lt; &gt; pdbpath** **-TP** **&lt; tracemessagefilesdirectorypath &gt;** **-o** **EapHostAuthr.txt**</span><span class="sxs-lookup"><span data-stu-id="21637-130">Convert the etl file into text using the following command: **tracerpt EapHostAuthr.etl** **–pdb** **&lt;pdbpath&gt;** **-tp** **&lt;tracemessagefilesdirectorypath&gt;** **-o** **EapHostAuthr.txt**</span></span>
    > [!Note]  
    > <span data-ttu-id="21637-131">Si no tiene acceso a la herramienta tracerpt, evite el último paso y, en su lugar, envíe el archivo. ETL a Microsoft soporte técnico Developer.</span><span class="sxs-lookup"><span data-stu-id="21637-131">If you do not have access to the tracerpt tool, avoid the last step and instead send the .etl file to Microsoft Developer Support.</span></span>

     

## <a name="event-tracing"></a><span data-ttu-id="21637-132">Seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="21637-132">Event tracing</span></span>

<span data-ttu-id="21637-133">En Windows 7 y versiones posteriores de Windows, EapHost proporciona seguimiento basado en eventos en el autenticador y en el mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="21637-133">In Windows 7 and later versions of Windows, EapHost provides event based tracing on the authenticator and the peer.</span></span> <span data-ttu-id="21637-134">La ventaja del seguimiento basado en eventos es que no se necesitan archivos de símbolos para ver los mensajes de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="21637-134">The advantage of event based tracing is that no symbol files are needed to view the trace messages.</span></span> <span data-ttu-id="21637-135">Para habilitar el seguimiento de eventos:</span><span class="sxs-lookup"><span data-stu-id="21637-135">To enable event tracing:</span></span>

1.  <span data-ttu-id="21637-136">Abra **EventViewer**.</span><span class="sxs-lookup"><span data-stu-id="21637-136">Open **EventViewer**.</span></span>
2.  <span data-ttu-id="21637-137">Los mensajes críticos de EapHost se registran en: "Custom views \\ Administrative Events"</span><span class="sxs-lookup"><span data-stu-id="21637-137">Critical EapHost messages are logged under: “Custom Views\\Administrative Events”</span></span>
3.  <span data-ttu-id="21637-138">Los mensajes no críticos se registran en: "aplicaciones y servicios \\ Microsoft \\ Windows \\ EAPHost</span><span class="sxs-lookup"><span data-stu-id="21637-138">Non-critical messages are logged under: “Applications and Services\\Microsoft\\Windows\\EapHost</span></span>
4.  <span data-ttu-id="21637-139">Los mensajes de eventos de tipo "análisis" y "depuración" se pueden ver en la misma ruta de acceso; para ello, seleccione **Mostrar registros analíticos y de depuración** en el menú **Ver** de la barra de título.</span><span class="sxs-lookup"><span data-stu-id="21637-139">"Analytic" and "Debug" type event messages can be seen under the same path by selecting **Show Analytic and Debug Logs** from the **view** menu in the title bar.</span></span>

## <a name="tracing-on-the-routing-and-remote-access-service"></a><span data-ttu-id="21637-140">Seguimiento en el servicio de enrutamiento y acceso remoto</span><span class="sxs-lookup"><span data-stu-id="21637-140">Tracing on the Routing and Remote Access Service</span></span>

<span data-ttu-id="21637-141">Para habilitar el seguimiento de RRAS:</span><span class="sxs-lookup"><span data-stu-id="21637-141">To enable RRAS tracing:</span></span>

1.  <span data-ttu-id="21637-142">Abra una ventana del símbolo del sistema con permisos elevados.</span><span class="sxs-lookup"><span data-stu-id="21637-142">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="21637-143">Ejecute el siguiente comando: **netsh** **ras** **set** **TR** **\* *_ _* en**</span><span class="sxs-lookup"><span data-stu-id="21637-143">Run the following command: **netsh** **ras** **set** **tr** **\**_ _\* en*\*</span></span>
3.  <span data-ttu-id="21637-144">Abrir el **\\ seguimiento de% SystemRoot%** para ver los SEGUIMIENTOs de Ras</span><span class="sxs-lookup"><span data-stu-id="21637-144">Open **%systemroot%\\tracing** to view RAS traces</span></span>

<span data-ttu-id="21637-145">Para deshabilitar el seguimiento de RRAS:</span><span class="sxs-lookup"><span data-stu-id="21637-145">To disable RRAS tracing:</span></span>

1.  <span data-ttu-id="21637-146">Abra una ventana del símbolo del sistema con permisos elevados.</span><span class="sxs-lookup"><span data-stu-id="21637-146">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="21637-147">Ejecute el siguiente comando: **netsh** **ras** **set** **TR** **\* *_ _* dis**</span><span class="sxs-lookup"><span data-stu-id="21637-147">Run the following command: **netsh** **ras** **set** **tr** **\**_ _\* dis*\*</span></span>

<span data-ttu-id="21637-148">Para obtener más información, vea [comandos Netsh](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="21637-148">For more information, see [Netsh Commands](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="21637-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="21637-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21637-150">Uso de EAPHost</span><span class="sxs-lookup"><span data-stu-id="21637-150">Using EAPHost</span></span>](using-eap-host.md)
</dt> <dt>

[<span data-ttu-id="21637-151">Servicio de enrutamiento y acceso remoto (RRAS)</span><span class="sxs-lookup"><span data-stu-id="21637-151">Routing and Remote Access Service (RRAS)</span></span>](/windows/desktop/RRAS/routing-start-page)
</dt> </dl>

 

 