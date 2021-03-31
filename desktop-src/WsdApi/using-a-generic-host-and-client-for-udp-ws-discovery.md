---
description: Si el cliente y el host no se pueden ver entre sí en la red, un host y un cliente genéricos se pueden sustituir por el host personalizado y el cliente para ayudar a solucionar el problema.
ms.assetid: e82ce911-b2a7-4a57-a2f0-9aca6b74478f
title: Usar un host y un cliente genéricos para WS-Discovery UDP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3289f5205e4e417fe8162b401be6c608432cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275784"
---
# <a name="using-a-generic-host-and-client-for-udp-ws-discovery"></a><span data-ttu-id="6fcd5-103">Usar un host y un cliente genéricos para WS-Discovery UDP</span><span class="sxs-lookup"><span data-stu-id="6fcd5-103">Using a Generic Host and Client for UDP WS-Discovery</span></span>

<span data-ttu-id="6fcd5-104">Si el cliente y el host no se pueden ver entre sí en la red, un host y un cliente genéricos se pueden sustituir por el host personalizado y el cliente para ayudar a solucionar el problema.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-104">If the client and host cannot see each other on the network, then a generic host and client can be substituted for the custom host and client to help troubleshoot the issue.</span></span> <span data-ttu-id="6fcd5-105">Si la dirección del dispositivo no aparece en la salida del cliente de depuración de WSD, es probable que el entorno de red esté causando el error.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-105">If the device address does not appear in the WSD Debug Client output, then the network environment is probably causing the failure.</span></span> <span data-ttu-id="6fcd5-106">Para obtener más información sobre el host y el cliente genéricos, vea [herramientas de depuración](debugging-tools.md).</span><span class="sxs-lookup"><span data-stu-id="6fcd5-106">For more information about the generic host and client, see [Debugging Tools](debugging-tools.md).</span></span>

<span data-ttu-id="6fcd5-107">Si el host o el cliente es una aplicación que se ejecuta en un equipo, el host o el cliente genéricos deben ejecutarse en el mismo contexto de seguridad que el host o cliente real.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-107">If either the host or client is an application running on a PC, the generic host or client should be run in the same security context as the actual host or client.</span></span> <span data-ttu-id="6fcd5-108">Por ejemplo, si el host o cliente real se ejecuta como administrador, el host o el cliente genéricos se deben ejecutar como administrador.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-108">For example, if the actual host or client runs as Administrator, then the generic host or client must run as Administrator.</span></span> <span data-ttu-id="6fcd5-109">Además, si el host o el cliente es un dispositivo independiente, debe reemplazarse por completo con un equipo que ejecute un host o un cliente genéricos.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-109">Also, if either the host or client is a standalone device, it should be completely replaced by a PC running a generic host or client.</span></span>

<span data-ttu-id="6fcd5-110">**Para usar un host y un cliente genéricos para solucionar problemas de WS-Discovery de UDP**</span><span class="sxs-lookup"><span data-stu-id="6fcd5-110">**To using a generic host and client to troubleshoot UDP WS-Discovery**</span></span>

1.  <span data-ttu-id="6fcd5-111">Abra una ventana de símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-111">Open a command prompt window.</span></span>
2.  <span data-ttu-id="6fcd5-112">Ejecute el comando siguiente: **WSDDebug \_host.exe/Mode Metadata/Start**</span><span class="sxs-lookup"><span data-stu-id="6fcd5-112">Run the following command: **WSDDebug\_host.exe /mode metadata /start**</span></span>

    > [!Note]  
    > <span data-ttu-id="6fcd5-113">Puede aparecer un cuadro de diálogo **alerta de seguridad de Windows** .</span><span class="sxs-lookup"><span data-stu-id="6fcd5-113">A **Windows Security Alert** dialog box may appear.</span></span> <span data-ttu-id="6fcd5-114">Si es así, haga clic en **desbloquear** para permitir la ejecución del host de depuración de WSD.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-114">If so, click **Unblock** to allow the WSD Debug Host to run.</span></span>

     

    <span data-ttu-id="6fcd5-115">Este comando genera un resultado similar al siguiente.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-115">This command generates output similar to the following.</span></span> <span data-ttu-id="6fcd5-116">Anote el identificador del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-116">Make a note of the device ID.</span></span>

    ``` syntax
    WSDAPI Debug Host
    Copyright (C) Microsoft Corporation 2007.  All rights reserved.
    Device ID is urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    Host metadata>
    ```

3.  <span data-ttu-id="6fcd5-117">Ejecute el siguiente comando: **WSDDebug \_client.exe/Mode Metadata/Hello OFF/Resolve** *<id>* .</span><span class="sxs-lookup"><span data-stu-id="6fcd5-117">Run the following command: **WSDDebug\_client.exe /mode metadata /hello off /resolve** *<id>*.</span></span> <span data-ttu-id="6fcd5-118">Reemplace *<id>* por el identificador de dispositivo identificado en el paso 2.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-118">Replace *<id>* with the device ID identified in step 2.</span></span>
    > [!Note]  
    > <span data-ttu-id="6fcd5-119">Puede aparecer un cuadro de diálogo **alerta de seguridad de Windows** .</span><span class="sxs-lookup"><span data-stu-id="6fcd5-119">A **Windows Security Alert** dialog box may appear.</span></span> <span data-ttu-id="6fcd5-120">Si es así, haga clic en **desbloquear** para permitir que se ejecute el cliente de depuración de WSD.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-120">If so, click **Unblock** to allow the WSD Debug Client to run.</span></span>

     

