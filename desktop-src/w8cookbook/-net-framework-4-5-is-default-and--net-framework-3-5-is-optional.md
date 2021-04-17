---
title: Configuración predeterminada de .NET Framework
description: .NET Framework 4,5 es el valor predeterminado y .NET Framework 3,5 es opcional
ms.assetid: 19B53C82-812A-49AC-87C6-C08E7C199208
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab1f91acc8739b2c660bfb1ba1392ea192511d1c
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "105705069"
---
# <a name="net-framework-45-is-default-and-net-framework-35-is-optional"></a><span data-ttu-id="292f1-103">.NET Framework 4,5 es el valor predeterminado y .NET Framework 3,5 es opcional</span><span class="sxs-lookup"><span data-stu-id="292f1-103">.NET Framework 4.5 is default and .NET Framework 3.5 is optional</span></span>

## <a name="platforms"></a><span data-ttu-id="292f1-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="292f1-104">Platforms</span></span>

<span data-ttu-id="292f1-105">**Clientes**   de   Windows 8</span><span class="sxs-lookup"><span data-stu-id="292f1-105">**Clients**   Windows 8</span></span>  
<span data-ttu-id="292f1-106">**Servidores**   de   Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="292f1-106">**Servers**   Windows Server 2012</span></span>  

## <a name="description"></a><span data-ttu-id="292f1-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="292f1-107">Description</span></span>

<span data-ttu-id="292f1-108">.NET Framework 4,5 está habilitado de forma predeterminada en Windows 8.</span><span class="sxs-lookup"><span data-stu-id="292f1-108">.NET Framework 4.5 is enabled by default in Windows 8.</span></span> <span data-ttu-id="292f1-109">Windows 8 no incluye .NET 3,5 de forma predeterminada, pero los archivos para .NET 3,5 están disponibles en los medios de instalación de Windows 8 como una característica opcional.</span><span class="sxs-lookup"><span data-stu-id="292f1-109">Windows 8 does not include .NET 3.5 by default, but the files for .NET 3.5 are available on the Windows 8 installation media as an optional feature.</span></span>

<span data-ttu-id="292f1-110">Si el usuario está actualizando de Windows 7 a Windows 8, .NET Framework 3,5 está totalmente habilitado para asegurarse de que las aplicaciones del equipo sigan funcionando correctamente.</span><span class="sxs-lookup"><span data-stu-id="292f1-110">If the user is upgrading from Windows 7 to Windows 8, .NET Framework 3.5 is fully enabled to ensure that any apps on the computer continue to work correctly.</span></span>

## <a name="manifestation"></a><span data-ttu-id="292f1-111">Manifestación</span><span class="sxs-lookup"><span data-stu-id="292f1-111">Manifestation</span></span>

<span data-ttu-id="292f1-112">Si el usuario realiza una instalación limpia de Windows 8 y, a continuación, instala las aplicaciones que requieren .NET Framework 3,5 (o 2,0), desencadenará una solicitud para los archivos de .NET 3,5 necesarios.</span><span class="sxs-lookup"><span data-stu-id="292f1-112">If the user performs a clean installation of Windows 8, and then installs apps that require .NET Framework 3.5 (or 2.0), they will trigger a request for the necessary .NET 3.5 files.</span></span> <span data-ttu-id="292f1-113">Normalmente, los archivos que faltan se descargarán de Windows Update (después de solicitar permiso al usuario), pero si no es posible el acceso a Windows Update, la habilitación de .NET Framework 3,5 producirá un error a menos que se haya especificado un origen alternativo para los archivos que faltan.</span><span class="sxs-lookup"><span data-stu-id="292f1-113">Normally the missing files will be downloaded from Windows Update (after asking the user for permission), but if access to Windows Update is not possible, enabling .NET Framework 3.5 will fail unless an alternate source for the missing files has been specified.</span></span>

## <a name="mitigation"></a><span data-ttu-id="292f1-114">Mitigación</span><span class="sxs-lookup"><span data-stu-id="292f1-114">Mitigation</span></span>

<span data-ttu-id="292f1-115">Para habilitar .NET Framework 3,5 solo en máquinas de prueba con instalaciones limpias de Windows 8:</span><span class="sxs-lookup"><span data-stu-id="292f1-115">To enable .NET Framework 3.5 on only test machines with clean installs of Windows 8:</span></span>

