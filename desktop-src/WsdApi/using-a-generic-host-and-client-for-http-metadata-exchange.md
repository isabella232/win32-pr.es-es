---
description: Si el cliente y el host no pueden intercambiar metadatos, un host y un cliente genéricos se pueden sustituir por el host personalizado y el cliente para ayudar a solucionar el problema.
ms.assetid: 7e5c8444-b3ee-4e9c-984f-13d54f2bbfc0
title: Usar un host y un cliente genéricos para el intercambio de metadatos HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36827dde8aa03fa15fc4beaa5917f1f2c3c36eca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705877"
---
# <a name="using-a-generic-host-and-client-for-http-metadata-exchange"></a><span data-ttu-id="6bf98-103">Usar un host y un cliente genéricos para el intercambio de metadatos HTTP</span><span class="sxs-lookup"><span data-stu-id="6bf98-103">Using a Generic Host and Client for HTTP Metadata Exchange</span></span>

<span data-ttu-id="6bf98-104">Si el cliente y el host no pueden intercambiar metadatos, un host y un cliente genéricos se pueden sustituir por el host personalizado y el cliente para ayudar a solucionar el problema.</span><span class="sxs-lookup"><span data-stu-id="6bf98-104">If the client and host cannot exchange metadata, then a generic host and client can be substituted for the custom host and client to help troubleshoot the issue.</span></span> <span data-ttu-id="6bf98-105">Si la dirección del dispositivo o los metadatos del dispositivo no aparecen en la salida del cliente de depuración de WSD, las direcciones de transporte proporcionadas o el entorno de red pueden estar causando el error.</span><span class="sxs-lookup"><span data-stu-id="6bf98-105">If the device address or device metadata does not appear in the WSD Debug Client output, then the supplied transport addresses or the network environment may be causing the failure.</span></span> <span data-ttu-id="6bf98-106">Para obtener más información sobre el host y el cliente genéricos, vea [herramientas de depuración](debugging-tools.md).</span><span class="sxs-lookup"><span data-stu-id="6bf98-106">For more information about the generic host and client, see [Debugging Tools](debugging-tools.md).</span></span>