<span data-ttu-id="6fcd5-121">El cliente de depuración de WSD genera una salida similar a la siguiente.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-121">WSD Debug Client generates output similar to the following.</span></span>

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
```

<span data-ttu-id="6fcd5-122">El cliente de depuración de WSD puede generar una gran cantidad de resultados en una red con muchos dispositivos DPWS.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-122">The WSD Debug Client may generate a lot of output on a network with many DPWS devices.</span></span> <span data-ttu-id="6fcd5-123">La salida se puede redirigir a un archivo para un análisis más sencillo.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-123">The output can be redirected to a file for easier analysis.</span></span> <span data-ttu-id="6fcd5-124">Escriba **log Tee** *<filename>* en el mensaje del cliente de depuración WSD para redirigir la salida a un archivo.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-124">Type **log tee** *<filename>* at the WSD Debug Client prompt to redirect output to a file.</span></span> <span data-ttu-id="6fcd5-125">La redirección de salida se puede detener escribiendo **log Tee STOP** en el símbolo del sistema de depuración WSD.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-125">Output redirection can be stopped by typing **log tee stop** at the WSD Debug Client prompt.</span></span>

<span data-ttu-id="6fcd5-126">Tome nota de la dirección de referencia de extremo (EPR).</span><span class="sxs-lookup"><span data-stu-id="6fcd5-126">Make a note of the endpoint reference (EPR) address.</span></span> <span data-ttu-id="6fcd5-127">Esta dirección de EPR debe coincidir con el identificador de dispositivo identificado en el paso 2 anterior.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-127">This EPR address should match the device ID identified in step 2 above.</span></span> <span data-ttu-id="6fcd5-128">En este caso, es probable que el error de aplicación no esté relacionado con el sistema operativo o con el entorno de red.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-128">If this is the case, then the application failure is likely not related to the operating system or the network environment.</span></span> <span data-ttu-id="6fcd5-129">Reemplace el host y el cliente genéricos con el cliente y el host personalizados y siga los procedimientos que se describen en [uso del cliente de depuración WSD para comprobar el tráfico de multidifusión para](using-wsddebug-client-to-verify-multicast-traffic.md)continuar con la solución de problemas.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-129">Replace the generic host and client with the custom host and client, and continue troubleshooting by following the procedures in [Using WSD Debug Client to Verify Multicast Traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>

<span data-ttu-id="6fcd5-130">Si el ID. de dispositivo no coincide con la dirección EPR, es probable que el error de aplicación esté relacionado con el sistema operativo o con el entorno de red.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-130">If the device ID does not match the EPR address, then the application failure is probably related to the operating system or the network environment.</span></span> <span data-ttu-id="6fcd5-131">El error podría tener una o varias de las causas siguientes:</span><span class="sxs-lookup"><span data-stu-id="6fcd5-131">The failure could have one or more of the following causes:</span></span>

-   <span data-ttu-id="6fcd5-132">La aplicación se está ejecutando en un contexto de seguridad incorrecto.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-132">The application is running in the wrong security context.</span></span> <span data-ttu-id="6fcd5-133">Compruebe que la aplicación está usando las credenciales correctas y que el cliente y el host tienen permisos suficientes para tener acceso a la red.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-133">Verify that the application is using the correct credentials and that the client and host have sufficient permission to access the network.</span></span>
-   <span data-ttu-id="6fcd5-134">La configuración del Firewall es incorrecta.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-134">The firewall configuration is wrong.</span></span> <span data-ttu-id="6fcd5-135">Siga las instrucciones de [inspección de la configuración del adaptador y del firewall](inspecting-adapter-and-firewall-settings.md) para comprobar que la configuración del firewall de Windows sea correcta y que no haya otras reglas que quiten los paquetes.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-135">Follow the instructions in [Inspecting Adapter and Firewall Settings](inspecting-adapter-and-firewall-settings.md) to verify that the Windows Firewall settings are correct and that there are no other rules dropping the packets.</span></span> <span data-ttu-id="6fcd5-136">El cliente y el host también se pueden copiar en un equipo "original" (uno con una instalación de sistema operativo predeterminada que nunca se ha unido a un dominio) para intentar reproducir el error.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-136">The client and host can also be copied onto a "pristine" machine (one with a default operating system installation that has never been joined to a domain) in order to attempt to reproduce the failure.</span></span>
-   <span data-ttu-id="6fcd5-137">Una directiva IPSec está bloqueando la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-137">An IPSec policy is blocking the application.</span></span> <span data-ttu-id="6fcd5-138">Copie el cliente y el host en un equipo que no esté sujeto a directivas IPSec y trate de reproducir el error.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-138">Copy the client and host onto a machine not subject to IPSec policies and try to reproduce the failure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6fcd5-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6fcd5-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fcd5-140">Procedimientos de diagnóstico de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="6fcd5-140">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="6fcd5-141">Introducción con la solución de problemas de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="6fcd5-141">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