1.  <span data-ttu-id="292f1-116">Copie \\ \\ los orígenes SxS \\ de la imagen ISO de compilación del sistema operativo montada en dotnet35 o en una carpeta similar.</span><span class="sxs-lookup"><span data-stu-id="292f1-116">Copy \\sources\\sxs\\ from the mounted operating system build ISO image to dotnet35 or similar folder.</span></span> <span data-ttu-id="292f1-117">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="292f1-117">For example:</span></span>
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  <span data-ttu-id="292f1-118">Ejecute esta línea de comandos con privilegios de administrador:</span><span class="sxs-lookup"><span data-stu-id="292f1-118">Execute this command line using admin privileges:</span></span>
    ```
    Dism.exe /online /enable-feature /featurename:NetFX3 /All /Source:c:\dotnet35 /LimitAccess

    ```



> [!Note]  
> <span data-ttu-id="292f1-119">La carpeta de orígenes \\ SxS no debe usarse como mecanismo de redistribución, ya que no es un mecanismo compatible.</span><span class="sxs-lookup"><span data-stu-id="292f1-119">The sources\\SxS folder must not be used as a redistribution mechanism since this is not a supported mechanism.</span></span>



## <a name="solution"></a><span data-ttu-id="292f1-120">Solución</span><span class="sxs-lookup"><span data-stu-id="292f1-120">Solution</span></span>

<span data-ttu-id="292f1-121">**Para los consumidores:**</span><span class="sxs-lookup"><span data-stu-id="292f1-121">**For consumers:**</span></span>

<span data-ttu-id="292f1-122">Windows 8 incluye un mecanismo que habilita automáticamente .NET Framework 3,5 al intentar instalar el paquete redistribuible o cuando un instalador de la aplicación que necesita .NET 3,5 invoca el redistribuible.</span><span class="sxs-lookup"><span data-stu-id="292f1-122">Windows 8 includes a mechanism that automatically enables .NET Framework 3.5 when attempting to install the redistributable package or when an application installer that needs .NET 3.5 invokes the redistributable.</span></span>

<span data-ttu-id="292f1-123">**Para desarrolladores de aplicaciones (y administradores de TI):**</span><span class="sxs-lookup"><span data-stu-id="292f1-123">**For App developers (and IT Administrators):**</span></span>

<span data-ttu-id="292f1-124">Los administradores de TI pueden configurar aplicaciones de .NET 3,5 para que se ejecuten en .NET 3,5 o .NET 4,5 (según lo que ya esté instalado).</span><span class="sxs-lookup"><span data-stu-id="292f1-124">IT administrators can configure .NET 3.5 apps to run on either .NET 3.5 or .NET 4.5 (depending on what's already installed).</span></span> <span data-ttu-id="292f1-125">Para ejecutar una aplicación administrada en 3,5 o 4,5, solo tiene que agregar una sección en el archivo de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="292f1-125">In order to run a managed app on either 3.5 or 4.5, just add a section in the application configuration file.</span></span> <span data-ttu-id="292f1-126">Esto garantizará que si .NET 3,5 está instalado, la aplicación se ejecutará en .NET 3,5; de lo contrario, la aplicación se ejecutará en .NET 4,5.</span><span class="sxs-lookup"><span data-stu-id="292f1-126">This will ensure that if .NET 3.5 is installed, the app will run on .NET 3.5; otherwise the app will run on .NET 4.5.</span></span> <span data-ttu-id="292f1-127">A continuación se proporciona un ejemplo de la sección adicional en el archivo de configuración:</span><span class="sxs-lookup"><span data-stu-id="292f1-127">An example of the additional section in the configuration file is provided below:</span></span>


```
<configuration>
   <startup>
      <supportedRuntime version="v2.0.50727"/>
      <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5"/>
   </startup>
</configuration>
```



<span data-ttu-id="292f1-128">**Para los OEM de empresa:**</span><span class="sxs-lookup"><span data-stu-id="292f1-128">**For enterprise OEMs:**</span></span>

<span data-ttu-id="292f1-129">Para habilitar .NET Framework 3,5 para las compilaciones de EEAP y para las aplicaciones que no tienen acceso a Windows Update:</span><span class="sxs-lookup"><span data-stu-id="292f1-129">To enable .NET Framework 3.5 for EEAP builds and for applications that do not have access to Windows Update:</span></span>

1.  <span data-ttu-id="292f1-130">Copie los \\ orígenes \\ SxS \\ de la imagen ISO de compilación del SO montado en la dotnet35 o en una carpeta similar.</span><span class="sxs-lookup"><span data-stu-id="292f1-130">Copy \\sources\\sxs\\ from the mounted OS build ISO image to the dotnet35 or similar folder.</span></span> <span data-ttu-id="292f1-131">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="292f1-131">For example:</span></span>
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  <span data-ttu-id="292f1-132">Establezca RegKey:</span><span class="sxs-lookup"><span data-stu-id="292f1-132">Set the regkey:</span></span>
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]
     LocalSourcePath = c:\dotnet35
    ```



<span data-ttu-id="292f1-133">**Para empresas:**</span><span class="sxs-lookup"><span data-stu-id="292f1-133">**For enterprises:**</span></span>

<span data-ttu-id="292f1-134">En el caso de las máquinas que están configuradas para usar WSUS para el servicio, puede establecer una entrada del registro para permitir que el equipo use Windows Update para habilitar .NET 3,5 en lugar de WSUS (el mantenimiento se realizará desde WSUS si lo hace).</span><span class="sxs-lookup"><span data-stu-id="292f1-134">For machines that are configured to use WSUS for servicing, you can set a registry entry to allow the machine to use Windows Update for enabling .NET 3.5 instead of WSUS (servicing will still be done from WSUS if you do this).</span></span>

-   <span data-ttu-id="292f1-135">Establezca RegKey:</span><span class="sxs-lookup"><span data-stu-id="292f1-135">Set the regkey:</span></span>
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]  RepairContentServerSource =DWORD(2)
    ```