<span data-ttu-id="6bf98-107">Si se ha comprobado que un host y un cliente genéricos pueden completar el intercambio de metadatos de WS-Discovery y HTTP, se puede omitir este procedimiento de diagnóstico y se puede continuar con la solución de problemas siguiendo los procedimientos que se describen en [uso del registro de WinHTTP para comprobar el tráfico de obtención](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="6bf98-107">If it has been verified that a generic host and client can complete both WS-Discovery and HTTP metadata exchange, then this diagnostic procedure can be skipped and troubleshooting can be continued by following the procedures in [Using WinHTTP Logging to Verify Get Traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>

<span data-ttu-id="6bf98-108">Si el host o el cliente es una aplicación que se ejecuta en un equipo, el host o el cliente genéricos deben ejecutarse en el mismo contexto de seguridad que el host o cliente real.</span><span class="sxs-lookup"><span data-stu-id="6bf98-108">If either the host or client is an application running on a PC, the generic host or client should be run in the same security context as the actual host or client.</span></span> <span data-ttu-id="6bf98-109">Por ejemplo, si el host o cliente real se ejecuta como administrador, el host o el cliente genéricos se deben ejecutar como administrador.</span><span class="sxs-lookup"><span data-stu-id="6bf98-109">For example, if the actual host or client runs as Administrator, then the generic host or client must run as Administrator.</span></span> <span data-ttu-id="6bf98-110">Además, si el host o el cliente es un dispositivo independiente, debe reemplazarse por completo por un equipo que ejecute un host o un cliente genéricos en un contexto de seguridad que garantice un acceso ilimitado a la red (por ejemplo, en ejecución como administrador).</span><span class="sxs-lookup"><span data-stu-id="6bf98-110">Also, if either the host or client is a standalone device, it should be completely replaced by a PC running a generic host or client in a security context that guarantees unlimited network access (for example, running as Administrator).</span></span>

<span data-ttu-id="6bf98-111">**Para usar un host y un cliente genéricos para solucionar problemas de intercambio de metadatos HTTP**</span><span class="sxs-lookup"><span data-stu-id="6bf98-111">**To using a generic host and client to troubleshoot HTTP metadata exchange**</span></span>

1.  <span data-ttu-id="6bf98-112">Abra una ventana de símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="6bf98-112">Open a command prompt window.</span></span>
2.  <span data-ttu-id="6bf98-113">Ejecute el comando siguiente: **WSDDebug \_host.exe/Mode Metadata/Start**</span><span class="sxs-lookup"><span data-stu-id="6bf98-113">Run the following command: **WSDDebug\_host.exe /mode metadata /start**</span></span>

    > [!Note]  
    > <span data-ttu-id="6bf98-114">Puede aparecer un cuadro de diálogo **alerta de seguridad de Windows** .</span><span class="sxs-lookup"><span data-stu-id="6bf98-114">A **Windows Security Alert** dialog box may appear.</span></span> <span data-ttu-id="6bf98-115">Si es así, haga clic en **desbloquear** para permitir la ejecución del host de depuración de WSD.</span><span class="sxs-lookup"><span data-stu-id="6bf98-115">If so, click **Unblock** to allow the WSD Debug Host to run.</span></span>

     

    <span data-ttu-id="6bf98-116">Este comando genera un resultado similar al siguiente.</span><span class="sxs-lookup"><span data-stu-id="6bf98-116">This command generates output similar to the following.</span></span> <span data-ttu-id="6bf98-117">Anote el identificador del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6bf98-117">Make a note of the device ID.</span></span>

    ``` syntax
    WSDAPI Debug Host
    Copyright (C) Microsoft Corporation 2007.  All rights reserved.
    Device ID is urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    Host metadata>
    ```

3.  <span data-ttu-id="6bf98-118">Ejecute el siguiente comando: **WSDDebug \_client.exe/Mode Metadata/Hello OFF/Resolve** *<id>* .</span><span class="sxs-lookup"><span data-stu-id="6bf98-118">Run the following command: **WSDDebug\_client.exe /mode metadata /hello off /resolve** *<id>*.</span></span> <span data-ttu-id="6bf98-119">Reemplace *<id>* por el identificador de dispositivo identificado en el paso 2.</span><span class="sxs-lookup"><span data-stu-id="6bf98-119">Replace *<id>* with the device ID identified in step 2.</span></span>
    > [!Note]  
    > <span data-ttu-id="6bf98-120">Puede aparecer un cuadro de diálogo **alerta de seguridad de Windows** .</span><span class="sxs-lookup"><span data-stu-id="6bf98-120">A **Windows Security Alert** dialog box may appear.</span></span> <span data-ttu-id="6bf98-121">Si es así, haga clic en **desbloquear** para permitir que se ejecute el cliente de depuración de WSD.</span><span class="sxs-lookup"><span data-stu-id="6bf98-121">If so, click **Unblock** to allow the WSD Debug Client to run.</span></span>

     

<span data-ttu-id="6bf98-122">El cliente de depuración de WSD genera una salida similar a la siguiente.</span><span class="sxs-lookup"><span data-stu-id="6bf98-122">WSD Debug Client generates output similar to the following.</span></span>

``` syntax
WSDAPI Debug Client
Copyright (C) Microsoft Corporation 2007.  All rights reserved.
Client ID is urn:uuid:0f571af7-6b0e-4daf-8054-f2233ac27910
Hello mode is disabled
Client metadata>
*****************************************************************************
Add at 02/28/07 15:16:51
+ EPR:
  + Address:                 urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
+ Types:
    (wsdp) https://schemas.xmlsoap.org/ws/2006/02/devprof:Device
+ XAddrs:
  https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
+ Metadata version:          2
+ Instance ID:               1
+ Probe/Resolve tag:         WSDAPI debug_client
+ Remote transport address:  [::1]:3702
+ Local transport address:   ::1
+ Local interface GUID:      42133cd4-6a70-11db-bbc9-806e6f6e6963
Client metadata>
*****************************************************************************
Getting metadata for host at 02/28/07 15:16:51:
+ Endpoint reference:
  + Address:
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
Using xAddr: https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
Client metadata>
*****************************************************************************
Metadata for host:
+ Endpoint reference:
  + Address:           urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
Metadata section:
  + Dialect:
    https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisDevice
  + Friendly name:
    [no lang]: Debugging Host
  + Firmware version:  1.0
  + Serial number:     00000000
Metadata section:
  + Dialect:
    https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisModel
  + Manufacturer:
    [no lang]: Microsoft Corporation
  + Manufacturer URL:  https://www.microsoft.com/
  + Model names:
    [no lang]: Microsoft Debugging Host
  + Model number:      https://www.microsoft.com/
End of metadata
Client metadata>
```

<span data-ttu-id="6bf98-123">El cliente de depuración de WSD puede generar una gran cantidad de resultados en una red con muchos dispositivos DPWS.</span><span class="sxs-lookup"><span data-stu-id="6bf98-123">The WSD Debug Client may generate a lot of output on a network with many DPWS devices.</span></span> <span data-ttu-id="6bf98-124">La salida se puede redirigir a un archivo para un análisis más sencillo.</span><span class="sxs-lookup"><span data-stu-id="6bf98-124">The output can be redirected to a file for easier analysis.</span></span> <span data-ttu-id="6bf98-125">Escriba **log Tee** *<filename>* en el mensaje del cliente de depuración WSD para redirigir la salida a un archivo.</span><span class="sxs-lookup"><span data-stu-id="6bf98-125">Type **log tee** *<filename>* at the WSD Debug Client prompt to redirect output to a file.</span></span> <span data-ttu-id="6bf98-126">La redirección de salida se puede detener escribiendo **log Tee STOP** en el símbolo del sistema de depuración WSD.</span><span class="sxs-lookup"><span data-stu-id="6bf98-126">Output redirection can be stopped by typing **log tee stop** at the WSD Debug Client prompt.</span></span>

<span data-ttu-id="6bf98-127">Tome nota de la dirección de referencia de extremo (EPR).</span><span class="sxs-lookup"><span data-stu-id="6bf98-127">Make a note of the endpoint reference (EPR) address.</span></span> <span data-ttu-id="6bf98-128">Esta dirección de EPR debe coincidir con el identificador de dispositivo identificado en el paso 2 anterior.</span><span class="sxs-lookup"><span data-stu-id="6bf98-128">This EPR address should match the device ID identified in step 2 above.</span></span> <span data-ttu-id="6bf98-129">Además, compruebe que el cliente de depuración de WSD imprimió por completo los metadatos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6bf98-129">Also, verify that the WSD Debug Client completely printed the metadata for the device.</span></span> <span data-ttu-id="6bf98-130">Los metadatos del dispositivo comienzan por `Metadata for host` y terminan con `End of metadata` .</span><span class="sxs-lookup"><span data-stu-id="6bf98-130">The device metadata begins with `Metadata for host` and ends with `End of metadata`.</span></span>

<span data-ttu-id="6bf98-131">Si el identificador de dispositivo y los metadatos del dispositivo aparecen correctamente en la salida del cliente de depuración de WSD, es probable que el error de aplicación no esté relacionado con las direcciones de transporte proporcionadas, el sistema operativo o el entorno de red.</span><span class="sxs-lookup"><span data-stu-id="6bf98-131">If the device ID and device metadata appears correctly in the WSD Debug Client output, then the application failure is likely not related to the supplied transport addresses, the operating system, or the network environment.</span></span> <span data-ttu-id="6bf98-132">Reemplace el host y el cliente genéricos con el cliente y el host personalizados y siga los procedimientos que se indican en [uso del registro de WinHTTP para comprobar el tráfico](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="6bf98-132">Replace the generic host and client with the custom host and client, and continue troubleshooting by following the procedures in [Using WinHTTP Logging to Verify Get Traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>

<span data-ttu-id="6bf98-133">Si la dirección del dispositivo y los metadatos del dispositivo no aparecen en la salida del cliente de depuración de WSD, el error podría tener una o varias de las causas siguientes:</span><span class="sxs-lookup"><span data-stu-id="6bf98-133">If the device address and device metadata do not appear in the WSD Debug Client output, then the failure could have one or more of the following causes:</span></span>

-   <span data-ttu-id="6bf98-134">La dirección de transporte anunciada por el host es incorrecta o tiene un formato incorrecto.</span><span class="sxs-lookup"><span data-stu-id="6bf98-134">The transport address advertised by the host is incorrect or malformed.</span></span> <span data-ttu-id="6bf98-135">El cliente de depuración de WSD intenta obtener los metadatos del dispositivo de la dirección URL proporcionada en el elemento **XAddrs** de un mensaje [ProbeMatches](probematches-message.md) o [ResolveMatches](resolvematches-message.md) .</span><span class="sxs-lookup"><span data-stu-id="6bf98-135">WSD Debug Client attempts to get device metadata from the URL provided in the **XAddrs** element of a [ProbeMatches](probematches-message.md) or [ResolveMatches](resolvematches-message.md) message.</span></span> <span data-ttu-id="6bf98-136">La dirección URL usada para el intercambio de metadatos aparece en la salida del cliente de depuración WSD, precedida por la frase `Using xAddr` .</span><span class="sxs-lookup"><span data-stu-id="6bf98-136">The URL used for metadata exchange appears in the WSD Debug Client output, prefixed by the phrase `Using xAddr`.</span></span> <span data-ttu-id="6bf98-137">En el ejemplo siguiente se muestra el XAddrs que se usa para el intercambio de metadatos en la salida del cliente de depuración WSD anterior.</span><span class="sxs-lookup"><span data-stu-id="6bf98-137">The following example shows the XAddrs used for metadata exchange in the above WSD Debug Client output.</span></span>

    ``` syntax
    Using xAddr: https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
    ```

    <span data-ttu-id="6bf98-138">Si el XAddrs proporcionado no se ajusta a las [reglas de validación de XAddr](xaddr-validation-rules.md), el cliente de depuración de WSD no puede obtener los metadatos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6bf98-138">If the supplied XAddrs do not conform to the [XAddr validation rules](xaddr-validation-rules.md), then the WSD Debug Client cannot get the device's metadata.</span></span>

-   <span data-ttu-id="6bf98-139">La aplicación se está ejecutando en un contexto de seguridad incorrecto.</span><span class="sxs-lookup"><span data-stu-id="6bf98-139">The application is running in the wrong security context.</span></span> <span data-ttu-id="6bf98-140">Compruebe que la aplicación está usando las credenciales correctas y que el cliente y el host tienen permisos suficientes para tener acceso a la red.</span><span class="sxs-lookup"><span data-stu-id="6bf98-140">Verify that the application is using the correct credentials and that the client and host have sufficient permission to access the network.</span></span>
-   <span data-ttu-id="6bf98-141">La configuración del Firewall es incorrecta.</span><span class="sxs-lookup"><span data-stu-id="6bf98-141">The firewall configuration is wrong.</span></span> <span data-ttu-id="6bf98-142">Siga las instrucciones de [inspección de la configuración del adaptador y del firewall](inspecting-adapter-and-firewall-settings.md) para comprobar que la configuración del firewall de Windows sea correcta y que no haya otras reglas que quiten los paquetes.</span><span class="sxs-lookup"><span data-stu-id="6bf98-142">Follow the instructions in [Inspecting Adapter and Firewall Settings](inspecting-adapter-and-firewall-settings.md) to verify that the Windows Firewall settings are correct and that there are no other rules dropping the packets.</span></span> <span data-ttu-id="6bf98-143">El cliente y el host también se pueden copiar en un equipo "original" (uno con una instalación de sistema operativo predeterminada que nunca se ha unido a un dominio) para intentar reproducir el error.</span><span class="sxs-lookup"><span data-stu-id="6bf98-143">The client and host can also be copied onto a "pristine" machine (one with a default operating system installation that has never been joined to a domain) in order to attempt to reproduce the failure.</span></span>
-   <span data-ttu-id="6bf98-144">Una directiva IPSec está bloqueando la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6bf98-144">An IPSec policy is blocking the application.</span></span> <span data-ttu-id="6bf98-145">Copie el cliente y el host en un equipo que no esté sujeto a directivas IPSec y trate de reproducir el error.</span><span class="sxs-lookup"><span data-stu-id="6bf98-145">Copy the client and host onto a machine that is not subject to IPSec policies and try to reproduce the failure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6bf98-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6bf98-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bf98-147">Procedimientos de diagnóstico de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="6bf98-147">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="6bf98-148">Introducción con la solución de problemas de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="6bf98-148">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



