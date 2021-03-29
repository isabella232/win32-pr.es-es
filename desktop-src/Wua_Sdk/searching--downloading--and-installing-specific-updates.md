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
# <a name="searching-downloading-and-installing-specific-updates"></a>Búsqueda, descarga e instalación de actualizaciones específicas

En el ejemplo de scripting de este tema se muestra cómo usar el agente de Windows Update (WUA) para examinar, descargar e instalar una actualización específica. La actualización puede especificarse por su título.

El ejemplo busca una actualización de software específica, descarga la actualización y, a continuación, instala la actualización. Por ejemplo, un usuario puede usar este método para determinar si una actualización de seguridad crítica está instalada en un equipo. Si la actualización no está instalada, el usuario puede asegurarse de que se ha descargado e instalado la actualización. El usuario también puede asegurarse de que se le notifique el estado de la instalación.

La actualización de ejemplo se identifica mediante el título de la actualización en la [**propiedad title de IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title). El título de la actualización que se sugiere en este ejemplo es "Update for Windows Rights Management Client 1,0."

> [!Note]  
> Para obtener información sobre cómo buscar, descargar e instalar todas las actualizaciones que se aplican a una aplicación específica, vea [Buscar, descargar e instalar actualizaciones](searching--downloading--and-installing-updates.md).

 

Antes de intentar ejecutar este ejemplo, tenga en cuenta lo siguiente:

-   WUA debe estar instalado en el equipo. Para obtener más información sobre cómo determinar la versión de WUA que está instalada, vea [determinar la versión actual de WUA](determining-the-current-version-of-wua.md).
-   El ejemplo no proporciona su propia interfaz de usuario. WUA solicita al usuario que reinicie el equipo si una actualización requiere un reinicio.
-   El ejemplo solo puede descargar actualizaciones de WUA. No puede descargar actualizaciones de un servidor de servicios de actualización de software (SUS) 1,0.
-   La ejecución de este ejemplo requiere Windows Script Host (WSH). Para obtener más información acerca de WSH, consulte la sección WSH del kit de desarrollo de software (SDK) de la plataforma. Si el ejemplo se copia en un archivo denominado WUA \_SpecificUpdate.vbs, puede ejecutarlo abriendo una ventana del símbolo del sistema y escribiendo este comando: **cscript WUA \_SpecificUpdate.vbs**  
    

## <a name="example"></a>Ejemplo

> [!IMPORTANT]
> Este script está pensado para demostrar el uso de las API del agente de Windows Update y proporcionar un ejemplo de cómo los desarrolladores pueden usar estas API para resolver los problemas. Este script no está pensado como código de producción y Microsoft no admite el propio script (aunque se admiten las API del agente de Windows Update subyacentes).

 


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



 

 



