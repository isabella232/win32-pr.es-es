---
description: Microsoft Windows Installer acepta un localizador uniforme de recursos (URL) como origen válido para una revisión.
ms.assetid: 11a65123-a8bd-46d8-a416-4fc2f2f1e121
title: Descarga e instalación de una revisión desde Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b5fe4ca51b08759bc178b89bfe71c89418e26d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158518"
---
# <a name="downloading-and-installing-a-patch-from-the-internet"></a>Descarga e instalación de una revisión desde Internet

Microsoft Windows Installer acepta un localizador uniforme de recursos (URL) como origen válido para una [revisión](patch-packages.md). Para instalar una revisión ubicada en un servidor web en https://MyWeb/MyPatch.msp , use la siguiente línea de comandos:

**msiexec /p https://MyWeb/MyPatch.msp**

Para evitar resultados inesperados, no inicie una revisión haciendo clic en el vínculo de la página web que muestra la dirección URL del archivo de revisión. También puede instalar una revisión mediante un script como el siguiente:


```VB
<SCRIPT LANGUAGE="VBScript"> 
<!-- 
Dim Installer
On Error Resume Next
set Installer=CreateObject("WindowsInstaller.Installer")
Installer.ApplyPatch "https://server/share/patch.msp", "", 0, "REINSTALL=ALL REINSTALLMODE=omus"
set Installer=Nothing
-->
</SCRIPT>
```



Tenga en cuenta que, dado que el objeto [**Installer**](installer-object.md) no está marcado como [SafeForScripting](safeforscripting.md) en el equipo del usuario, los usuarios deben ajustar la configuración de seguridad del explorador para que el ejemplo funcione correctamente.

Para obtener más información, vea [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and Digital Signatures (Directrices para crear instalaciones seguras y firmas [digitales) y Windows Installer](digital-signatures-and-windows-installer.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Paquetes de revisión](patch-packages.md)
</dt> <dt>

[Creación de un paquete de revisión](creating-a-patch-package.md)
</dt> <dt>

[Aplicación de revisiones a aplicaciones personalizadas](patching-customized-applications.md)
</dt> <dt>

[Descargar una instalación desde Internet](downloading-an-installation-from-the-internet.md)
</dt> </dl>

 

 



