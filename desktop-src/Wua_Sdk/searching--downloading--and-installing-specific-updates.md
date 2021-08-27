---
description: En el ejemplo de scripting de este tema se muestra cómo usar Windows Update Agent (WUA) para examinar, descargar e instalar una actualización específica. La actualización se puede especificar por su título.
ms.assetid: 4a5bb920-fc51-48a0-8f66-bb2fcc72589f
title: Buscar, descargar e instalar actualizaciones específicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c2da9569ed6fe34b18264ee59e91965877d63e422ae20e25fc27fbc025e812
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071294"
---
# <a name="searching-downloading-and-installing-specific-updates"></a>Buscar, descargar e instalar actualizaciones específicas

En el ejemplo de scripting de este tema se muestra cómo usar Windows Update Agent (WUA) para examinar, descargar e instalar una actualización específica. La actualización se puede especificar por su título.

El ejemplo busca una actualización de software específica, la descarga y, a continuación, la instala. Por ejemplo, un usuario puede usar este método para determinar si hay una actualización de seguridad crítica instalada en un equipo. Si la actualización no está instalada, el usuario puede asegurarse de que la actualización se descarga e instala. El usuario también puede asegurarse de que se le notifica el estado de la instalación.

La actualización de ejemplo se identifica mediante el título de la actualización en [**la propiedad Title de IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title). El título de la actualización que se sugiere en este ejemplo es "Update for Windows Rights Management client 1.0".

> [!Note]  
> Para obtener información sobre cómo buscar, descargar e instalar todas las actualizaciones que se aplican a una aplicación específica, vea Buscar, descargar e [instalar actualizaciones.](searching--downloading--and-installing-updates.md)

 

Antes de intentar ejecutar este ejemplo, tenga en cuenta lo siguiente:

-   WUA debe estar instalado en el equipo. Para obtener más información sobre cómo determinar la versión de WUA que está instalada, vea Determinar la [versión actual de WUA.](determining-the-current-version-of-wua.md)
-   El ejemplo no proporciona su propia interfaz de usuario. WUA solicita al usuario que reinicie el equipo si una actualización requiere un reinicio.
-   El ejemplo solo puede descargar actualizaciones de WUA. No puede descargar actualizaciones desde un servidor de Software Update Services (SUS) 1.0.
-   La ejecución de este ejemplo requiere Windows host de script (WSH). Para obtener más información sobre WSH, consulte la sección WSH del Kit de desarrollo de software (SDK) de plataforma. Si el ejemplo se copia en un archivo denominado WUASpecificUpdate.vbs, puede ejecutarlo abriendo una ventana del símbolo del sistema y escribiendo este \_ comando: **cscript WUA \_SpecificUpdate.vbs**  
    

## <a name="example"></a>Ejemplo

> [!IMPORTANT]
> Este script está pensado para mostrar el uso de las API del agente de Windows Update y proporcionar un ejemplo de cómo los desarrolladores pueden usar estas API para solucionar problemas. Este script no está pensado como código de producción y Microsoft no admite el propio script (aunque se admiten las API Windows Update Agent subyacentes).

 


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



 

 



