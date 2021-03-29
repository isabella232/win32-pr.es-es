---
description: En el ejemplo de scripting de este tema se muestra cómo usar el agente de Windows Update (WUA) para examinar, descargar e instalar una actualización específica. La actualización puede especificarse por su título.
ms.assetid: 4a5bb920-fc51-48a0-8f66-bb2fcc72589f
title: Búsqueda, descarga e instalación de actualizaciones específicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aadd7903303356c3937f41e44aa7a47e71192409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360360"
---
# <a name="searching-downloading-and-installing-specific-updates"></a><span data-ttu-id="cab0b-104">Búsqueda, descarga e instalación de actualizaciones específicas</span><span class="sxs-lookup"><span data-stu-id="cab0b-104">Searching, Downloading, and Installing Specific Updates</span></span>

<span data-ttu-id="cab0b-105">En el ejemplo de scripting de este tema se muestra cómo usar el agente de Windows Update (WUA) para examinar, descargar e instalar una actualización específica.</span><span class="sxs-lookup"><span data-stu-id="cab0b-105">The scripting sample in this topic shows you how to use the Windows Update Agent (WUA) to scan, download, and install a specific update.</span></span> <span data-ttu-id="cab0b-106">La actualización puede especificarse por su título.</span><span class="sxs-lookup"><span data-stu-id="cab0b-106">The update can be specified by its title.</span></span>

<span data-ttu-id="cab0b-107">El ejemplo busca una actualización de software específica, descarga la actualización y, a continuación, instala la actualización.</span><span class="sxs-lookup"><span data-stu-id="cab0b-107">The sample searches for a specific software update, downloads the update, and then installs the update.</span></span> <span data-ttu-id="cab0b-108">Por ejemplo, un usuario puede usar este método para determinar si una actualización de seguridad crítica está instalada en un equipo.</span><span class="sxs-lookup"><span data-stu-id="cab0b-108">For example, a user can use this method to determine if a critical security update is installed on a computer.</span></span> <span data-ttu-id="cab0b-109">Si la actualización no está instalada, el usuario puede asegurarse de que se ha descargado e instalado la actualización.</span><span class="sxs-lookup"><span data-stu-id="cab0b-109">If the update isn't installed, the user can ensure that the update is downloaded and installed.</span></span> <span data-ttu-id="cab0b-110">El usuario también puede asegurarse de que se le notifique el estado de la instalación.</span><span class="sxs-lookup"><span data-stu-id="cab0b-110">The user can also ensure that they are notified about the status of the installation.</span></span>

<span data-ttu-id="cab0b-111">La actualización de ejemplo se identifica mediante el título de la actualización en la [**propiedad title de IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title).</span><span class="sxs-lookup"><span data-stu-id="cab0b-111">The sample update is identified by the update title in [**Title Property of IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title).</span></span> <span data-ttu-id="cab0b-112">El título de la actualización que se sugiere en este ejemplo es "Update for Windows Rights Management Client 1,0."</span><span class="sxs-lookup"><span data-stu-id="cab0b-112">The title of the update that is suggested in this sample is "Update for Windows Rights Management client 1.0."</span></span>

> [!Note]  
> <span data-ttu-id="cab0b-113">Para obtener información sobre cómo buscar, descargar e instalar todas las actualizaciones que se aplican a una aplicación específica, vea [Buscar, descargar e instalar actualizaciones](searching--downloading--and-installing-updates.md).</span><span class="sxs-lookup"><span data-stu-id="cab0b-113">For info about how to search, download, and install all the updates that apply to a specific application, see [Searching, Downloading, and Installing Updates](searching--downloading--and-installing-updates.md).</span></span>

 

<span data-ttu-id="cab0b-114">Antes de intentar ejecutar este ejemplo, tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cab0b-114">Before you attempt to run this sample, note the following:</span></span>

