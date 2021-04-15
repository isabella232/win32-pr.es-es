---
title: Solución de problemas de empaquetado, implementación y consulta de aplicaciones de Windows
description: Siga estas sugerencias para solucionar los problemas que experimente al empaquetar, implementar o consultar un paquete de la aplicación.
ms.assetid: 38E327C6-0345-4FA6-BCDB-5FA2FCD421FB
ms.topic: article
ms.date: 02/20/2020
manager: dcscontentpm
ms.custom:
- CI 111497
- CSSTroubleshooting
- contperf-fy21q2
ms.openlocfilehash: a2ee7c28e7de2d616bd01e9b5cae0de3c325caf4
ms.sourcegitcommit: 80198645ddacc3c12c72f3814b71ade0f415e705
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/25/2021
ms.locfileid: "105709280"
---
# <a name="troubleshooting-packaging-deployment-and-query-of-windows-apps"></a><span data-ttu-id="a222d-103">Solución de problemas de empaquetado, implementación y consulta de aplicaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="a222d-103">Troubleshooting packaging, deployment, and query of Windows apps</span></span>

<span data-ttu-id="a222d-104">Siga estas sugerencias para solucionar los problemas que experimente al empaquetar, implementar o consultar un paquete de aplicación de Windows (. msix/. appx) como desarrollador.</span><span class="sxs-lookup"><span data-stu-id="a222d-104">Use these suggestions to troubleshoot problems you experience when packaging, deploying, or querying a Windows app package (.msix/.appx) as a developer.</span></span>

