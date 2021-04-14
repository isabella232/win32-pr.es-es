---
title: SSL de modo kernel
description: SSL de modo kernel
ms.assetid: ada82704-cb7d-4e98-8c87-76c7bfbd098b
keywords:
- SSL de modo kernel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 737ac7c6c25bac6e7b66d91aa967fc6fa550459b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665733"
---
# <a name="kernel-mode-ssl"></a><span data-ttu-id="976a6-104">SSL de modo kernel</span><span class="sxs-lookup"><span data-stu-id="976a6-104">Kernel Mode SSL</span></span>

<span data-ttu-id="976a6-105">SSL de modo kernel se presentó en Windows Server 2003 con Service Pack 1 (SP1) con compatibilidad limitada.</span><span class="sxs-lookup"><span data-stu-id="976a6-105">Kernel mode SSL was introduced in Windows Server 2003 with Service Pack 1 (SP1) with limited support.</span></span> <span data-ttu-id="976a6-106">En el caso de los equipos que ejecutan Windows Server 2003 con SP1, debe establecerse una clave del registro para habilitar SSL de kernel.</span><span class="sxs-lookup"><span data-stu-id="976a6-106">For computers running on Windows Server 2003 with SP1 a registry key must be set to enable kernel SSL.</span></span> <span data-ttu-id="976a6-107">En el caso de los equipos que ejecutan Windows Server 2008 y Windows Vista, se proporciona compatibilidad total con el modo kernel para SSL.</span><span class="sxs-lookup"><span data-stu-id="976a6-107">For computers running on Windows Server 2008 and Windows Vista, full kernel mode support for SSL is provided.</span></span>

<span data-ttu-id="976a6-108">En las secciones siguientes se describe la compatibilidad con SSL de modo kernel:</span><span class="sxs-lookup"><span data-stu-id="976a6-108">The following sections describe kernel mode SSL support:</span></span>

-   <span data-ttu-id="976a6-109">Modos de kernel SSL en Windows Server 2003 con SP1</span><span class="sxs-lookup"><span data-stu-id="976a6-109">Kernel Modes SSL in Windows Server 2003 with SP1</span></span>
-   <span data-ttu-id="976a6-110">SSL en modo kernel en Windows Server 2008 y Windows Vista</span><span class="sxs-lookup"><span data-stu-id="976a6-110">Kernel Mode SSL in Windows Server 2008 and Windows Vista</span></span>

## <a name="kernel-modes-ssl-in-windows-server-2003-with-sp1"></a><span data-ttu-id="976a6-111">Modos de kernel SSL en Windows Server 2003 con SP1</span><span class="sxs-lookup"><span data-stu-id="976a6-111">Kernel Modes SSL in Windows Server 2003 with SP1</span></span>

<span data-ttu-id="976a6-112">En Windows Server 2003 con SP1, la API de servidor HTTP ofrece la opción de ejecutar la seguridad SSL en modo kernel (el valor predeterminado es SSL de modo usuario).</span><span class="sxs-lookup"><span data-stu-id="976a6-112">In Windows Server 2003 with SP1, HTTP Server API provides the option of running SSL security in kernel mode (user mode SSL is the default).</span></span> <span data-ttu-id="976a6-113">La característica de modo kernel mejora el rendimiento de SSL moviendo las operaciones de cifrado y descifrado al kernel, con lo que se reduce el número de transiciones entre el modo kernel y el modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="976a6-113">The kernel mode feature improves SSL performance by moving encryption and decryption operations to the kernel, thus reducing the number of transitions between kernel mode and user mode.</span></span>

<span data-ttu-id="976a6-114">Las siguientes características no se admiten cuando SSL se ejecuta en modo kernel:</span><span class="sxs-lookup"><span data-stu-id="976a6-114">The following features are not supported when SSL is run in kernel mode:</span></span>