-   <span data-ttu-id="cab0b-115">WUA debe estar instalado en el equipo.</span><span class="sxs-lookup"><span data-stu-id="cab0b-115">WUA must be installed on the computer.</span></span> <span data-ttu-id="cab0b-116">Para obtener más información sobre cómo determinar la versión de WUA que está instalada, vea [determinar la versión actual de WUA](determining-the-current-version-of-wua.md).</span><span class="sxs-lookup"><span data-stu-id="cab0b-116">For more info about how to determine the version of WUA that is installed, see [Determining the Current Version of WUA](determining-the-current-version-of-wua.md).</span></span>
-   <span data-ttu-id="cab0b-117">El ejemplo no proporciona su propia interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="cab0b-117">The sample doesn't provide its own user interface.</span></span> <span data-ttu-id="cab0b-118">WUA solicita al usuario que reinicie el equipo si una actualización requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="cab0b-118">WUA prompts the user to restart the computer if an update requires a restart.</span></span>
-   <span data-ttu-id="cab0b-119">El ejemplo solo puede descargar actualizaciones de WUA.</span><span class="sxs-lookup"><span data-stu-id="cab0b-119">The sample can download updates only from WUA.</span></span> <span data-ttu-id="cab0b-120">No puede descargar actualizaciones de un servidor de servicios de actualización de software (SUS) 1,0.</span><span class="sxs-lookup"><span data-stu-id="cab0b-120">It can't download updates from a Software Update Services (SUS) 1.0 server.</span></span>
-   <span data-ttu-id="cab0b-121">La ejecución de este ejemplo requiere Windows Script Host (WSH).</span><span class="sxs-lookup"><span data-stu-id="cab0b-121">Running this sample requires Windows Script Host (WSH).</span></span> <span data-ttu-id="cab0b-122">Para obtener más información acerca de WSH, consulte la sección WSH del kit de desarrollo de software (SDK) de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="cab0b-122">For more info about WSH, see the WSH section of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="cab0b-123">Si el ejemplo se copia en un archivo denominado WUA \_SpecificUpdate.vbs, puede ejecutarlo abriendo una ventana del símbolo del sistema y escribiendo este comando: **cscript WUA \_SpecificUpdate.vbs**</span><span class="sxs-lookup"><span data-stu-id="cab0b-123">If the sample is copied to a file named WUA\_SpecificUpdate.vbs, you can run it by opening a Command Prompt window and by typing this command: **cscript WUA\_SpecificUpdate.vbs**</span></span>  
    

## <a name="example"></a><span data-ttu-id="cab0b-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cab0b-124">Example</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cab0b-125">Este script está pensado para demostrar el uso de las API del agente de Windows Update y proporcionar un ejemplo de cómo los desarrolladores pueden usar estas API para resolver los problemas.</span><span class="sxs-lookup"><span data-stu-id="cab0b-125">This script is intended to demonstrate the use of the Windows Update Agent APIs, and provide an example of how developers can use these APIs to solve problems.</span></span> <span data-ttu-id="cab0b-126">Este script no está pensado como código de producción y Microsoft no admite el propio script (aunque se admiten las API del agente de Windows Update subyacentes).</span><span class="sxs-lookup"><span data-stu-id="cab0b-126">This script is not intended as production code, and the script itself is not supported by Microsoft (though the underlying Windows Update Agent APIs are supported).</span></span>

 


```VB
Set updateSession = CreateObject("Microsoft.Update.Session")
updateSession.ClientApplicationID = "MSDN Sample Script"

'Get update title to search for
WScript.Echo "Enter the title of the update: " & _
"(for example, Update for Windows Rights Management client 1.0)"
updateTitle = WScript.StdIn.Readline

WScript.Echo vbCRLF & "Searching for: " & updateTitle & "..."

Set updateSearcher = updateSession.CreateupdateSearcher()

'Search for all software updates, already installed and not installed
Set searchResult = _
updateSearcher.Search("Type='Software'")

Set updateToInstall = CreateObject("Microsoft.Update.UpdateColl")

updateIsApplicable = False

'Cycle through search results to look for the update title
For i = 0 To searchResult.Updates.Count-1
   Set update = searchResult.Updates.Item(i)
   If UCase(update.Title) = UCase(updateTitle) Then
   'Update in list of applicable updates 
   'Determine if it is already installed or not
      If update.IsInstalled = False Then
         WScript.Echo vbCRLF & _
         "Result: Update applicable, not installed."
         updateIsApplicable = True
         updateToInstall.Add(update)
      Else 
         'Update is installed so notify user and quit
         WScript.Echo vbCRLF & _
         "Result: Update applicable, already installed."
         updateIsApplicable = True
         WScript.Quit 
      End If
   End If 
Next

If updateIsApplicable = False Then
   WScript.Echo "Result: Update is not applicable to this machine."
   WScript.Quit
End If

WScript.Echo vbCRLF & "Would you like to install now? (Y/N)"
stdInput = WScript.StdIn.Readline
 
If (strInput = "N" or strInput = "n") Then 
   WScript.Quit
ElseIf  (stdInput = "Y" OR stdInput = "y") Then
   'Download update
   Set downloader = updateSession.CreateUpdateDownloader() 
   downloader.Updates = updateToInstall
   WScript.Echo vbCRLF & "Downloading..."
   Set downloadResult = downloader.Download()
   WScript.Echo "Download Result: " & downloadResult.ResultCode
  
   'Install Update
   Set installer = updateSession.CreateUpdateInstaller()
   WScript.Echo vbCRLF & "Installing..."
   installer.Updates = updateToInstall
   Set installationResult = installer.Install()
  
   'Output the result of the installation
   WScript.Echo "Installation Result: " & _
   installationResult.ResultCode
   WScript.Echo "Reboot Required: " & _
   installationResult.RebootRequired 
End If
```



 

 



