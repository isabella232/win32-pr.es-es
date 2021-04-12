---
description: Microsoft Windows Installer acepta un localizador uniforme de recursos (URL) como origen válido de una revisión.
ms.assetid: 11a65123-a8bd-46d8-a416-4fc2f2f1e121
title: Descargar e instalar una revisión desde Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b5fe4ca51b08759bc178b89bfe71c89418e26d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154821"
---
# <a name="downloading-and-installing-a-patch-from-the-internet"></a><span data-ttu-id="7eee7-103">Descargar e instalar una revisión desde Internet</span><span class="sxs-lookup"><span data-stu-id="7eee7-103">Downloading and Installing a Patch From the Internet</span></span>

<span data-ttu-id="7eee7-104">Microsoft Windows Installer acepta un localizador uniforme de recursos (URL) como origen válido de una [revisión](patch-packages.md).</span><span class="sxs-lookup"><span data-stu-id="7eee7-104">Microsoft Windows Installer accepts a Uniform Resource Locator (URL) as a valid source for a [patch](patch-packages.md).</span></span> <span data-ttu-id="7eee7-105">Para instalar una revisión ubicada en un servidor Web en https://MyWeb/MyPatch.msp , utilice la siguiente línea de comandos:</span><span class="sxs-lookup"><span data-stu-id="7eee7-105">To install a patch located on a web server at https://MyWeb/MyPatch.msp, use the following command line:</span></span>

<span data-ttu-id="7eee7-106">**msiexec/p https://MyWeb/MyPatch.msp**</span><span class="sxs-lookup"><span data-stu-id="7eee7-106">**msiexec /p https://MyWeb/MyPatch.msp**</span></span>

<span data-ttu-id="7eee7-107">Para evitar resultados inesperados, no inicie una revisión haciendo clic en el vínculo de la página web que muestra la dirección URL del archivo de revisión.</span><span class="sxs-lookup"><span data-stu-id="7eee7-107">To avoid unexpected results, do not launch a patch by clicking the link on the webpage showing the patch file's URL.</span></span> <span data-ttu-id="7eee7-108">También puede instalar una revisión mediante un script similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="7eee7-108">You can also install a patch by using a script like the following:</span></span>


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



<span data-ttu-id="7eee7-109">Tenga en cuenta que, como el objeto de [**instalador**](installer-object.md) no está marcado como [SafeForScripting](safeforscripting.md) en el equipo del usuario, los usuarios deben ajustar la configuración de seguridad del explorador para que el ejemplo funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="7eee7-109">Note that because the [**Installer**](installer-object.md) object is not marked as [SafeForScripting](safeforscripting.md) on the user's computer, users need to adjust their browser security settings for the example to work correctly.</span></span>

<span data-ttu-id="7eee7-110">Para obtener más información, consulte [instrucciones para crear instalaciones seguras](guidelines-for-authoring-secure-installations.md) y [firmas digitales y Windows Installer](digital-signatures-and-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="7eee7-110">For more information, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7eee7-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7eee7-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7eee7-112">Paquetes de revisión</span><span class="sxs-lookup"><span data-stu-id="7eee7-112">Patch Packages</span></span>](patch-packages.md)
</dt> <dt>

[<span data-ttu-id="7eee7-113">Crear un paquete de revisión</span><span class="sxs-lookup"><span data-stu-id="7eee7-113">Creating a Patch Package</span></span>](creating-a-patch-package.md)
</dt> <dt>

[<span data-ttu-id="7eee7-114">Aplicación de revisiones a aplicaciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="7eee7-114">Patching Customized Applications</span></span>](patching-customized-applications.md)
</dt> <dt>

[<span data-ttu-id="7eee7-115">Descarga de una instalación desde Internet</span><span class="sxs-lookup"><span data-stu-id="7eee7-115">Downloading an Installation From the Internet</span></span>](downloading-an-installation-from-the-internet.md)
</dt> </dl>

 

 