-   <span data-ttu-id="976a6-115">Certificados de cliente</span><span class="sxs-lookup"><span data-stu-id="976a6-115">Client certificates</span></span>
-   <span data-ttu-id="976a6-116">Cifrados de RC2</span><span class="sxs-lookup"><span data-stu-id="976a6-116">RC2 ciphers</span></span>
-   <span data-ttu-id="976a6-117">Protocolo PCT 1,0</span><span class="sxs-lookup"><span data-stu-id="976a6-117">The PCT 1.0 protocol</span></span>
-   <span data-ttu-id="976a6-118">Los cambios en la configuración del certificado de servidor requieren un reinicio del servicio HTTP</span><span class="sxs-lookup"><span data-stu-id="976a6-118">Server certificate configuration changes require a restart of the HTTP service</span></span>
-   <span data-ttu-id="976a6-119">Compatibilidad con cifrado masivo y descarga</span><span class="sxs-lookup"><span data-stu-id="976a6-119">Bulk encryption and offload support</span></span>

## <a name="configuring-kernel-mode-ssl"></a><span data-ttu-id="976a6-120">Configuración de SSL en modo kernel</span><span class="sxs-lookup"><span data-stu-id="976a6-120">Configuring Kernel Mode SSL</span></span>

<span data-ttu-id="976a6-121">SSL de modo kernel se controla mediante el valor del registro **EnableKernelSSL** y se habilita estableciendo el valor en 1.</span><span class="sxs-lookup"><span data-stu-id="976a6-121">Kernel mode SSL is controlled by the **EnableKernelSSL** registry value and is enabled by setting the value to 1.</span></span> <span data-ttu-id="976a6-122">Al habilitar SSL en modo kernel, se deshabilitará el modo de usuario SSL y es necesario reiniciar el servicio HTTP para que surta efecto.</span><span class="sxs-lookup"><span data-stu-id="976a6-122">Enabling kernel mode SSL will disable user mode SSL and requires the HTTP service to be restarted to take effect.</span></span> <span data-ttu-id="976a6-123">La clave del registro **EnableKernelSSL** se encuentra en:</span><span class="sxs-lookup"><span data-stu-id="976a6-123">The **EnableKernelSSL** registry key is located at:</span></span>

<span data-ttu-id="976a6-124">**HKEY \_ \_** \\ Parámetros http **del sistema** de equipo local \\ **CurrentControlSet** \\ **Services** \\  \\  \\ **EnableKernelSSL**</span><span class="sxs-lookup"><span data-stu-id="976a6-124">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**HTTP**\\**Parameters**\\**EnableKernelSSL**</span></span>

## <a name="kernel-mode-ssl-in-windows-server-2008-and-windows-vista"></a><span data-ttu-id="976a6-125">SSL en modo kernel en Windows Server 2008 y Windows Vista</span><span class="sxs-lookup"><span data-stu-id="976a6-125">Kernel Mode SSL in Windows Server 2008 and Windows Vista</span></span>

<span data-ttu-id="976a6-126">En el caso de los equipos que ejecutan Windows Server 2008 y Windows Vista, la API del servidor HTTP incluye la funcionalidad SSL mejorada.</span><span class="sxs-lookup"><span data-stu-id="976a6-126">For computers running on Windows Server 2008 and Windows Vista, the HTTP Server API features enhanced SSL functionality.</span></span>

<span data-ttu-id="976a6-127">Se admiten las siguientes características nuevas:</span><span class="sxs-lookup"><span data-stu-id="976a6-127">The following new features are supported:</span></span>

-   <span data-ttu-id="976a6-128">Compatibilidad completa con certificados de cliente en modo kernel SSL</span><span class="sxs-lookup"><span data-stu-id="976a6-128">Full client certificate support in kernel mode SSL</span></span>
-   <span data-ttu-id="976a6-129">SSL de modo kernel para todas las transacciones HTTP SSL</span><span class="sxs-lookup"><span data-stu-id="976a6-129">Kernel mode SSL for all HTTP SSL transactions</span></span>
-   <span data-ttu-id="976a6-130">Compatibilidad con cifrado masivo y descarga</span><span class="sxs-lookup"><span data-stu-id="976a6-130">Bulk encryption and offload support</span></span>
-   <span data-ttu-id="976a6-131">Protocolo PCT 1,0</span><span class="sxs-lookup"><span data-stu-id="976a6-131">The PCT 1.0 protocol</span></span>
-   <span data-ttu-id="976a6-132">Cifrados de RC2</span><span class="sxs-lookup"><span data-stu-id="976a6-132">RC2 ciphers</span></span>
-   <span data-ttu-id="976a6-133">Mayor rendimiento en el modo de usuario SSL</span><span class="sxs-lookup"><span data-stu-id="976a6-133">Increased performance over user mode SSL</span></span>