> [!NOTE]
> <span data-ttu-id="a222d-105">Este artículo está destinado a los desarrolladores.</span><span class="sxs-lookup"><span data-stu-id="a222d-105">This article is intended for developers.</span></span> <span data-ttu-id="a222d-106">Si no es un desarrollador y busca ayuda con un error de instalación de aplicación de Windows, consulte [soporte técnico de Windows](https://support.microsoft.com/hub/4338813/windows-help?os=windows-10).</span><span class="sxs-lookup"><span data-stu-id="a222d-106">If you are not a developer and you are looking for help with a Windows app installation error, see [Windows support](https://support.microsoft.com/hub/4338813/windows-help?os=windows-10).</span></span>

## <a name="get-diagnostic-information"></a><span data-ttu-id="a222d-107">Obtención de información de diagnóstico</span><span class="sxs-lookup"><span data-stu-id="a222d-107">Get diagnostic information</span></span>

<span data-ttu-id="a222d-108">Cuando se produce un error en una API, devuelve un código de error que describe el problema.</span><span class="sxs-lookup"><span data-stu-id="a222d-108">When an API fails, it returns an error code that describes the problem.</span></span> <span data-ttu-id="a222d-109">Si el código de error no proporciona suficiente información, encontrará más información de diagnóstico en los registros de eventos detallados.</span><span class="sxs-lookup"><span data-stu-id="a222d-109">If the error code doesn't provide enough information, you find more diagnostic information in the detailed event logs.</span></span>

<span data-ttu-id="a222d-110">Para obtener acceso a los registros de eventos de empaquetado e implementación mediante **visor de eventos**, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="a222d-110">To access the packaging and deployment event logs by using **Event Viewer**, follow these steps:</span></span>

1. <span data-ttu-id="a222d-111">Realice uno de estos pasos:</span><span class="sxs-lookup"><span data-stu-id="a222d-111">Perform one of the following steps:</span></span>

    * <span data-ttu-id="a222d-112">Haga clic en **Inicio** en el menú Windows, escriba **visor de eventos** y **presione Entrar**.</span><span class="sxs-lookup"><span data-stu-id="a222d-112">Click **Start** on the Windows menu, type **Event Viewer**, and **press Enter**.</span></span>
    * <span data-ttu-id="a222d-113">Ejecute **eventvwr. msc**.</span><span class="sxs-lookup"><span data-stu-id="a222d-113">Run **eventvwr.msc**.</span></span>

2. <span data-ttu-id="a222d-114">En la página de la izquierda, expanda **visor de eventos (local)**  >  **registros de aplicaciones y servicios**  >  **Microsoft**  >  **Windows**.</span><span class="sxs-lookup"><span data-stu-id="a222d-114">In the left page, expand **Event Viewer (Local)** > **Applications and Services Logs** > **Microsoft** > **Windows**.</span></span>
3. <span data-ttu-id="a222d-115">Compruebe si hay registros disponibles en estas categorías:</span><span class="sxs-lookup"><span data-stu-id="a222d-115">Check for available logs under these categories:</span></span>

    * <span data-ttu-id="a222d-116">**AppxPackagingOM**  >  **Microsoft-Windows-AppxPackaging/Operational**</span><span class="sxs-lookup"><span data-stu-id="a222d-116">**AppxPackagingOM** > **Microsoft-Windows-AppxPackaging/Operational**</span></span>
    * <span data-ttu-id="a222d-117">**AppXDeployment: servidor**  >  **Microsoft-Windows-AppXDeploymentServer/Operational**</span><span class="sxs-lookup"><span data-stu-id="a222d-117">**AppXDeployment-Server** > **Microsoft-Windows-AppXDeploymentServer/Operational**</span></span>

<span data-ttu-id="a222d-118">Para empezar, consulte los registros en **AppXDeployment-Server**.</span><span class="sxs-lookup"><span data-stu-id="a222d-118">Start by looking at the logs under **AppXDeployment-Server**.</span></span> <span data-ttu-id="a222d-119">Si el error se debe a **0x80073CF0** o **ERROR_INSTALL_OPEN_PACKAGE_FAILED**, pueden aparecer detalles adicionales en los registros de **AppxpackagingOM** .</span><span class="sxs-lookup"><span data-stu-id="a222d-119">If the error was caused by **0x80073CF0** or **ERROR_INSTALL_OPEN_PACKAGE_FAILED**, additional details may be present in the **AppxpackagingOM** logs.</span></span>

<span data-ttu-id="a222d-120">También puede usar el comando [Get-AppxLog](/powershell/module/appx/get-appxlog) en PowerShell para obtener los primeros eventos registrados.</span><span class="sxs-lookup"><span data-stu-id="a222d-120">You can also use the [Get-AppxLog](/powershell/module/appx/get-appxlog) command in PowerShell to get the first few logged events.</span></span> <span data-ttu-id="a222d-121">En el ejemplo siguiente se muestran los registros asociados con la operación de implementación más reciente.</span><span class="sxs-lookup"><span data-stu-id="a222d-121">The following example displays the logs associated with the most recent deployment operation.</span></span>

```PowerShell
Get-Appxlog
```

<span data-ttu-id="a222d-122">En el ejemplo siguiente se muestran los registros asociados con la operación de implementación más reciente en una tabla interactiva en una ventana independiente.</span><span class="sxs-lookup"><span data-stu-id="a222d-122">The following example displays the logs associated with the most recent deployment operation in an interactive table in a separate window.</span></span>

```PowerShell
Get-Appxlog | Out-GridView
```

## <a name="common-error-codes"></a><span data-ttu-id="a222d-123">Códigos comunes de error</span><span class="sxs-lookup"><span data-stu-id="a222d-123">Common error codes</span></span>

<span data-ttu-id="a222d-124">En esta tabla se enumeran algunos de los códigos de error más comunes.</span><span class="sxs-lookup"><span data-stu-id="a222d-124">This table lists some of the most common error codes.</span></span> <span data-ttu-id="a222d-125">Si necesita más ayuda con uno de estos errores, o si encuentra un código de error que no está en esta lista, consulte Opciones de [ayuda adicionales](#get-additional-help).</span><span class="sxs-lookup"><span data-stu-id="a222d-125">If you need further help with one of these errors, or if you're encountering an error code not in this list, see [additional help options](#get-additional-help).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a222d-126">Código de error</span><span class="sxs-lookup"><span data-stu-id="a222d-126">Error code</span></span></th>
<th><span data-ttu-id="a222d-127">Value</span><span class="sxs-lookup"><span data-stu-id="a222d-127">Value</span></span></th>
<th><span data-ttu-id="a222d-128">Descripción y causas posibles</span><span class="sxs-lookup"><span data-stu-id="a222d-128">Description and possible causes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
<td><span data-ttu-id="a222d-129"><strong>E_FILENOTFOUND</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-129"><strong>E_FILENOTFOUND</strong></span></span></td>
<td><span data-ttu-id="a222d-130">0x80070002</span><span class="sxs-lookup"><span data-stu-id="a222d-130">0x80070002</span></span></td>
<td><span data-ttu-id="a222d-131">El archivo o la ruta de acceso no se encuentra.</span><span class="sxs-lookup"><span data-stu-id="a222d-131">File or path is not found.</span></span> <span data-ttu-id="a222d-132">Esto puede ocurrir durante la validación de la biblioteca de bibliotecas COM requiere que la ruta de acceso del directorio exista realmente en el paquete MSIX.</span><span class="sxs-lookup"><span data-stu-id="a222d-132">This can occur during a COM  typelib validation requires that the path for the directory actually exist within your MSIX package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-133"><strong>ERROR_BAD_FORMAT</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-133"><strong>ERROR_BAD_FORMAT</strong></span></span></td>
<td><span data-ttu-id="a222d-134">0x8007000B</span><span class="sxs-lookup"><span data-stu-id="a222d-134">0x8007000B</span></span></td>
<td><span data-ttu-id="a222d-135">El paquete no tiene el formato correcto y debe volver a generarse o firmarse.</span><span class="sxs-lookup"><span data-stu-id="a222d-135">The package isn't correctly formatted and needs to be re-built or re-signed.</span></span><br/> <span data-ttu-id="a222d-136">Este error puede aparecer si hay una discrepancia entre el nombre de sujeto del certificado de firma y el nombre del publicador de AppxManifest.xml.</span><span class="sxs-lookup"><span data-stu-id="a222d-136">You may get this error if there is a mismatch between the signing certificate subject name and the AppxManifest.xml publisher name.</span></span><br/> <span data-ttu-id="a222d-137">Consulte <a href="how-to-sign-a-package-using-signtool.md">cómo firmar un paquete de aplicación mediante SignTool</a>.</span><span class="sxs-lookup"><span data-stu-id="a222d-137">See <a href="how-to-sign-a-package-using-signtool.md">How to sign an app package using SignTool</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-138"><strong>E_INVALIDARG</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-138"><strong>E_INVALIDARG</strong></span></span></td>
<td><span data-ttu-id="a222d-139">0x80070057</span><span class="sxs-lookup"><span data-stu-id="a222d-139">0x80070057</span></span></td>
<td><span data-ttu-id="a222d-140">Uno o varios argumentos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="a222d-140">One or more arguments are not valid.</span></span> <span data-ttu-id="a222d-141">Si comprueba la AppXDeployment-Server registro de eventos y ve el siguiente evento: "al instalar el paquete, el sistema no pudo registrar la extensión Windows. repositoryExtension debido al siguiente error: el parámetro es incorrecto".</span><span class="sxs-lookup"><span data-stu-id="a222d-141">If you check the AppXDeployment-Server event log and see the following event: "While installing the package, the system failed to register the windows.repositoryExtension extension due to the following error: The parameter is incorrect."</span></span> <br/> <span data-ttu-id="a222d-142">Este error puede aparecer si el elemento de manifiesto DisplayName o Description contiene caracteres no permitidos por Firewall de Windows; es decir, |  y todo, debido a que Windows no puede crear el perfil de AppContainer para el paquete.</span><span class="sxs-lookup"><span data-stu-id="a222d-142">You may get this error if the manifest elements DisplayName or Description contain characters disallowed by Windows firewall; namely  |  and  all , due to which Windows fails to create the AppContainer profile for the package.</span></span> <span data-ttu-id="a222d-143">Quite estos caracteres del manifiesto e intente instalar el paquete.</span><span class="sxs-lookup"><span data-stu-id="a222d-143">Please remove these characters from the manifest and try installing the package.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-144"><strong>ERROR_INSTALL_OPEN_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-144"><strong>ERROR_INSTALL_OPEN_</strong></span></span><br/> <span data-ttu-id="a222d-145"><strong>PACKAGE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-145"><strong>PACKAGE_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-146">0x80073CF0</span><span class="sxs-lookup"><span data-stu-id="a222d-146">0x80073CF0</span></span></td>
<td><span data-ttu-id="a222d-147">No se pudo abrir el paquete.</span><span class="sxs-lookup"><span data-stu-id="a222d-147">The package couldn't be opened.</span></span><br/> <span data-ttu-id="a222d-148">Causas posibles:</span><span class="sxs-lookup"><span data-stu-id="a222d-148">Possible causes:</span></span><br/>
<ul>
<li><span data-ttu-id="a222d-149">El paquete no está firmado.</span><span class="sxs-lookup"><span data-stu-id="a222d-149">The package is unsigned.</span></span></li>
<li><span data-ttu-id="a222d-150">El nombre del publicador no coincide con el firmante del certificado de firma.</span><span class="sxs-lookup"><span data-stu-id="a222d-150">The publisher name doesn't match the signing certificate subject.</span></span></li>
<li><span data-ttu-id="a222d-151">Falta el prefijo file://o el paquete no se pudo encontrar en la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="a222d-151">The file:// prefix is missing or the package couldn't be found at the specified location.</span></span></li>
</ul>
<span data-ttu-id="a222d-152">Para obtener más información, consulte el registro de eventos <strong>AppxPackagingOM</strong> .</span><span class="sxs-lookup"><span data-stu-id="a222d-152">For more information, check the <strong>AppxPackagingOM</strong> event log.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-153"><strong>ERROR_INSTALL_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-153"><strong>ERROR_INSTALL_PACKAGE_</strong></span></span><br/> <span data-ttu-id="a222d-154"><strong>NOT_FOUND</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-154"><strong>NOT_FOUND</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-155">0x80073CF1</span><span class="sxs-lookup"><span data-stu-id="a222d-155">0x80073CF1</span></span></td>
<td><span data-ttu-id="a222d-156">No se pudo encontrar el paquete.</span><span class="sxs-lookup"><span data-stu-id="a222d-156">The package couldn't be found.</span></span><br/> <span data-ttu-id="a222d-157">Puede obtener este error al quitar un paquete que no está instalado para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="a222d-157">You may get this error while removing a package that isn't installed for the current user.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-158"><strong>ERROR_INSTALL_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-158"><strong>ERROR_INSTALL_INVALID_</strong></span></span><br/> <span data-ttu-id="a222d-159"><strong>CONFIGURA</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-159"><strong>PACKAGE</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-160">0x80073CF2</span><span class="sxs-lookup"><span data-stu-id="a222d-160">0x80073CF2</span></span></td>
<td><span data-ttu-id="a222d-161">Los datos del paquete no son válidos.</span><span class="sxs-lookup"><span data-stu-id="a222d-161">The package data isn't valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-162"><strong>ERROR_INSTALL_RESOLVE_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-162"><strong>ERROR_INSTALL_RESOLVE_</strong></span></span><br/> <span data-ttu-id="a222d-163"><strong>DEPENDENCY_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-163"><strong>DEPENDENCY_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-164">0x80073CF3</span><span class="sxs-lookup"><span data-stu-id="a222d-164">0x80073CF3</span></span></td>
<td><span data-ttu-id="a222d-165">Error de actualización, dependencia o validación de conflicto en el paquete.</span><span class="sxs-lookup"><span data-stu-id="a222d-165">The package failed update, dependency, or conflict validation.</span></span><br/> <span data-ttu-id="a222d-166">Causas posibles:</span><span class="sxs-lookup"><span data-stu-id="a222d-166">Possible causes:</span></span><br/>
<ul>
<li><span data-ttu-id="a222d-167">El paquete entrante entra en conflicto con un paquete instalado.</span><span class="sxs-lookup"><span data-stu-id="a222d-167">The incoming package conflicts with an installed package.</span></span></li>
<li><span data-ttu-id="a222d-168">No se encuentra una dependencia del paquete especificada.</span><span class="sxs-lookup"><span data-stu-id="a222d-168">A specified package dependency can't be found.</span></span></li>
<li><span data-ttu-id="a222d-169">El paquete no es compatible con la arquitectura de procesador correcta.</span><span class="sxs-lookup"><span data-stu-id="a222d-169">The package doesn't support the correct processor architecture.</span></span></li>
</ul>
<span data-ttu-id="a222d-170">Para obtener más informtion, consulte el registro de eventos <strong>de AppXDeployment-Server</strong> .</span><span class="sxs-lookup"><span data-stu-id="a222d-170">For more informtion, check the <strong>AppXDeployment-Server</strong> event log.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-171"><strong>ERROR_INSTALL_OUT_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-171"><strong>ERROR_INSTALL_OUT_</strong></span></span><br/> <span data-ttu-id="a222d-172"><strong>OF_DISK_SPACE</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-172"><strong>OF_DISK_SPACE</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-173">0x80073CF4</span><span class="sxs-lookup"><span data-stu-id="a222d-173">0x80073CF4</span></span></td>
<td><span data-ttu-id="a222d-174">No hay suficiente espacio en disco en el equipo.</span><span class="sxs-lookup"><span data-stu-id="a222d-174">There isn't enough disk space on your computer.</span></span> <span data-ttu-id="a222d-175">Libere espacio y vuelva a intentarlo.</span><span class="sxs-lookup"><span data-stu-id="a222d-175">Free some space and try again.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-176"><strong>ERROR_INSTALL_NETWORK_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-176"><strong>ERROR_INSTALL_NETWORK_</strong></span></span><br/> <span data-ttu-id="a222d-177"><strong>FALLIDA</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-177"><strong>FAILURE</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-178">0x80073CF5</span><span class="sxs-lookup"><span data-stu-id="a222d-178">0x80073CF5</span></span></td>
<td><span data-ttu-id="a222d-179">No se puede descargar el paquete.</span><span class="sxs-lookup"><span data-stu-id="a222d-179">The package can't be downloaded.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-180"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-180"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="a222d-181"><strong>REGISTRATION_FAILURE</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-181"><strong>REGISTRATION_FAILURE</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-182">0x80073CF6</span><span class="sxs-lookup"><span data-stu-id="a222d-182">0x80073CF6</span></span></td>
<td><span data-ttu-id="a222d-183">No se puede registrar el paquete.</span><span class="sxs-lookup"><span data-stu-id="a222d-183">The package can't be registered.</span></span><br/> <span data-ttu-id="a222d-184">Para obtener más información, consulte el registro de eventos de <strong>AppXDeployment-Server</strong> .</span><span class="sxs-lookup"><span data-stu-id="a222d-184">For more information, check the <strong>AppXDeployment-Server</strong> event log.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-185"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-185"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="a222d-186"><strong>DEREGISTRATION_EFAILURE</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-186"><strong>DEREGISTRATION_EFAILURE</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-187">0x80073CF7</span><span class="sxs-lookup"><span data-stu-id="a222d-187">0x80073CF7</span></span></td>
<td><span data-ttu-id="a222d-188">No se puede anular el registro del paquete.</span><span class="sxs-lookup"><span data-stu-id="a222d-188">The package can't be unregistered.</span></span><br/> <span data-ttu-id="a222d-189">Puede obtener este error al quitar un paquete.</span><span class="sxs-lookup"><span data-stu-id="a222d-189">You may get this error while removing a package.</span></span><br/> <span data-ttu-id="a222d-190">Para obtener más información, consulte el registro de eventos de <strong>AppXDeployment-Server</strong> .</span><span class="sxs-lookup"><span data-stu-id="a222d-190">For more information, check the <strong>AppXDeployment-Server</strong> event log.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-191"><strong>ERROR_INSTALL_CANCEL</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-191"><strong>ERROR_INSTALL_CANCEL</strong></span></span></td>
<td><span data-ttu-id="a222d-192">0x80073CF8</span><span class="sxs-lookup"><span data-stu-id="a222d-192">0x80073CF8</span></span></td>
<td><span data-ttu-id="a222d-193">El usuario canceló la solicitud de instalación.</span><span class="sxs-lookup"><span data-stu-id="a222d-193">The user canceled the install request.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-194"><strong>ERROR_INSTALL_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-194"><strong>ERROR_INSTALL_FAILED</strong></span></span></td>
<td><span data-ttu-id="a222d-195">0x80073CF9</span><span class="sxs-lookup"><span data-stu-id="a222d-195">0x80073CF9</span></span></td>
<td><span data-ttu-id="a222d-196">No se pudo instalar el paquete.</span><span class="sxs-lookup"><span data-stu-id="a222d-196">Package install failed.</span></span> <span data-ttu-id="a222d-197">Póngase en contacto con el proveedor de software.</span><span class="sxs-lookup"><span data-stu-id="a222d-197">Contact the software vendor.</span></span><br/> <span data-ttu-id="a222d-198">Para obtener más información, consulte el registro de eventos de <strong>AppXDeployment-Server</strong> .</span><span class="sxs-lookup"><span data-stu-id="a222d-198">For more information, check the <strong>AppXDeployment-Server</strong> event log.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-199"><strong>ERROR_REMOVE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-199"><strong>ERROR_REMOVE_FAILED</strong></span></span></td>
<td><span data-ttu-id="a222d-200">0x80073CFA</span><span class="sxs-lookup"><span data-stu-id="a222d-200">0x80073CFA</span></span></td>
<td><span data-ttu-id="a222d-201">No se pudo quitar el paquete.</span><span class="sxs-lookup"><span data-stu-id="a222d-201">Package removal failed.</span></span><br/> <span data-ttu-id="a222d-202">Puede obtener este error en caso de errores que se produzcan durante la desinstalación del paquete.</span><span class="sxs-lookup"><span data-stu-id="a222d-202">You may get this error for failures that occur during package uninstall.</span></span><br/> <span data-ttu-id="a222d-203">Para obtener más información, vea <a href="/uwp/api/windows.management.deployment.packagemanager.removepackageasync"><strong>RemovePackageAsync</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a222d-203">For more information, see <a href="/uwp/api/windows.management.deployment.packagemanager.removepackageasync"><strong>RemovePackageAsync</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-204"><strong>ERROR_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-204"><strong>ERROR_PACKAGE_</strong></span></span><br/> <span data-ttu-id="a222d-205"><strong>ALREADY_EXISTS</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-205"><strong>ALREADY_EXISTS</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-206">0x80073CFB</span><span class="sxs-lookup"><span data-stu-id="a222d-206">0x80073CFB</span></span></td>
<td><span data-ttu-id="a222d-207">El paquete suministrado ya está instalado y se ha bloqueado la reinstalación del paquete.</span><span class="sxs-lookup"><span data-stu-id="a222d-207">The provided package is already installed, and reinstallation of the package is blocked.</span></span> <br/> <span data-ttu-id="a222d-208">Puede obtener este error si instala un paquete que no es idéntico bit a bit al paquete que ya está instalado.</span><span class="sxs-lookup"><span data-stu-id="a222d-208">You may get this error if installing a package that is not bitwise identical to the package that is already installed.</span></span> <span data-ttu-id="a222d-209">Tenga en cuenta que la firma digital también forma parte del paquete.</span><span class="sxs-lookup"><span data-stu-id="a222d-209">Note that the digital signature is also part of the package.</span></span> <span data-ttu-id="a222d-210">Por lo tanto, si se vuelve a generar o se vuelve a firmar un paquete, ya no es idéntico bit a bit al paquete instalado previamente.</span><span class="sxs-lookup"><span data-stu-id="a222d-210">Hence if a package is rebuilt or resigned, it is no longer bitwise identical to the previously installed package.</span></span> <span data-ttu-id="a222d-211">Dos opciones posibles para corregir este error son: (1) incrementar el número de versión de la aplicación y, a continuación, volver a generar y firmar el paquete (2) quitar el paquete antiguo para todos los usuarios del sistema antes de instalar el nuevo paquete.</span><span class="sxs-lookup"><span data-stu-id="a222d-211">Two possible options to fix this error are: (1) Increment the version number of the app, then rebuild and resign the package (2) Remove the old package for every user on the system before installing the new package.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-212"><strong>ERROR_NEEDS_REMEDIATION</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-212"><strong>ERROR_NEEDS_REMEDIATION</strong></span></span></td>
<td><span data-ttu-id="a222d-213">0x80073CFC</span><span class="sxs-lookup"><span data-stu-id="a222d-213">0x80073CFC</span></span></td>
<td><span data-ttu-id="a222d-214">No se puede iniciar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a222d-214">The app can't be started.</span></span> <span data-ttu-id="a222d-215">Intente volver a instalar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a222d-215">Try reinstalling the app.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-216"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-216"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="a222d-217"><strong>PREREQUISITE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-217"><strong>PREREQUISITE_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-218">0x80073CFD</span><span class="sxs-lookup"><span data-stu-id="a222d-218">0x80073CFD</span></span></td>
<td><span data-ttu-id="a222d-219">No se pudo satisfacer un requisito previo de instalación especificado.</span><span class="sxs-lookup"><span data-stu-id="a222d-219">A specified install prerequisite couldn't be satisfied.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-220"><strong>ERROR_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-220"><strong>ERROR_PACKAGE_</strong></span></span><br/> <span data-ttu-id="a222d-221"><strong>REPOSITORY_CORRUPTED</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-221"><strong>REPOSITORY_CORRUPTED</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-222">0x80073CFE</span><span class="sxs-lookup"><span data-stu-id="a222d-222">0x80073CFE</span></span></td>
<td><span data-ttu-id="a222d-223">El repositorio de paquetes está dañado.</span><span class="sxs-lookup"><span data-stu-id="a222d-223">The package repository is corrupted.</span></span><br/> <span data-ttu-id="a222d-224">Puede obtener este error si la carpeta a la que hace referencia esta clave del registro no existe o está dañada:</span><span class="sxs-lookup"><span data-stu-id="a222d-224">You may get this error if the folder referenced by this registry key doesn't exist or is corrupted:</span></span> <br/> <span data-ttu-id="a222d-225"><strong>HKLM\SOFTWARE\Microsoft\Windows</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-225"><strong>HKLM\Software\Microsoft\Windows\</strong></span></span><br/> <span data-ttu-id="a222d-226"><strong>CurrentVersion\Appx\PackageRepositoryRoot</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-226"><strong>CurrentVersion\Appx\PackageRepositoryRoot</strong></span></span><br/> <span data-ttu-id="a222d-227">Para recuperarse de este estado, actualice el equipo.</span><span class="sxs-lookup"><span data-stu-id="a222d-227">To recover from this state, refresh your PC.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-228"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-228"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="a222d-229"><strong>POLICY_FAILURE</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-229"><strong>POLICY_FAILURE</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-230">0x80073CFF</span><span class="sxs-lookup"><span data-stu-id="a222d-230">0x80073CFF</span></span></td>
<td><span data-ttu-id="a222d-231">Para instalar esta aplicación, necesita una licencia de desarrollador o un sistema habilitado para instalación de prueba.</span><span class="sxs-lookup"><span data-stu-id="a222d-231">To install this app, you need a developer license or a sideloading-enabled system.</span></span> <br/> <span data-ttu-id="a222d-232">Es posible que reciba este error si el paquete no cumple uno de los siguientes requisitos:</span><span class="sxs-lookup"><span data-stu-id="a222d-232">You may get this error if the package doesn't meet one of the following requirements:</span></span><br/>
<ul>
<li><span data-ttu-id="a222d-233">La aplicación se implementa con F5 en Visual Studio en un equipo con una licencia de desarrollador de Windows.</span><span class="sxs-lookup"><span data-stu-id="a222d-233">The app is deployed using F5 in Visual Studio on a computer with a Windows developer license.</span></span></li>
<li><span data-ttu-id="a222d-234">El paquete se firma con una firma de Microsoft y se implementa como parte de Windows o desde el Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="a222d-234">The package is signed with a Microsoft signature and deployed as part of Windows or from the Microsoft Store.</span></span></li>
<li><span data-ttu-id="a222d-235">El paquete se firma con una firma de confianza y se instala en un equipo con una licencia de desarrollador, un equipo unido a un dominio con la Directiva AllowAllTrustedApps habilitada, o un equipo con una licencia de instalación de prueba de Windows con la Directiva AllowAllTrustedApps habilitada.</span><span class="sxs-lookup"><span data-stu-id="a222d-235">The package is signed with a trusted signature and installed on a computer with a developer license, a domain-joined computer with the AllowAllTrustedApps policy enabled, or a computer with a Windows Sideloading license with the AllowAllTrustedApps policy enabled.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-236"><strong>ERROR_PACKAGE_UPDATING</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-236"><strong>ERROR_PACKAGE_UPDATING</strong></span></span></td>
<td><span data-ttu-id="a222d-237">0x80073D00</span><span class="sxs-lookup"><span data-stu-id="a222d-237">0x80073D00</span></span></td>
<td><span data-ttu-id="a222d-238">No se puede iniciar la aplicación porque se está actualizando.</span><span class="sxs-lookup"><span data-stu-id="a222d-238">The app can't be started because it's currently updating.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-239"><strong>ERROR_DEPLOYMENT_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-239"><strong>ERROR_DEPLOYMENT_</strong></span></span><br/> <span data-ttu-id="a222d-240"><strong>BLOCKED_BY_POLICY</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-240"><strong>BLOCKED_BY_POLICY</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-241">0x80073D01</span><span class="sxs-lookup"><span data-stu-id="a222d-241">0x80073D01</span></span></td>
<td><span data-ttu-id="a222d-242">La Directiva bloquea la operación de implementación de paquetes.</span><span class="sxs-lookup"><span data-stu-id="a222d-242">The package deployment operation is blocked by policy.</span></span> <span data-ttu-id="a222d-243">Póngase en contacto con el administrador del sistema.</span><span class="sxs-lookup"><span data-stu-id="a222d-243">Contact your system administrator.</span></span><br/> <span data-ttu-id="a222d-244">Causas posibles:</span><span class="sxs-lookup"><span data-stu-id="a222d-244">Possible causes:</span></span><br/>
<ul>
<li><span data-ttu-id="a222d-245">Las directivas de control de aplicaciones bloquean la implementación de paquetes.</span><span class="sxs-lookup"><span data-stu-id="a222d-245">Package deployment is blocked by Application Control Policies.</span></span></li>
<li><span data-ttu-id="a222d-246">La implementación de paquetes está bloqueada por la &quot; Directiva permitir operaciones de implementación en perfiles especiales &quot; .</span><span class="sxs-lookup"><span data-stu-id="a222d-246">Package deployment is blocked by the &quot;Allow deployment operations in special profiles&quot; policy.</span></span></li>
</ul>
<span data-ttu-id="a222d-247">Uno de los motivos posibles es una necesidad de un perfil móvil.</span><span class="sxs-lookup"><span data-stu-id="a222d-247">One of the possible reasons is a need for a roaming profile.</span></span> <span data-ttu-id="a222d-248">Para obtener información acerca de cómo configurar perfiles de usuario móviles en cuentas de usuario, consulte <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj649079(v=ws.11)">implementar perfiles de usuario móviles</a>.</span><span class="sxs-lookup"><span data-stu-id="a222d-248">For information about setting up Roaming User Profiles on user accounts, see <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj649079(v=ws.11)">Deploy Roaming User Profiles</a>.</span></span> <span data-ttu-id="a222d-249">Si no hay directivas configuradas en el sistema y sigue viendo este error, es posible que haya iniciado sesión con un perfil temporal.</span><span class="sxs-lookup"><span data-stu-id="a222d-249">If there are no policies configured on your system and you still see this error, perhaps you are logged in with a temporary profile.</span></span> <span data-ttu-id="a222d-250">Cierre la sesión y vuelva a iniciarla e intente la operación de nuevo.</span><span class="sxs-lookup"><span data-stu-id="a222d-250">Log out and log in again, then try the operation again.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-251"><strong>ERROR_PACKAGES_IN_USE</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-251"><strong>ERROR_PACKAGES_IN_USE</strong></span></span></td>
<td><span data-ttu-id="a222d-252">0x80073D02</span><span class="sxs-lookup"><span data-stu-id="a222d-252">0x80073D02</span></span></td>
<td><span data-ttu-id="a222d-253">No se pudo instalar el paquete porque los recursos modificados están actualmente en uso.</span><span class="sxs-lookup"><span data-stu-id="a222d-253">The package couldn't be installed because resources it modifies are currently in use.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-254"><strong>ERROR_RECOVERY_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-254"><strong>ERROR_RECOVERY_</strong></span></span><br/> <span data-ttu-id="a222d-255"><strong>FILE_CORRUPT</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-255"><strong>FILE_CORRUPT</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-256">0x80073D03</span><span class="sxs-lookup"><span data-stu-id="a222d-256">0x80073D03</span></span></td>
<td><span data-ttu-id="a222d-257">No se pudo recuperar el paquete porque los datos necesarios para la recuperación están dañados.</span><span class="sxs-lookup"><span data-stu-id="a222d-257">The package couldn't be recovered because data that's necessary for recovery is corrupted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-258"><strong>ERROR_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-258"><strong>ERROR_INVALID_</strong></span></span><br/> <span data-ttu-id="a222d-259"><strong>STAGED_SIGNATURE</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-259"><strong>STAGED_SIGNATURE</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-260">0x80073D04</span><span class="sxs-lookup"><span data-stu-id="a222d-260">0x80073D04</span></span></td>
<td><span data-ttu-id="a222d-261">La firma no es válida.</span><span class="sxs-lookup"><span data-stu-id="a222d-261">The signature isn't valid.</span></span> <span data-ttu-id="a222d-262">Para registrarse en modo de desarrollador, AppxSignature. p7x y AppxBlockMap.xml deben ser válidos o no deben estar presentes.</span><span class="sxs-lookup"><span data-stu-id="a222d-262">To register in developer mode, AppxSignature.p7x and AppxBlockMap.xml must be valid or shouldn't be present.</span></span><br/> <span data-ttu-id="a222d-263">Si es un desarrollador que usa F5 con Visual Studio, asegúrese de que el directorio de proyecto creado no contiene archivos de asignación de firma o bloque de las versiones anteriores del paquete.</span><span class="sxs-lookup"><span data-stu-id="a222d-263">If you are a developer using F5 with Visual Studio, ensure that your built project directory doesn't contain signature or block map files from previous versions of the package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-264"><strong>ERROR_DELETING_EXISTING_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-264"><strong>ERROR_DELETING_EXISTING_</strong></span></span><br/> <span data-ttu-id="a222d-265"><strong>APPLICATIONDATA_STORE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-265"><strong>APPLICATIONDATA_STORE_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-266">0x80073D05</span><span class="sxs-lookup"><span data-stu-id="a222d-266">0x80073D05</span></span></td>
<td><span data-ttu-id="a222d-267">Se produjo un error al eliminar los datos de aplicación existentes anteriormente del paquete.</span><span class="sxs-lookup"><span data-stu-id="a222d-267">An error occurred while deleting the package's previously existing application data.</span></span><br/> <span data-ttu-id="a222d-268">Puede obtener este error si el <a href="/previous-versions/hh441475(v=vs.110)">simulador</a> se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="a222d-268">You can get this error if the <a href="/previous-versions/hh441475(v=vs.110)">simulator</a> is running.</span></span> <span data-ttu-id="a222d-269">Cierre el simulador.</span><span class="sxs-lookup"><span data-stu-id="a222d-269">Close the simulator.</span></span> <span data-ttu-id="a222d-270">También puede obtener este error si hay archivos abiertos en los datos de la aplicación (por ejemplo, si tiene un archivo de registro abierto en un editor de texto).</span><span class="sxs-lookup"><span data-stu-id="a222d-270">You can also get this error if there are files open in the app data (for example, if you have a log file open in a text editor).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-271"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-271"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="a222d-272"><strong>PACKAGE_DOWNGRADE</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-272"><strong>PACKAGE_DOWNGRADE</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-273">0x80073D06</span><span class="sxs-lookup"><span data-stu-id="a222d-273">0x80073D06</span></span></td>
<td><span data-ttu-id="a222d-274">No se pudo instalar el paquete porque ya hay instalada una versión superior de este paquete.</span><span class="sxs-lookup"><span data-stu-id="a222d-274">The package couldn't be installed because a higher version of this package is already installed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-275"><strong>ERROR_SYSTEM_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-275"><strong>ERROR_SYSTEM_</strong></span></span><br/> <span data-ttu-id="a222d-276"><strong>NEEDS_REMEDIATION</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-276"><strong>NEEDS_REMEDIATION</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-277">0x80073D07</span><span class="sxs-lookup"><span data-stu-id="a222d-277">0x80073D07</span></span></td>
<td><span data-ttu-id="a222d-278">Se detectó un error en un archivo binario del sistema.</span><span class="sxs-lookup"><span data-stu-id="a222d-278">An error in a system binary was detected.</span></span> <span data-ttu-id="a222d-279">Para solucionar el problema, intente actualizar el equipo.</span><span class="sxs-lookup"><span data-stu-id="a222d-279">To fix the problem, try refreshing the PC.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-280"><strong>ERROR_APPX_INTEGRITY_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-280"><strong>ERROR_APPX_INTEGRITY_</strong></span></span><br/> <span data-ttu-id="a222d-281"><strong>FAILURE_EXTERNAL</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-281"><strong>FAILURE_EXTERNAL</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-282">0x80073D08</span><span class="sxs-lookup"><span data-stu-id="a222d-282">0x80073D08</span></span></td>
<td><span data-ttu-id="a222d-283">Se detectó un binario dañado que no es de Windows en el sistema.</span><span class="sxs-lookup"><span data-stu-id="a222d-283">A corrupted non-Windows binary was detected on the system.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-284"><strong>ERROR_RESILIENCY_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-284"><strong>ERROR_RESILIENCY_</strong></span></span><br/> <span data-ttu-id="a222d-285"><strong>FILE_CORRUPT</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-285"><strong>FILE_CORRUPT</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-286">0x80073D09</span><span class="sxs-lookup"><span data-stu-id="a222d-286">0x80073D09</span></span></td>
<td><span data-ttu-id="a222d-287">No se pudo reanudar la operación porque los datos necesarios para la recuperación están dañados.</span><span class="sxs-lookup"><span data-stu-id="a222d-287">The operation couldn't be resumed because data that's necessary for recovery is corrupted.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-288"><strong>ERROR_INSTALL_FIREWALL_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-288"><strong>ERROR_INSTALL_FIREWALL_</strong></span></span><br/> <span data-ttu-id="a222d-289"><strong>SERVICE_NOT_RUNNING</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-289"><strong>SERVICE_NOT_RUNNING</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-290">0x80073D0A</span><span class="sxs-lookup"><span data-stu-id="a222d-290">0x80073D0A</span></span></td>
<td><span data-ttu-id="a222d-291">No se pudo instalar el paquete porque el servicio Firewall de Windows no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="a222d-291">The package couldn't be installed because the Windows Firewall service isn't running.</span></span> <span data-ttu-id="a222d-292">Habilite el servicio Firewall de Windows e inténtelo de nuevo.</span><span class="sxs-lookup"><span data-stu-id="a222d-292">Enable the Windows Firewall service and try again.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-293"><strong>ERROR_PACKAGE_MOVE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-293"><strong>ERROR_PACKAGE_MOVE_FAILED</strong></span></span></td>
<td><span data-ttu-id="a222d-294">0x80073D0B</span><span class="sxs-lookup"><span data-stu-id="a222d-294">0x80073D0B</span></span></td>
<td><span data-ttu-id="a222d-295">Error en la operación de movimiento del paquete.</span><span class="sxs-lookup"><span data-stu-id="a222d-295">The package move operation failed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-296"><strong>ERROR_INSTALL_VOLUME_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-296"><strong>ERROR_INSTALL_VOLUME_</strong></span></span><br/> <span data-ttu-id="a222d-297"><strong>NOT_EMPTY</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-297"><strong>NOT_EMPTY</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-298">0x80073D0C</span><span class="sxs-lookup"><span data-stu-id="a222d-298">0x80073D0C</span></span></td>
<td><span data-ttu-id="a222d-299">No se pudo realizar la operación de implementación porque el volumen no está vacío.</span><span class="sxs-lookup"><span data-stu-id="a222d-299">The deployment operation failed because the volume is not empty.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-300"><strong>ERROR_INSTALL_VOLUME_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-300"><strong>ERROR_INSTALL_VOLUME_</strong></span></span><br/> <span data-ttu-id="a222d-301"><strong>N</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-301"><strong>OFFLINE</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-302">0x80073D0D</span><span class="sxs-lookup"><span data-stu-id="a222d-302">0x80073D0D</span></span></td>
<td><span data-ttu-id="a222d-303">No se pudo realizar la operación de implementación porque el volumen está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="a222d-303">The deployment operation failed because the volume is offline.</span></span> <span data-ttu-id="a222d-304">En el caso de una actualización del paquete, el volumen hace referencia al volumen instalado de todas las versiones del paquete.</span><span class="sxs-lookup"><span data-stu-id="a222d-304">For a package update, the volume refers to the installed volume of all package versions.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-305"><strong>ERROR_INSTALL_VOLUME_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-305"><strong>ERROR_INSTALL_VOLUME_</strong></span></span><br/> <span data-ttu-id="a222d-306"><strong>CORRUPCIÓN</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-306"><strong>CORRUPT</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-307">0x80073D0E</span><span class="sxs-lookup"><span data-stu-id="a222d-307">0x80073D0E</span></span></td>
<td><span data-ttu-id="a222d-308">No se pudo realizar la operación de implementación porque el volumen especificado está dañado.</span><span class="sxs-lookup"><span data-stu-id="a222d-308">The deployment operation failed because the specified volume is corrupt.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-309"><strong>ERROR_NEEDS_REGISTRATION</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-309"><strong>ERROR_NEEDS_REGISTRATION</strong></span></span><br/> <strong></strong><br/></td>
<td><span data-ttu-id="a222d-310">0x80073D0F</span><span class="sxs-lookup"><span data-stu-id="a222d-310">0x80073D0F</span></span></td>
<td><span data-ttu-id="a222d-311">No se pudo realizar la operación de implementación porque primero es necesario registrar la aplicación especificada.</span><span class="sxs-lookup"><span data-stu-id="a222d-311">The deployment operation failed because the specified application needs to be registered first.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-312"><strong>ERROR_INSTALL_WRONG_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-312"><strong>ERROR_INSTALL_WRONG_</strong></span></span><br/> <span data-ttu-id="a222d-313"><strong>PROCESSOR_ARCHITECTURE</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-313"><strong>PROCESSOR_ARCHITECTURE</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-314">0x80073D10</span><span class="sxs-lookup"><span data-stu-id="a222d-314">0x80073D10</span></span></td>
<td><span data-ttu-id="a222d-315">No se pudo realizar la operación de implementación porque el paquete tiene como destino la arquitectura de procesador incorrecta.</span><span class="sxs-lookup"><span data-stu-id="a222d-315">The deployment operation failed because the package targets the wrong processor architecture.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-316"><strong>ERROR_DEV_SIDELOAD_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-316"><strong>ERROR_DEV_SIDELOAD_</strong></span></span><br/> <span data-ttu-id="a222d-317"><strong>LIMIT_EXCEEDED</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-317"><strong>LIMIT_EXCEEDED</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-318">0x80073D11</span><span class="sxs-lookup"><span data-stu-id="a222d-318">0x80073D11</span></span></td>
<td><span data-ttu-id="a222d-319">Ha alcanzado el número máximo de paquetes de instalación de prueba de desarrollador permitidos en este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a222d-319">You have reached the maximum number of developer sideloaded packages allowed on this device.</span></span> <span data-ttu-id="a222d-320">Desinstale un paquete de instalación de prueba y vuelva a intentarlo.</span><span class="sxs-lookup"><span data-stu-id="a222d-320">Please uninstall a sideloaded package and try again.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-321"><strong>ERROR_INSTALL_OPTIONAL_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-321"><strong>ERROR_INSTALL_OPTIONAL_</strong></span></span><br/> <span data-ttu-id="a222d-322"><strong>PACKAGE_REQUIRES_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-322"><strong>PACKAGE_REQUIRES_</strong></span></span><br/> <span data-ttu-id="a222d-323"><strong>MAIN_PACKAGE</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-323"><strong>MAIN_PACKAGE</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-324">0x80073D12</span><span class="sxs-lookup"><span data-stu-id="a222d-324">0x80073D12</span></span></td>
<td><span data-ttu-id="a222d-325">Se requiere un paquete de aplicación principal para instalar este paquete opcional.</span><span class="sxs-lookup"><span data-stu-id="a222d-325">A main app package is required to install this optional package.</span></span> <span data-ttu-id="a222d-326">Instale primero el paquete principal e inténtelo de nuevo.</span><span class="sxs-lookup"><span data-stu-id="a222d-326">Install the main package first and try again.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-327"><strong>ERROR_PACKAGE_NOT_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-327"><strong>ERROR_PACKAGE_NOT_</strong></span></span><br/> <span data-ttu-id="a222d-328"><strong>SUPPORTED_ON_FILESYSTEM</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-328"><strong>SUPPORTED_ON_FILESYSTEM</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-329">0x80073D13</span><span class="sxs-lookup"><span data-stu-id="a222d-329">0x80073D13</span></span></td>
<td><span data-ttu-id="a222d-330">Este tipo de paquete de aplicación no es compatible con este sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="a222d-330">This app package type is not supported on this filesystem.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-331"><strong>ERROR_PACKAGE_MOVE_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-331"><strong>ERROR_PACKAGE_MOVE_</strong></span></span><br/> <span data-ttu-id="a222d-332"><strong>BLOCKED_BY_STREAMING</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-332"><strong>BLOCKED_BY_STREAMING</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-333">0x80073D14</span><span class="sxs-lookup"><span data-stu-id="a222d-333">0x80073D14</span></span></td>
<td><span data-ttu-id="a222d-334">La operación de movimiento de paquetes se bloquea hasta que la aplicación haya finalizado el streaming.</span><span class="sxs-lookup"><span data-stu-id="a222d-334">Package move operation is blocked until the application has finished streaming.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-335"><strong>ERROR_INSTALL_OPTIONAL_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-335"><strong>ERROR_INSTALL_OPTIONAL_</strong></span></span><br/> <span data-ttu-id="a222d-336"><strong>PACKAGE_APPLICATIONID_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-336"><strong>PACKAGE_APPLICATIONID_</strong></span></span><br/> <span data-ttu-id="a222d-337"><strong>NOT_UNIQUE</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-337"><strong>NOT_UNIQUE</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-338">0x80073D15</span><span class="sxs-lookup"><span data-stu-id="a222d-338">0x80073D15</span></span></td>
<td><span data-ttu-id="a222d-339">Un paquete de aplicación principal u otro opcional tiene el mismo identificador de aplicación que este paquete opcional.</span><span class="sxs-lookup"><span data-stu-id="a222d-339">A main or another optional app package has the same application ID as this optional package.</span></span> <span data-ttu-id="a222d-340">Cambie el identificador de la aplicación para el paquete opcional para evitar conflictos.</span><span class="sxs-lookup"><span data-stu-id="a222d-340">Change the application ID for the optional package to avoid conflicts.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-341"><strong>ERROR_PACKAGE_STAGING_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-341"><strong>ERROR_PACKAGE_STAGING_</strong></span></span><br/> <span data-ttu-id="a222d-342"><strong>ONHOLD</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-342"><strong>ONHOLD</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-343">0x80073D16</span><span class="sxs-lookup"><span data-stu-id="a222d-343">0x80073D16</span></span></td>
<td><span data-ttu-id="a222d-344">Esta sesión de ensayo se ha mantenido para permitir la priorización de otra operación de almacenamiento provisional.</span><span class="sxs-lookup"><span data-stu-id="a222d-344">This staging session has been held to allow another staging operation to be prioritized.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-345"><strong>ERROR_INSTALL_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-345"><strong>ERROR_INSTALL_INVALID_</strong></span></span><br/> <span data-ttu-id="a222d-346"><strong>RELATED_SET_UPDATE</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-346"><strong>RELATED_SET_UPDATE</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-347">0x80073D17</span><span class="sxs-lookup"><span data-stu-id="a222d-347">0x80073D17</span></span></td>
<td><span data-ttu-id="a222d-348">No se puede actualizar un conjunto relacionado porque el conjunto actualizado no es válido.</span><span class="sxs-lookup"><span data-stu-id="a222d-348">A related set cannot be updated because the updated set is invalid.</span></span> <span data-ttu-id="a222d-349">Todos los paquetes del conjunto relacionado deben actualizarse al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="a222d-349">All packages in the related set must be updated at the same time.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-350"><strong>ERROR_INSTALL_OPTIONAL_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-350"><strong>ERROR_INSTALL_OPTIONAL_</strong></span></span><br/> <span data-ttu-id="a222d-351"><strong>PACKAGE_REQUIRES_MAIN_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-351"><strong>PACKAGE_REQUIRES_MAIN_</strong></span></span><br/> <span data-ttu-id="a222d-352"><strong>PACKAGE_FULLTRUST_CAPABILITY</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-352"><strong>PACKAGE_FULLTRUST_CAPABILITY</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-353">0x80073D18</span><span class="sxs-lookup"><span data-stu-id="a222d-353">0x80073D18</span></span></td>
<td><span data-ttu-id="a222d-354">Un paquete opcional con un punto de entrada FullTrust requiere que el paquete principal tenga la funcionalidad <strong>runFullTrust</strong> .</span><span class="sxs-lookup"><span data-stu-id="a222d-354">An optional package with a FullTrust entry point requires the main package to have the <strong>runFullTrust</strong> capability.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-355"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-355"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span></span><br/> <span data-ttu-id="a222d-356"><strong>BY_USER_LOG_OFF</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-356"><strong>BY_USER_LOG_OFF</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-357">0x80073D19</span><span class="sxs-lookup"><span data-stu-id="a222d-357">0x80073D19</span></span></td>
<td><span data-ttu-id="a222d-358">Error al cerrar la sesión de un usuario.</span><span class="sxs-lookup"><span data-stu-id="a222d-358">An error occurred because a user was logged off.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-359"><strong>ERROR_PROVISION_OPTIONAL_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-359"><strong>ERROR_PROVISION_OPTIONAL_</strong></span></span><br/> <span data-ttu-id="a222d-360"><strong>PACKAGE_REQUIRES_MAIN_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-360"><strong>PACKAGE_REQUIRES_MAIN_</strong></span></span><br/> <span data-ttu-id="a222d-361"><strong>PACKAGE_PROVISIONED</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-361"><strong>PACKAGE_PROVISIONED</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-362">0x80073D1A</span><span class="sxs-lookup"><span data-stu-id="a222d-362">0x80073D1A</span></span></td>
<td><span data-ttu-id="a222d-363">Un aprovisionamiento de paquetes opcional requiere que el paquete principal de dependencia también esté aprovisionado.</span><span class="sxs-lookup"><span data-stu-id="a222d-363">An optional package provision requires the dependency main package to also be provisioned.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-364"><strong>ERROR_PACKAGES_REPUTATION_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-364"><strong>ERROR_PACKAGES_REPUTATION_</strong></span></span><br/> <span data-ttu-id="a222d-365"><strong>CHECK_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-365"><strong>CHECK_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-366">0x80073D1B</span><span class="sxs-lookup"><span data-stu-id="a222d-366">0x80073D1B</span></span></td>
<td><span data-ttu-id="a222d-367">No se pudo <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">comprobar la reputación de SmartScreen</a>en los paquetes.</span><span class="sxs-lookup"><span data-stu-id="a222d-367">The packages failed the <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">SmartScreen reputation check</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-368"><strong>ERROR_PACKAGES_REPUTATION_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-368"><strong>ERROR_PACKAGES_REPUTATION_</strong></span></span><br/> <span data-ttu-id="a222d-369"><strong>CHECK_TIMEDOUT</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-369"><strong>CHECK_TIMEDOUT</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-370">0x80073D1C</span><span class="sxs-lookup"><span data-stu-id="a222d-370">0x80073D1C</span></span></td>
<td><span data-ttu-id="a222d-371">Se agotó el tiempo de espera de la operación de <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">comprobación de reputación de SmartScreen</a> .</span><span class="sxs-lookup"><span data-stu-id="a222d-371">The <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">SmartScreen reputation check</a> operation timed out.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-372"><strong>ERROR_DEPLOYMENT_OPTION_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-372"><strong>ERROR_DEPLOYMENT_OPTION_</strong></span></span><br/> <span data-ttu-id="a222d-373"><strong>NOT_SUPPORTED</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-373"><strong>NOT_SUPPORTED</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-374">0x80073D1D</span><span class="sxs-lookup"><span data-stu-id="a222d-374">0x80073D1D</span></span></td>
<td><span data-ttu-id="a222d-375">No se admite la opción de implementación actual.</span><span class="sxs-lookup"><span data-stu-id="a222d-375">The current deployment option is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-376"><strong>ERROR_APPINSTALLER_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-376"><strong>ERROR_APPINSTALLER_</strong></span></span><br/> <span data-ttu-id="a222d-377"><strong>ACTIVATION_BLOCKED</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-377"><strong>ACTIVATION_BLOCKED</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-378">0x80073D1E</span><span class="sxs-lookup"><span data-stu-id="a222d-378">0x80073D1E</span></span></td>
<td><span data-ttu-id="a222d-379">La activación está bloqueada debido a la configuración de actualización. AppInstaller para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="a222d-379">Activation is blocked due to the .appinstaller update settings for this app.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-380"><strong>ERROR_REGISTRATION_FROM_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-380"><strong>ERROR_REGISTRATION_FROM_</strong></span></span><br/> <span data-ttu-id="a222d-381"><strong>REMOTE_DRIVE_NOT_SUPPORTED</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-381"><strong>REMOTE_DRIVE_NOT_SUPPORTED</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-382">0x80073D1F</span><span class="sxs-lookup"><span data-stu-id="a222d-382">0x80073D1F</span></span></td>
<td><span data-ttu-id="a222d-383">No se admiten las unidades remotas.</span><span class="sxs-lookup"><span data-stu-id="a222d-383">Remote drives are not supported.</span></span> <span data-ttu-id="a222d-384">Use <strong> \\ servidor\recurso compartido</strong> para registrar un paquete remoto.</span><span class="sxs-lookup"><span data-stu-id="a222d-384">Use <strong>\\server\share</strong> to register a remote package.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-385"><strong>ERROR_APPX_RAW_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-385"><strong>ERROR_APPX_RAW_</strong></span></span><br/> <span data-ttu-id="a222d-386"><strong>DATA_WRITE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-386"><strong>DATA_WRITE_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-387">0x80073D20</span><span class="sxs-lookup"><span data-stu-id="a222d-387">0x80073D20</span></span></td>
<td><span data-ttu-id="a222d-388">No se pudieron procesar y escribir los datos del paquete descargado en el disco.</span><span class="sxs-lookup"><span data-stu-id="a222d-388">Failed to process and write downloaded package data to disk.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-389"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-389"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span></span><br/> <span data-ttu-id="a222d-390"><strong>BY_VOLUME_POLICY_PACKAGE</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-390"><strong>BY_VOLUME_POLICY_PACKAGE</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-391">0x80073D21</span><span class="sxs-lookup"><span data-stu-id="a222d-391">0x80073D21</span></span></td>
<td><span data-ttu-id="a222d-392">La operación de implementación se bloqueó debido a una directiva de familia por paquete que restringe las implementaciones en un volumen que no es del sistema.</span><span class="sxs-lookup"><span data-stu-id="a222d-392">The deployment operation was blocked due to a per-package-family policy restricting deployments on a non-system volume.</span></span> <span data-ttu-id="a222d-393">Por directiva, esta aplicación debe instalarse en la unidad del sistema, pero no se establece como el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a222d-393">Per policy, this app must be installed to the system drive, but that's not set as the default.</span></span> <span data-ttu-id="a222d-394">En configuración de almacenamiento, haga que la unidad del sistema sea la ubicación predeterminada para guardar el nuevo contenido y, a continuación, vuelva a intentar la instalación.</span><span class="sxs-lookup"><span data-stu-id="a222d-394">In Storage settings, make the system drive the default location to save new content, then retry the install.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-395"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-395"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span></span><br/> <span data-ttu-id="a222d-396"><strong>BY_VOLUME_POLICY_MACHINE</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-396"><strong>BY_VOLUME_POLICY_MACHINE</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-397">0x80073D22</span><span class="sxs-lookup"><span data-stu-id="a222d-397">0x80073D22</span></span></td>
<td><span data-ttu-id="a222d-398">La operación de implementación se bloqueó debido a que una directiva de todo el equipo restringe las implementaciones en un volumen que no es del sistema.</span><span class="sxs-lookup"><span data-stu-id="a222d-398">The deployment operation was blocked due to a machine-wide policy restricting deployments on a non-system volume.</span></span> <span data-ttu-id="a222d-399">Por directiva, esta aplicación debe instalarse en la unidad del sistema, pero no se establece como el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a222d-399">Per policy, this app must be installed to the system drive, but that's not set as the default.</span></span> <span data-ttu-id="a222d-400">En configuración de almacenamiento, haga que la unidad del sistema sea la ubicación predeterminada para guardar el nuevo contenido y, a continuación, vuelva a intentar la instalación.</span><span class="sxs-lookup"><span data-stu-id="a222d-400">In Storage settings, make the system drive the default location to save new content, then retry the install.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-401"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-401"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span></span><br/> <span data-ttu-id="a222d-402"><strong>BY_PROFILE_POLICY</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-402"><strong>BY_PROFILE_POLICY</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-403">0x80073D23</span><span class="sxs-lookup"><span data-stu-id="a222d-403">0x80073D23</span></span></td>
<td><span data-ttu-id="a222d-404">La operación de implementación se bloqueó porque no se permite una implementación de perfil especial (los perfiles especiales son perfiles de usuario en los que se descartan los cambios después de que el usuario cierra la sesión).</span><span class="sxs-lookup"><span data-stu-id="a222d-404">The deployment operation was blocked because special profile deployment is not allowed (special profiles are user profiles where changes are discarded after the user signs out).</span></span> <span data-ttu-id="a222d-405">Intente iniciar sesión en una cuenta que no sea un perfil especial.</span><span class="sxs-lookup"><span data-stu-id="a222d-405">Try logging into an account that is not a special profile.</span></span> <span data-ttu-id="a222d-406">Puede intentar cerrar la sesión y volver a iniciarla en la cuenta actual, o bien intentar iniciar sesión en una cuenta diferente.</span><span class="sxs-lookup"><span data-stu-id="a222d-406">You can try logging out and logging back into the current account, or try logging into a different account.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-407"><strong>ERROR_DEPLOYMENT_FAILED_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-407"><strong>ERROR_DEPLOYMENT_FAILED_</strong></span></span><br/> <span data-ttu-id="a222d-408"><strong>CONFLICTING_MUTABLE_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-408"><strong>CONFLICTING_MUTABLE_PACKAGE_</strong></span></span><br/> <span data-ttu-id="a222d-409"><strong>Active</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-409"><strong>DIRECTORY</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-410">0x80073D24</span><span class="sxs-lookup"><span data-stu-id="a222d-410">0x80073D24</span></span></td>
<td><span data-ttu-id="a222d-411">No se pudo realizar la operación de implementación debido a un <a href="/uwp/schemas/appxpackage/uapmanifestschema/element-desktop6-mutablepackagedirectory">Directorio de paquetes mutable</a>de un paquete conflictivo.</span><span class="sxs-lookup"><span data-stu-id="a222d-411">The deployment operation failed due to a conflicting package's <a href="/uwp/schemas/appxpackage/uapmanifestschema/element-desktop6-mutablepackagedirectory">mutable package directory</a>.</span></span> <span data-ttu-id="a222d-412">Para instalar este paquete, quite el paquete existente con el directorio de paquetes mutables en conflicto.</span><span class="sxs-lookup"><span data-stu-id="a222d-412">To install this package, remove the existing package with the conflicting mutable package directory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-413"><strong>ERROR_SINGLETON_RESOURCE_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-413"><strong>ERROR_SINGLETON_RESOURCE_</strong></span></span><br/> <span data-ttu-id="a222d-414"><strong>INSTALLED_IN_ACTIVE_USER</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-414"><strong>INSTALLED_IN_ACTIVE_USER</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-415">0x80073D25</span><span class="sxs-lookup"><span data-stu-id="a222d-415">0x80073D25</span></span></td>
<td><span data-ttu-id="a222d-416">No se pudo instalar el paquete porque se especificó un recurso singleton y otro usuario con ese paquete instalado inició sesión.</span><span class="sxs-lookup"><span data-stu-id="a222d-416">The package installation failed because a singleton resource was specified and another user with that package installed is logged in.</span></span> <span data-ttu-id="a222d-417">Asegúrese de que todos los usuarios activos con el paquete instalado estén desconectados y vuelva a intentar la instalación.</span><span class="sxs-lookup"><span data-stu-id="a222d-417">Make sure that all active users with the package installed are logged out and retry installation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-418">ERROR_DIFFERENT_VERSION_<strong></strong></span><span class="sxs-lookup"><span data-stu-id="a222d-418">ERROR_DIFFERENT_VERSION_<strong></strong></span></span><br/> <span data-ttu-id="a222d-419"><strong>OF_PACKAGED_SERVICE_INSTALLED</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-419"><strong>OF_PACKAGED_SERVICE_INSTALLED</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-420">0x80073D26</span><span class="sxs-lookup"><span data-stu-id="a222d-420">0x80073D26</span></span></td>
<td><span data-ttu-id="a222d-421">Error en la instalación del paquete porque hay instalada una versión diferente del servicio.</span><span class="sxs-lookup"><span data-stu-id="a222d-421">The package installation failed because a different version of the service is installed.</span></span> <span data-ttu-id="a222d-422">Intente instalar una versión más reciente del paquete.</span><span class="sxs-lookup"><span data-stu-id="a222d-422">Try installing a newer version of the package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-423"><strong>ERROR_SERVICE_EXISTS_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-423"><strong>ERROR_SERVICE_EXISTS_</strong></span></span><br/> <span data-ttu-id="a222d-424"><strong>AS_NON_PACKAGED_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-424"><strong>AS_NON_PACKAGED_SERVICE</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-425">0x80073D27</span><span class="sxs-lookup"><span data-stu-id="a222d-425">0x80073D27</span></span></td>
<td><span data-ttu-id="a222d-426">Error en la instalación del paquete porque existe una versión del servicio fuera de un paquete. msix/. appx.</span><span class="sxs-lookup"><span data-stu-id="a222d-426">The package installation failed because a version of the service exists outside of an .msix/.appx package.</span></span> <span data-ttu-id="a222d-427">Póngase en contacto con su proveedor de software.</span><span class="sxs-lookup"><span data-stu-id="a222d-427">Contact your software vendor.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-428"><strong>ERROR_PACKAGED_SERVICE_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-428"><strong>ERROR_PACKAGED_SERVICE_</strong></span></span><br/> <span data-ttu-id="a222d-429"><strong>REQUIRES_ADMIN_PRIVILEGES</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-429"><strong>REQUIRES_ADMIN_PRIVILEGES</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-430">0x80073D28</span><span class="sxs-lookup"><span data-stu-id="a222d-430">0x80073D28</span></span></td>
<td><span data-ttu-id="a222d-431">No se pudo instalar el paquete porque se necesitan privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="a222d-431">The package installation failed because administrator privileges are required.</span></span> <span data-ttu-id="a222d-432">Póngase en contacto con un administrador para instalar este paquete.</span><span class="sxs-lookup"><span data-stu-id="a222d-432">Contact an administrator to install this package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-433"><strong>ERROR_REDIRECTION_TO_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-433"><strong>ERROR_REDIRECTION_TO_</strong></span></span><br/> <span data-ttu-id="a222d-434"><strong>DEFAULT_ACCOUNT_NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-434"><strong>DEFAULT_ACCOUNT_NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-435">0x80073D29</span><span class="sxs-lookup"><span data-stu-id="a222d-435">0x80073D29</span></span></td>
<td><span data-ttu-id="a222d-436">Se produjo un error en la implementación del paquete porque la operación se habría redirigido a la cuenta predeterminada, cuando el autor de la llamada dijo que no lo haga.</span><span class="sxs-lookup"><span data-stu-id="a222d-436">The package deployment failed because the operation would have redirected to default account, when the caller said not to do so.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-437"><strong>ERROR_PACKAGE_LACKS_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-437"><strong>ERROR_PACKAGE_LACKS_</strong></span></span><br/> <span data-ttu-id="a222d-438"><strong>CAPABILITY_TO_DEPLOY_ON_HOST</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-438"><strong>CAPABILITY_TO_DEPLOY_ON_HOST</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-439">0x80073D2A</span><span class="sxs-lookup"><span data-stu-id="a222d-439">0x80073D2A</span></span></td>
<td><span data-ttu-id="a222d-440">No se pudo implementar el paquete porque el paquete requiere una funcionalidad para establecer como destino de forma nativa este host.</span><span class="sxs-lookup"><span data-stu-id="a222d-440">The package deployment failed because the package requires a capability to natively target this host.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-441"><strong>ERROR_UNSIGNED_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-441"><strong>ERROR_UNSIGNED_PACKAGE_</strong></span></span><br/> <span data-ttu-id="a222d-442"><strong>INVALID_CONTENT</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-442"><strong>INVALID_CONTENT</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-443">0x80073D2B</span><span class="sxs-lookup"><span data-stu-id="a222d-443">0x80073D2B</span></span></td>
<td><span data-ttu-id="a222d-444">No se pudo implementar el paquete porque su contenido no es válido para un paquete sin firmar.</span><span class="sxs-lookup"><span data-stu-id="a222d-444">The package deployment failed because its content is not valid for an unsigned package.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-445"><strong>ERROR_UNSIGNED_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-445"><strong>ERROR_UNSIGNED_PACKAGE_</strong></span></span><br/> <span data-ttu-id="a222d-446"><strong>INVALID_PUBLISHER_NAMESPACE</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-446"><strong>INVALID_PUBLISHER_NAMESPACE</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-447">0x80073D2C</span><span class="sxs-lookup"><span data-stu-id="a222d-447">0x80073D2C</span></span></td>
<td><span data-ttu-id="a222d-448">No se pudo implementar el paquete porque su publicador no está en el espacio de nombres sin firmar.</span><span class="sxs-lookup"><span data-stu-id="a222d-448">The package deployment failed because its publisher is not in the unsigned namespace.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-449"><strong>ERROR_SIGNED_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-449"><strong>ERROR_SIGNED_PACKAGE_</strong></span></span><br/> <span data-ttu-id="a222d-450"><strong>INVALID_PUBLISHER_NAMESPACE</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-450"><strong>INVALID_PUBLISHER_NAMESPACE</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-451">0x80073D2D</span><span class="sxs-lookup"><span data-stu-id="a222d-451">0x80073D2D</span></span></td>
<td><span data-ttu-id="a222d-452">No se pudo implementar el paquete porque su publicador no está en el espacio de nombres firmado.</span><span class="sxs-lookup"><span data-stu-id="a222d-452">The package deployment failed because its publisher is not in the signed namespace.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-453"><strong>ERROR_PACKAGE_EXTERNAL_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-453"><strong>ERROR_PACKAGE_EXTERNAL_</strong></span></span><br/> <span data-ttu-id="a222d-454"><strong>LOCATION_NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-454"><strong>LOCATION_NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-455">0x80073D2E</span><span class="sxs-lookup"><span data-stu-id="a222d-455">0x80073D2E</span></span></td>
<td><span data-ttu-id="a222d-456">No se pudo implementar el paquete porque su publicador no está en el espacio de nombres firmado.</span><span class="sxs-lookup"><span data-stu-id="a222d-456">The package deployment failed because its publisher is not in the signed namespace.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-457"><strong>ERROR_INSTALL_FULLTRUST_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-457"><strong>ERROR_INSTALL_FULLTRUST_</strong></span></span><br/> <span data-ttu-id="a222d-458"><strong>HOSTRUNTIME_REQUIRES_MAIN_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-458"><strong>HOSTRUNTIME_REQUIRES_MAIN_</strong></span></span><br/> <span data-ttu-id="a222d-459"><strong>PACKAGE_FULLTRUST_CAPABILITY</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-459"><strong>PACKAGE_FULLTRUST_CAPABILITY</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-460">0x80073D2F</span><span class="sxs-lookup"><span data-stu-id="a222d-460">0x80073D2F</span></span></td>
<td><span data-ttu-id="a222d-461">Una dependencia de tiempo de ejecución de host que se resuelve en un paquete con contenido de plena confianza requiere que el paquete principal tenga la funcionalidad <strong>runFullTrust</strong> .</span><span class="sxs-lookup"><span data-stu-id="a222d-461">A host runtime dependency resolving to a package with full trust content requires the main package to have the <strong>runFullTrust</strong> capability.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-462"><strong>APPX_E_PACKAGING_INTERNAL</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-462"><strong>APPX_E_PACKAGING_INTERNAL</strong></span></span></td>
<td><span data-ttu-id="a222d-463">0x80080200</span><span class="sxs-lookup"><span data-stu-id="a222d-463">0x80080200</span></span></td>
<td><span data-ttu-id="a222d-464">La API de empaquetado encontró un error interno.</span><span class="sxs-lookup"><span data-stu-id="a222d-464">The packaging API has encountered an internal error.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-465"><strong>APPX_E_INTERLEAVING_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-465"><strong>APPX_E_INTERLEAVING_</strong></span></span><br/> <span data-ttu-id="a222d-466"><strong>NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-466"><strong>NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-467">0x80080201</span><span class="sxs-lookup"><span data-stu-id="a222d-467">0x80080201</span></span></td>
<td><span data-ttu-id="a222d-468">El paquete no es válido porque su contenido está intercalado.</span><span class="sxs-lookup"><span data-stu-id="a222d-468">The package isn't valid because its contents are interleaved.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-469"><strong>APPX_E_RELATIONSHIPS_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-469"><strong>APPX_E_RELATIONSHIPS_</strong></span></span><br/> <span data-ttu-id="a222d-470"><strong>NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-470"><strong>NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-471">0x80080202</span><span class="sxs-lookup"><span data-stu-id="a222d-471">0x80080202</span></span></td>
<td><span data-ttu-id="a222d-472">El paquete no es válido porque contiene relaciones OPC.</span><span class="sxs-lookup"><span data-stu-id="a222d-472">The package isn't valid because it contains OPC relationships.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-473"><strong>APPX_E_MISSING_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-473"><strong>APPX_E_MISSING_</strong></span></span><br/> <span data-ttu-id="a222d-474"><strong>REQUIRED_FILE</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-474"><strong>REQUIRED_FILE</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-475">0x80080203</span><span class="sxs-lookup"><span data-stu-id="a222d-475">0x80080203</span></span></td>
<td><span data-ttu-id="a222d-476">El paquete no es válido porque falta un manifiesto o una asignación de bloque, o bien hay un archivo de integridad de código, pero falta un archivo de signatura.</span><span class="sxs-lookup"><span data-stu-id="a222d-476">The package isn't valid because it's missing a manifest or block map, or a code integrity file is present but a signature file is missing.</span></span><br/> <span data-ttu-id="a222d-477">Asegúrese de que el paquete no tiene uno o varios de estos archivos necesarios:</span><span class="sxs-lookup"><span data-stu-id="a222d-477">Ensure that the package isn't missing one or more of these required files:</span></span><br/>
<ul>
<li><span data-ttu-id="a222d-478">\AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="a222d-478">\AppxManifest.xml</span></span></li>
<li><span data-ttu-id="a222d-479">\AppxBlockMap.xml</span><span class="sxs-lookup"><span data-stu-id="a222d-479">\AppxBlockMap.xml</span></span></li>
</ul>
<span data-ttu-id="a222d-480">Si el paquete contiene \AppxMetadata\CodeIntegrity.cat, también debe contener \AppxSignature.p7x.</span><span class="sxs-lookup"><span data-stu-id="a222d-480">If the package contains \AppxMetadata\CodeIntegrity.cat, it must also contain \AppxSignature.p7x.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-481"><strong>APPX_E_INVALID_MANIFEST</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-481"><strong>APPX_E_INVALID_MANIFEST</strong></span></span></td>
<td><span data-ttu-id="a222d-482">0x80080204</span><span class="sxs-lookup"><span data-stu-id="a222d-482">0x80080204</span></span></td>
<td><span data-ttu-id="a222d-483">El archivo de AppxManifest.xml del paquete no es válido.</span><span class="sxs-lookup"><span data-stu-id="a222d-483">The package's AppxManifest.xml file isn't valid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-484"><strong>APPX_E_INVALID_BLOCKMAP</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-484"><strong>APPX_E_INVALID_BLOCKMAP</strong></span></span></td>
<td><span data-ttu-id="a222d-485">0x80080205</span><span class="sxs-lookup"><span data-stu-id="a222d-485">0x80080205</span></span></td>
<td><span data-ttu-id="a222d-486">El archivo de AppxBlockMap.xml del paquete no es válido.</span><span class="sxs-lookup"><span data-stu-id="a222d-486">The package's AppxBlockMap.xml file isn't valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-487"><strong>APPX_E_CORRUPT_CONTENT</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-487"><strong>APPX_E_CORRUPT_CONTENT</strong></span></span></td>
<td><span data-ttu-id="a222d-488">0x80080206</span><span class="sxs-lookup"><span data-stu-id="a222d-488">0x80080206</span></span></td>
<td><span data-ttu-id="a222d-489">No se puede leer el contenido del paquete porque está dañado.</span><span class="sxs-lookup"><span data-stu-id="a222d-489">The package contents can't be read because it's corrupted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-490"><strong>APPX_E_BLOCK_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-490"><strong>APPX_E_BLOCK_</strong></span></span><br/> <span data-ttu-id="a222d-491"><strong>HASH_INVALID</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-491"><strong>HASH_INVALID</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-492">0x80080207</span><span class="sxs-lookup"><span data-stu-id="a222d-492">0x80080207</span></span></td>
<td><span data-ttu-id="a222d-493">El valor hash calculado del bloque no coincide con el valor que tiene almacenado en la asignación de bloques.</span><span class="sxs-lookup"><span data-stu-id="a222d-493">The computed hash value of the block doesn't match the has value stored in the block map.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-494"><strong>APPX_E_REQUESTED_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-494"><strong>APPX_E_REQUESTED_</strong></span></span><br/> <span data-ttu-id="a222d-495"><strong>RANGE_TOO_LARGE</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-495"><strong>RANGE_TOO_LARGE</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-496">0x80080208</span><span class="sxs-lookup"><span data-stu-id="a222d-496">0x80080208</span></span></td>
<td><span data-ttu-id="a222d-497">El intervalo de bytes solicitado es superior a 4 GB cuando se traduce a un intervalo de bytes de bloques.</span><span class="sxs-lookup"><span data-stu-id="a222d-497">The requested byte range is over 4 GB when translated to a byte range of blocks.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-498"><strong>TRUST_E_NOSIGNATURE</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-498"><strong>TRUST_E_NOSIGNATURE</strong></span></span></td>
<td><span data-ttu-id="a222d-499">0x800B0100</span><span class="sxs-lookup"><span data-stu-id="a222d-499">0x800B0100</span></span></td>
<td><span data-ttu-id="a222d-500">No hay ninguna firma presente en el asunto.</span><span class="sxs-lookup"><span data-stu-id="a222d-500">No signature is present in the subject.</span></span><br/> <span data-ttu-id="a222d-501">Este error puede aparecer si el paquete no está firmado o la firma no es válida.</span><span class="sxs-lookup"><span data-stu-id="a222d-501">You may get this error if the package is unsigned or the signature isn't valid.</span></span> <span data-ttu-id="a222d-502">El paquete debe estar firmado para implementarse.</span><span class="sxs-lookup"><span data-stu-id="a222d-502">The package must be signed to be deployed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-503"><strong>CERT_E_UNTRUSTEDROOT</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-503"><strong>CERT_E_UNTRUSTEDROOT</strong></span></span></td>
<td><span data-ttu-id="a222d-504">0x800B0109</span><span class="sxs-lookup"><span data-stu-id="a222d-504">0x800B0109</span></span></td>
<td><span data-ttu-id="a222d-505">Una cadena de certificados procesada, pero termina en un certificado raíz que no es de confianza para el proveedor de confianza.</span><span class="sxs-lookup"><span data-stu-id="a222d-505">A certificate chain processed, but terminated in a root certificate which isn't trusted by the trust provider.</span></span><br/> <span data-ttu-id="a222d-506">Vea <a href="/previous-versions/br230260(v=vs.110)">firmar un paquete</a>.</span><span class="sxs-lookup"><span data-stu-id="a222d-506">See <a href="/previous-versions/br230260(v=vs.110)">Signing a package</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-507"><strong>CERT_E_CHAINING</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-507"><strong>CERT_E_CHAINING</strong></span></span></td>
<td><span data-ttu-id="a222d-508">0x800B010A</span><span class="sxs-lookup"><span data-stu-id="a222d-508">0x800B010A</span></span></td>
<td><span data-ttu-id="a222d-509">No se pudo crear una cadena de certificados en una entidad de certificación raíz de confianza.</span><span class="sxs-lookup"><span data-stu-id="a222d-509">A certificate chain couldn't be built to a trusted root certification authority.</span></span><br/> <span data-ttu-id="a222d-510">Vea <a href="/previous-versions/br230260(v=vs.110)">firmar un paquete</a>.</span><span class="sxs-lookup"><span data-stu-id="a222d-510">See <a href="/previous-versions/br230260(v=vs.110)">Signing a package</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-511"><strong>APPX_E_INVALID_</strong> </span><span class="sxs-lookup"><span data-stu-id="a222d-511"><strong>APPX_E_INVALID_</strong> </span></span><br/> <span data-ttu-id="a222d-512"><strong>SIP_CLIENT_DATA</strong> </span><span class="sxs-lookup"><span data-stu-id="a222d-512"><strong>SIP_CLIENT_DATA</strong> </span></span><br/></td>
<td><span data-ttu-id="a222d-513">0x80080209</span><span class="sxs-lookup"><span data-stu-id="a222d-513">0x80080209</span></span></td>
<td><span data-ttu-id="a222d-514">La estructura de <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO</strong></a>utilizada para firmar el paquete no contiene los datos necesarios</span><span class="sxs-lookup"><span data-stu-id="a222d-514">The <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO</strong></a>structure used to sign the package didn't contain the required data</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-515"><strong>APPX_E_INVALID_</strong> </span><span class="sxs-lookup"><span data-stu-id="a222d-515"><strong>APPX_E_INVALID_</strong> </span></span><br/> <span data-ttu-id="a222d-516"><strong>KEY_INFO</strong> </span><span class="sxs-lookup"><span data-stu-id="a222d-516"><strong>KEY_INFO</strong> </span></span><br/></td>
<td><span data-ttu-id="a222d-517">0x8008020A</span><span class="sxs-lookup"><span data-stu-id="a222d-517">0x8008020A</span></span></td>
<td><span data-ttu-id="a222d-518">La estructura de <a href="/windows/win32/api/appxpackaging/ns-appxpackaging-appx_key_info"><strong>APPX_KEY_INFO</strong></a> utilizada para cifrar o descifrar el paquete contiene datos no válidos.</span><span class="sxs-lookup"><span data-stu-id="a222d-518">The <a href="/windows/win32/api/appxpackaging/ns-appxpackaging-appx_key_info"><strong>APPX_KEY_INFO</strong></a> structure used to encrypt or decrypt the package contains invalid data.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-519"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-519"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="a222d-520"><strong>CONTENTGROUPMAP</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-520"><strong>CONTENTGROUPMAP</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-521">0x8008020B</span><span class="sxs-lookup"><span data-stu-id="a222d-521">0x8008020B</span></span></td>
<td><span data-ttu-id="a222d-522">El mapa del grupo de contenido del paquete. msix/. appx no es válido.</span><span class="sxs-lookup"><span data-stu-id="a222d-522">The .msix/.appx package's content group map is invalid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-523"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-523"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="a222d-524"><strong>APPINSTALLER</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-524"><strong>APPINSTALLER</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-525">0x8008020C</span><span class="sxs-lookup"><span data-stu-id="a222d-525">0x8008020C</span></span></td>
<td><span data-ttu-id="a222d-526">El <a href="/windows/msix/app-installer/app-installer-root">archivo. AppInstaller</a> para el paquete no es válido.</span><span class="sxs-lookup"><span data-stu-id="a222d-526">The <a href="/windows/msix/app-installer/app-installer-root">.appinstaller file</a> for the package is invalid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-527"><strong>APPX_E_DELTA_BASELINE_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-527"><strong>APPX_E_DELTA_BASELINE_</strong></span></span><br/> <span data-ttu-id="a222d-528"><strong>VERSION_MISMATCH</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-528"><strong>VERSION_MISMATCH</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-529">0x8008020D</span><span class="sxs-lookup"><span data-stu-id="a222d-529">0x8008020D</span></span></td>
<td><span data-ttu-id="a222d-530">La versión del paquete de línea de base en el paquete Delta no coincide con la versión del paquete de base de referencia que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="a222d-530">The baseline package version in delta package does not match the version in the baseline package to be updated.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-531"><strong>APPX_E_DELTA_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-531"><strong>APPX_E_DELTA_PACKAGE_</strong></span></span><br/> <span data-ttu-id="a222d-532"><strong>MISSING_FILE</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-532"><strong>MISSING_FILE</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-533">0x8008020E</span><span class="sxs-lookup"><span data-stu-id="a222d-533">0x8008020E</span></span></td>
<td><span data-ttu-id="a222d-534">Falta un archivo en el paquete Delta del paquete actualizado.</span><span class="sxs-lookup"><span data-stu-id="a222d-534">The delta package is missing a file from the updated package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-535"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-535"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="a222d-536"><strong>DELTA_PACKAGE</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-536"><strong>DELTA_PACKAGE</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-537">0x8008020F</span><span class="sxs-lookup"><span data-stu-id="a222d-537">0x8008020F</span></span></td>
<td><span data-ttu-id="a222d-538">El paquete Delta no es válido.</span><span class="sxs-lookup"><span data-stu-id="a222d-538">The delta package is invalid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-539"><strong>APPX_E_DELTA_APPENDED_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-539"><strong>APPX_E_DELTA_APPENDED_</strong></span></span><br/> <span data-ttu-id="a222d-540"><strong>PACKAGE_NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-540"><strong>PACKAGE_NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-541">0x80080210</span><span class="sxs-lookup"><span data-stu-id="a222d-541">0x80080210</span></span></td>
<td><span data-ttu-id="a222d-542">No se permite el paquete Delta anexado para la operación actual.</span><span class="sxs-lookup"><span data-stu-id="a222d-542">The delta appended package is not allowed for the current operation.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-543"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-543"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="a222d-544"><strong>PACKAGING_LAYOUT</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-544"><strong>PACKAGING_LAYOUT</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-545">0x80080211</span><span class="sxs-lookup"><span data-stu-id="a222d-545">0x80080211</span></span></td>
<td><span data-ttu-id="a222d-546">El archivo de diseño de empaquetado no es válido.</span><span class="sxs-lookup"><span data-stu-id="a222d-546">The packaging layout file is invalid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-547"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-547"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="a222d-548"><strong>PACKAGESIGNCONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-548"><strong>PACKAGESIGNCONFIG</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-549">0x80080212</span><span class="sxs-lookup"><span data-stu-id="a222d-549">0x80080212</span></span></td>
<td><span data-ttu-id="a222d-550">El archivo packageSignConfig no es válido.</span><span class="sxs-lookup"><span data-stu-id="a222d-550">The packageSignConfig file is invalid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-551"><strong>APPX_E_RESOURCESPRI_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-551"><strong>APPX_E_RESOURCESPRI_</strong></span></span><br/> <span data-ttu-id="a222d-552"><strong>NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-552"><strong>NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-553">0x80080213</span><span class="sxs-lookup"><span data-stu-id="a222d-553">0x80080213</span></span></td>
<td><span data-ttu-id="a222d-554">No se permite el archivo resources. PRI cuando no hay elementos de recursos en el manifiesto del paquete.</span><span class="sxs-lookup"><span data-stu-id="a222d-554">The resources.pri file is not allowed when there are no resource elements in the package manifest.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-555"><strong>APPX_E_FILE_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-555"><strong>APPX_E_FILE_</strong></span></span><br/> <span data-ttu-id="a222d-556"><strong>COMPRESSION_MISMATCH</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-556"><strong>COMPRESSION_MISMATCH</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-557">0x80080214</span><span class="sxs-lookup"><span data-stu-id="a222d-557">0x80080214</span></span></td>
<td><span data-ttu-id="a222d-558">El estado de compresión del archivo en la línea base y el paquete actualizado no coincide.</span><span class="sxs-lookup"><span data-stu-id="a222d-558">The compression state of file in baseline and updated package does not match.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a222d-559"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-559"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="a222d-560"><strong>PAYLOAD_PACKAGE_EXTENSION</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-560"><strong>PAYLOAD_PACKAGE_EXTENSION</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-561">0x80080215</span><span class="sxs-lookup"><span data-stu-id="a222d-561">0x80080215</span></span></td>
<td><span data-ttu-id="a222d-562">No se permiten extensiones no. appx para paquetes de carga destinados a plataformas anteriores.</span><span class="sxs-lookup"><span data-stu-id="a222d-562">Non .appx extensions are not allowed for payload packages targeting older platforms.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a222d-563"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-563"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="a222d-564"><strong>ENCRYPTION_EXCLUSION_FILE_LIST</strong></span><span class="sxs-lookup"><span data-stu-id="a222d-564"><strong>ENCRYPTION_EXCLUSION_FILE_LIST</strong></span></span><br/></td>
<td><span data-ttu-id="a222d-565">0x80080216</span><span class="sxs-lookup"><span data-stu-id="a222d-565">0x80080216</span></span></td>
<td><span data-ttu-id="a222d-566">El archivo encryptionExclusionFileList no es válido.</span><span class="sxs-lookup"><span data-stu-id="a222d-566">The encryptionExclusionFileList file is invalid.</span></span><br/></td>
</tr>
</tbody>
</table>

## <a name="applications-dont-start-and-their-names-are-dimmed"></a><span data-ttu-id="a222d-567">Las aplicaciones no se inician y sus nombres están atenuados</span><span class="sxs-lookup"><span data-stu-id="a222d-567">Applications don't start and their names are dimmed</span></span>

<span data-ttu-id="a222d-568">En un equipo basado en Windows 10, no se pueden iniciar algunas aplicaciones y los nombres de las aplicaciones aparecen atenuados.</span><span class="sxs-lookup"><span data-stu-id="a222d-568">On a Windows 10-based computer, you cannot start some applications, and the application names appear dimmed.</span></span>

![Algunos nombres de aplicaciones aparecen atenuados en el menú Inicio](./images/app-names-dimmed.png)

<span data-ttu-id="a222d-570">Al intentar abrir una aplicación seleccionando el nombre atenuado, puede recibir uno de los siguientes mensajes de error:</span><span class="sxs-lookup"><span data-stu-id="a222d-570">When you try to open an application by selecting the dimmed name, you may receive one of the following error messages:</span></span>

> <span data-ttu-id="a222d-571">Hay un problema con \<*application name*> .</span><span class="sxs-lookup"><span data-stu-id="a222d-571">There's a problem with \<*application name*>.</span></span> <span data-ttu-id="a222d-572">Póngase en contacto con el administrador del sistema para repararlo o reinstalarlo.</span><span class="sxs-lookup"><span data-stu-id="a222d-572">Contact your system administrator about repairing or reinstalling it</span></span>  
> <span data-ttu-id="a222d-573">Error: esta aplicación no se puede abrir</span><span class="sxs-lookup"><span data-stu-id="a222d-573">Error: This app can't open</span></span>

<span data-ttu-id="a222d-574">Además, las siguientes entradas de eventos se registran en el registro "Microsoft-Windows-TWinUI/Operational" en **Applications and Services\Microsoft\Windows\Apps**:</span><span class="sxs-lookup"><span data-stu-id="a222d-574">Additionally, the following event entries are logged in the "Microsoft-Windows-TWinUI/Operational" log under **Applications and Services\Microsoft\Windows\Apps**:</span></span>

> <span data-ttu-id="a222d-575">Nombre de registro: Microsoft-Windows-TWinUI/Operational</span><span class="sxs-lookup"><span data-stu-id="a222d-575">Log Name: Microsoft-Windows-TWinUI/Operational</span></span>  
> <span data-ttu-id="a222d-576">Origen: Microsoft-Windows-inmersivo-Shell</span><span class="sxs-lookup"><span data-stu-id="a222d-576">Source: Microsoft-Windows-Immersive-Shell</span></span>  
> <span data-ttu-id="a222d-577">Fecha: <*fecha*></span><span class="sxs-lookup"><span data-stu-id="a222d-577">Date: <*date*></span></span>  
> <span data-ttu-id="a222d-578">ID. de evento: 5960</span><span class="sxs-lookup"><span data-stu-id="a222d-578">Event ID: 5960</span></span>  
> <span data-ttu-id="a222d-579">Categoría de tarea: (5960)</span><span class="sxs-lookup"><span data-stu-id="a222d-579">Task Category: (5960)</span></span>  
> <span data-ttu-id="a222d-580">Nivel: error</span><span class="sxs-lookup"><span data-stu-id="a222d-580">Level: Error</span></span>  
> <span data-ttu-id="a222d-581">Palabras clave:</span><span class="sxs-lookup"><span data-stu-id="a222d-581">Keywords:</span></span>  
> <span data-ttu-id="a222d-582">Descripción:</span><span class="sxs-lookup"><span data-stu-id="a222d-582">Description:</span></span>  
> <span data-ttu-id="a222d-583">La activación del Microsoft.BingNews_8wekyb3d8bbwe de la aplicación. AppexNews para Windows.</span><span class="sxs-lookup"><span data-stu-id="a222d-583">Activation of the app Microsoft.BingNews_8wekyb3d8bbwe!AppexNews for the Windows.</span></span> <span data-ttu-id="a222d-584">El contrato de inicio se bloqueó con el error 0x80073CFC porque su paquete se encuentra en estado: modificado.</span><span class="sxs-lookup"><span data-stu-id="a222d-584">Launch contract was blocked with error 0x80073CFC because its package is in state: Modified.</span></span>  

### <a name="cause"></a><span data-ttu-id="a222d-585">Causa</span><span class="sxs-lookup"><span data-stu-id="a222d-585">Cause</span></span>

<span data-ttu-id="a222d-586">Este problema se produce porque se modificó la entrada del registro para el valor de estado del paquete correspondiente de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a222d-586">This issue occurs because the registry entry for the status value of application's corresponding package was modified.</span></span>

### <a name="resolution"></a><span data-ttu-id="a222d-587">Solución</span><span class="sxs-lookup"><span data-stu-id="a222d-587">Resolution</span></span>

> [!WARNING]
> <span data-ttu-id="a222d-588">Pueden producirse problemas graves si modifica el registro de manera incorrecta mediante el Editor del Registro u otro método.</span><span class="sxs-lookup"><span data-stu-id="a222d-588">Serious problems might occur if you modify the registry incorrectly by using Registry Editor or by using another method.</span></span> <span data-ttu-id="a222d-589">Estos problemas pueden requerir que tenga que volver a instalar el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a222d-589">These problems might require that you reinstall the operating system.</span></span> <span data-ttu-id="a222d-590">Microsoft no brinda ninguna garantía de que se puedan solucionar estos problemas.</span><span class="sxs-lookup"><span data-stu-id="a222d-590">Microsoft cannot guarantee that these problems can be solved.</span></span> <span data-ttu-id="a222d-591">Modifique el registro bajo su responsabilidad.</span><span class="sxs-lookup"><span data-stu-id="a222d-591">Modify the registry at your own risk.</span></span>

<span data-ttu-id="a222d-592">Para corregir este problema:</span><span class="sxs-lookup"><span data-stu-id="a222d-592">To fix this issue:</span></span>

1. <span data-ttu-id="a222d-593">Inicie el editor del registro y, a continuación, busque la subclave **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList** .</span><span class="sxs-lookup"><span data-stu-id="a222d-593">Start Registry Editor, and then locate the **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList** subkey.</span></span>
2. <span data-ttu-id="a222d-594">Para hacer una copia de seguridad de los datos de la subclave, haga clic con el botón secundario en **PackageList**, seleccione **exportar** y, a continuación, guarde los datos como un archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="a222d-594">To back up the subkey data, right-click **PackageList**, select **Export**, and then save the data as a registry file.</span></span>
3. <span data-ttu-id="a222d-595">Para cada una de las aplicaciones que se enumeran en las entradas de registro de ID. de evento 5960, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="a222d-595">For each of the applications that are listed in the Event ID 5960 log entries, follow these steps:</span></span>  
   1. <span data-ttu-id="a222d-596">Busque la entrada **PackageStatus** .</span><span class="sxs-lookup"><span data-stu-id="a222d-596">Locate the **PackageStatus** entry.</span></span>
   2. <span data-ttu-id="a222d-597">Establezca el valor de **PackageStatus** en cero (**0**).</span><span class="sxs-lookup"><span data-stu-id="a222d-597">Set the value of **PackageStatus** to zero (**0**).</span></span>
   > [!NOTE]  
   > <span data-ttu-id="a222d-598">Si no hay ninguna entrada para la aplicación en **PackageList**, el problema tiene alguna otra causa.</span><span class="sxs-lookup"><span data-stu-id="a222d-598">If there are no entries for the application under **PackageList**, then the issue has some other cause.</span></span> <span data-ttu-id="a222d-599">En el caso del evento de ejemplo de este artículo, la subclave completa es **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList\Microsoft.BingNews_8wekyb3d8bbwe!AppexNews\PackageStatus**</span><span class="sxs-lookup"><span data-stu-id="a222d-599">In the case of the example event in this article, the full subkey is **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList\Microsoft.BingNews_8wekyb3d8bbwe!AppexNews\PackageStatus**</span></span>
4. <span data-ttu-id="a222d-600">Reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="a222d-600">Restart the computer.</span></span>

## <a name="get-additional-help"></a><span data-ttu-id="a222d-601">Obtener ayuda adicional</span><span class="sxs-lookup"><span data-stu-id="a222d-601">Get additional help</span></span>

<span data-ttu-id="a222d-602">Si necesita más ayuda con la resolución de un problema que está experimentando al empaquetar, implementar o consultar un paquete de aplicación de Windows (. msix/. appx) como desarrollador, consulte estos recursos de soporte técnico para desarrolladores adicionales.</span><span class="sxs-lookup"><span data-stu-id="a222d-602">If you need further help with resolving a problem you are experience when packaging, deploying, or querying a Windows app package (.msix/.appx) as a developer, refer to these additional developer support resources.</span></span>

- <span data-ttu-id="a222d-603">[Microsoft Q&a](/answers/topics/uwp.html?filter=all&sort=active) ofrece respuestas pertinentes y oportunas a sus problemas técnicos de una comunidad de expertos y ingenieros de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a222d-603">[Microsoft Q&A](/answers/topics/uwp.html?filter=all&sort=active) offers relevant and timely answers to your technical problems from a community of experts and Microsoft engineers.</span></span>
- <span data-ttu-id="a222d-604">Para obtener ayuda de la comunidad con preguntas de desarrollo, existen nuestros [foros](https://social.msdn.microsoft.com/Forums/newthread?category=windowsapps&forum=wpdevelop&prof=required)y [stackoverflow](https://stackoverflow.com/questions).</span><span class="sxs-lookup"><span data-stu-id="a222d-604">For community assistance with development questions, there are our [forums](https://social.msdn.microsoft.com/Forums/newthread?category=windowsapps&forum=wpdevelop&prof=required), and [StackOverflow](https://stackoverflow.com/questions).</span></span>
- <span data-ttu-id="a222d-605">El sitio de [soporte técnico para desarrolladores de Windows](https://developer.microsoft.com/windows/support) explica otras opciones de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="a222d-605">The [Windows developer support](https://developer.microsoft.com/windows/support) site explains other support options.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a222d-606">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a222d-606">Related topics</span></span>

- <span data-ttu-id="a222d-607">[How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md) (Cómo firmar un paquete de la aplicación con SignTool)</span><span class="sxs-lookup"><span data-stu-id="a222d-607">[How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md)</span></span>
- [<span data-ttu-id="a222d-608">Cómo solucionar errores de firma de paquete de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="a222d-608">How to troubleshoot app package signature errors</span></span>](how-to-troubleshoot-app-package-signature-errors.md)