<span data-ttu-id="292f1-136">Esta entrada del registro también se puede establecer mediante directiva de grupo (Directiva de equipo local-configuración del equipo de >-> Plantillas administrativas-> sistema.</span><span class="sxs-lookup"><span data-stu-id="292f1-136">This registry entry can also be set via Group Policy (Local Computer Policy -> Computer Configuration -> Administrative Templates -> System.</span></span> <span data-ttu-id="292f1-137">Seleccione la opción especificar la configuración de instalación de componentes opcionales y reparación de componentes.</span><span class="sxs-lookup"><span data-stu-id="292f1-137">Select the setting  Specify settings for optional component installation and component repair .</span></span>

<span data-ttu-id="292f1-138">Si selecciona contacto Windows Update directamente para descargar el contenido de reparación en lugar de Windows Server Update Services (WSUS), cualquier intento de agregar características de Windows (por ejemplo, .NET Framework 3,5) o características de reparación desencadenará descargas de archivos de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="292f1-138">If you select  Contact Windows Update directly to download repair content instead of Windows Server Update Services (WSUS) , any attempts to add Windows features (for example, .NET Framework 3.5) or repair features will trigger file downloads from Windows Update.</span></span> <span data-ttu-id="292f1-139">Los equipos de destino necesitan acceso a Internet y WU para esta opción.</span><span class="sxs-lookup"><span data-stu-id="292f1-139">Target computers require Internet and WU access for this option.</span></span> <span data-ttu-id="292f1-140">Las operaciones de mantenimiento normales siguen usando WSUS si se ha configurado como origen.</span><span class="sxs-lookup"><span data-stu-id="292f1-140">Normal servicing operations continue to use WSUS if it has been configured as a source.</span></span>

<span data-ttu-id="292f1-141">**Nota relativa a la configuración de la ubicación de origen local a través de entradas del registro**</span><span class="sxs-lookup"><span data-stu-id="292f1-141">**A note regarding setting local source location via registry entries**</span></span>

<span data-ttu-id="292f1-142">Los administradores de TI pueden establecer ubicaciones de origen locales para los archivos de .NET 3,5 a través de una entrada del registro, de modo que los usuarios puedan usar el cuadro de diálogo Agregar o quitar características de Windows para habilitar características con carga útil que faltan sin tener que especificar una ubicación de origen.</span><span class="sxs-lookup"><span data-stu-id="292f1-142">IT administrators can set local source location(s) for .NET 3.5 files via a registry entry, so that users can use the Add/Remove Windows Features dialog to enable features with missing payload without having to specify a source location.</span></span> <span data-ttu-id="292f1-143">El valor de la entrada del registro se puede controlar a través de la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="292f1-143">The value of the registry entry can be controlled via group policy.</span></span>

<span data-ttu-id="292f1-144">Se admite esta entrada del registro:</span><span class="sxs-lookup"><span data-stu-id="292f1-144">This registry entry is supported:</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="292f1-145">Entrada</span><span class="sxs-lookup"><span data-stu-id="292f1-145">Entry</span></span></th>
<th><span data-ttu-id="292f1-146">Tipo</span><span class="sxs-lookup"><span data-stu-id="292f1-146">Type</span></span></th>
<th><span data-ttu-id="292f1-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="292f1-147">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="292f1-148">Ruta de acceso de origen local</span><span class="sxs-lookup"><span data-stu-id="292f1-148">Local Source Path</span></span></td>
<td><span data-ttu-id="292f1-149"> REG_EXPAND_SZ </span><span class="sxs-lookup"><span data-stu-id="292f1-149">REG_EXPAND_SZ</span></span></td>
<td><span data-ttu-id="292f1-150">Rutas de acceso de origen local que se usarán de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="292f1-150">Local source path(s) to be used by default.</span></span> <span data-ttu-id="292f1-151">Se pueden especificar varias rutas de acceso; deben separarse mediante;.</span><span class="sxs-lookup"><span data-stu-id="292f1-151">Multiple paths can be specified; they should be separated by  ; .</span></span> <span data-ttu-id="292f1-152">Las ubicaciones se buscarán en el orden en que se especifiquen.</span><span class="sxs-lookup"><span data-stu-id="292f1-152">Locations will be searched in the order they are specified.</span></span> <br/> <span data-ttu-id="292f1-153">Las ubicaciones de origen locales especificadas en la línea de comandos de DISM tienen prioridad sobre las ubicaciones especificadas en esta entrada del registro.</span><span class="sxs-lookup"><span data-stu-id="292f1-153">Local source location(s) that are specified on the DISM command line, take precedence over locations specified in this registry entry.</span></span> <span data-ttu-id="292f1-154">Las ubicaciones de carpeta se pueden especificar en esta entrada del registro.</span><span class="sxs-lookup"><span data-stu-id="292f1-154">Folder locations can be specified in this registry entry.</span></span> <br/> <span data-ttu-id="292f1-155">Se puede usar Wim, pero la ruta de acceso debe ser al archivo WIM; no es necesario montarlo, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="292f1-155">WIMs can be used, but the path must be to the WIM file; there is no need to mount it, for example:</span></span> <br/> <dl> <span data-ttu-id="292f1-156">Wim: \\ machine\share\file.Wim: 1</span><span class="sxs-lookup"><span data-stu-id="292f1-156">wim:\\machine\share\file.wim:1</span></span><br />
</dl> <span data-ttu-id="292f1-157">Observe el 1 al final.</span><span class="sxs-lookup"><span data-stu-id="292f1-157">Notice the  1  at the end.</span></span> <span data-ttu-id="292f1-158">Debe especificar el índice numérico de la imagen que desea utilizar en el archivo WIM.</span><span class="sxs-lookup"><span data-stu-id="292f1-158">You must specify the numerical index of the image you want to use in the WIM file.</span></span> <br/> <span data-ttu-id="292f1-159">En el caso de una WIM montada, la ruta de acceso de origen debe hacer referencia al directorio de Windows de la imagen montada, en lugar de al punto de montaje (por ejemplo:/Source: <mount_point> \Windows en lugar de/Source: <mount_point> ).</span><span class="sxs-lookup"><span data-stu-id="292f1-159">For a mounted WIM, the source path needs to refer to the windows directory of the mounted image, rather than to the mount point (for example: /source:<mount_point>\windows rather than /source:<mount_point>).</span></span> <br/></td>
</tr>
</tbody>
</table>





## <a name="resources"></a><span data-ttu-id="292f1-160">Recursos</span><span class="sxs-lookup"><span data-stu-id="292f1-160">Resources</span></span>

<dl>

[<span data-ttu-id="292f1-161">Implementación de directivas basadas en el registro</span><span class="sxs-lookup"><span data-stu-id="292f1-161">Implementing Registry-based Policy</span></span>](/previous-versions/windows/desktop/Policy/implementing-registry-based-policy)  
</dl>