## <a name="configuration"></a><span data-ttu-id="976a6-134">Configuración</span><span class="sxs-lookup"><span data-stu-id="976a6-134">Configuration</span></span>

<span data-ttu-id="976a6-135">SSL de modo kernel se puede configurar a través de dos valores de registro en la clave HTTP Parameters que se encuentra en:</span><span class="sxs-lookup"><span data-stu-id="976a6-135">Kernel mode SSL is configurable through two registry values under the HTTP Parameters key located at:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
                  EnableSslCloseNotify
                  DisableSslCertChainCacheOnlyUrlRetrieval
```

<span data-ttu-id="976a6-136">Un usuario debe tener privilegios de administrador o sistema local para modificar los valores del registro y ver o modificar los archivos de registro y la carpeta que los contiene.</span><span class="sxs-lookup"><span data-stu-id="976a6-136">A user must have Administrator/Local System privileges to modify the registry values and view, or modify, the log files and the folder that contains them.</span></span>

<span data-ttu-id="976a6-137">La información de configuración de los valores del registro se lee cuando se inicia el controlador de la API del servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="976a6-137">Configuration information in the registry values is read when the HTTP Server API driver is started.</span></span> <span data-ttu-id="976a6-138">Como resultado, si se cambia la configuración, el controlador debe detenerse y reiniciarse para leer los nuevos valores.</span><span class="sxs-lookup"><span data-stu-id="976a6-138">As a result, if the settings are changed the driver must be stopped and restarted to read the new values.</span></span> <span data-ttu-id="976a6-139">Esto puede realizarse mediante los siguientes comandos de la consola:</span><span class="sxs-lookup"><span data-stu-id="976a6-139">This can be accomplished by using the following console commands:</span></span>

<span data-ttu-id="976a6-140">**net stop http**</span><span class="sxs-lookup"><span data-stu-id="976a6-140">**net stop http**</span></span>

<span data-ttu-id="976a6-141">**net start http**</span><span class="sxs-lookup"><span data-stu-id="976a6-141">**net start http**</span></span>

<span data-ttu-id="976a6-142">En la tabla siguiente se enumeran los valores de configuración del registro.</span><span class="sxs-lookup"><span data-stu-id="976a6-142">The following table lists registry configuration values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="976a6-143">Valor del registro</span><span class="sxs-lookup"><span data-stu-id="976a6-143">Registry Value</span></span></th>
<th><span data-ttu-id="976a6-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="976a6-144">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="976a6-145">EnableKernelSSL</span><span class="sxs-lookup"><span data-stu-id="976a6-145">EnableKernelSSL</span></span></td>
<td><span data-ttu-id="976a6-146"><strong>Windows Server 2008 y Windows Vista:</strong> Este valor del registro está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="976a6-146"><strong>Windows Server 2008 and Windows Vista:</strong> This registry value is obsolete.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="976a6-147">EnableSslCloseNotify</span><span class="sxs-lookup"><span data-stu-id="976a6-147">EnableSslCloseNotify</span></span></td>
<td><span data-ttu-id="976a6-148">Valor <strong>DWORD</strong> que se establece en <strong>true</strong> para habilitar la notificación de cierre o <strong>false</strong> para deshabilitar el requisito de notificación de cierre.</span><span class="sxs-lookup"><span data-stu-id="976a6-148">A <strong>DWORD</strong> value that is set to <strong>TRUE</strong> to enable close-notify, or <strong>FALSE</strong> to disable the close-notify requirement.</span></span> <span data-ttu-id="976a6-149">Close: Notify está deshabilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="976a6-149">Close-notify is disabled by default.</span></span><br/> <span data-ttu-id="976a6-150">Cuando está habilitada la notificación de cierre, se requiere la aplicación cliente para enviar un mensaje de notificación de cierre antes de cerrar las conexiones TCP.</span><span class="sxs-lookup"><span data-stu-id="976a6-150">When close-notify is enabled, the client application is required to send a close-notify message before closing TCP connections.</span></span> <span data-ttu-id="976a6-151">La API del servidor HTTP también envía una notificación de cierre antes de cerrar la conexión.</span><span class="sxs-lookup"><span data-stu-id="976a6-151">The HTTP Server API also sends a close-notify before closing the connection.</span></span><br/> <span data-ttu-id="976a6-152">Cuando está habilitada la notificación de cierre y el cliente envía un mensaje de notificación de cierre, la API del servidor HTTP volverá a usar la sesión SSL en futuras conexiones con el cliente.</span><span class="sxs-lookup"><span data-stu-id="976a6-152">When close-notify is enabled, and the client sends a close-notify message, the HTTP Server API will reuse the SSL session on future connections to the client.</span></span> <span data-ttu-id="976a6-153">Si el cliente no envía una notificación de cierre, la API del servidor HTTP no volverá a usar la misma sesión SSL en conexiones futuras.</span><span class="sxs-lookup"><span data-stu-id="976a6-153">If the client does not send a close-notify, the HTTP Server API will not reuse the same SSL session on future connections.</span></span> <span data-ttu-id="976a6-154">Por lo tanto, se desencadena un protocolo de enlace SSL completo en la nueva conexión, con lo que se reduce el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="976a6-154">Thus, a full SSL handshake is triggered on the new connection thereby reducing performance.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="976a6-155">Habilitar Close-Notify ayuda a mitigar los ataques de truncamiento contra las solicitudes y respuestas HTTPS.</span><span class="sxs-lookup"><span data-stu-id="976a6-155">Enabling close-notify helps mitigate truncation attacks against the HTTPS requests and responses.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="976a6-156">Cuando se deshabilita la notificación de cierre, la API del servidor HTTP vuelve a usar la sesión SSL para futuras conexiones.</span><span class="sxs-lookup"><span data-stu-id="976a6-156">When close-notify is disabled, the HTTP Server API reuses the SSL session for future connections.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="976a6-157">DisableSslCertChainCacheOnlyUrlRetrieval</span><span class="sxs-lookup"><span data-stu-id="976a6-157">DisableSslCertChainCacheOnlyUrlRetrieval</span></span></td>
<td><span data-ttu-id="976a6-158">Valor <strong>DWORD</strong> que se establece en <strong>true</strong> para permitir que la API del servidor http recupere certificados intermedios desde Internet o desde el almacén local, o bien <strong>false</strong> para recuperar certificados intermedios solo del almacén local.</span><span class="sxs-lookup"><span data-stu-id="976a6-158">A <strong>DWORD</strong> value that is set to <strong>TRUE</strong> to enable the HTTP Server API to retrieve intermediate certificates from either the Internet, or the local store, or <strong>FALSE</strong> to retrieve intermediate certificates from the local store only.</span></span> <span data-ttu-id="976a6-159">El valor del registro predeterminado es <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="976a6-159">The default registry value is <strong>FALSE</strong>.</span></span><br/> <span data-ttu-id="976a6-160">De forma predeterminada, la API del servidor HTTP crea una cadena de certificados de cliente mediante la recuperación de los certificados intermedios del almacén de entidades de certificación intermedio en la cuenta del equipo local.</span><span class="sxs-lookup"><span data-stu-id="976a6-160">By default, the HTTP Server API builds a client certificate chain by retrieving the intermediate certificates from the Intermediate Certificate Authority store under the local machine account.</span></span> <span data-ttu-id="976a6-161">Establecer este valor en <strong>true</strong> permite que la API del servidor http recupere los certificados intermedios no solo del almacén local, sino también de la entidad de certificación intermedia en Internet.</span><span class="sxs-lookup"><span data-stu-id="976a6-161">Setting this value to <strong>TRUE</strong> enables the HTTP Server API to retrieve the intermediate certificates not only from the local store, but also from the Intermediate Certificate Authority on the Internet.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 





