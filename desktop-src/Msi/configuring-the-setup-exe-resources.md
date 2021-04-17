---
description: En los componentes Windows SDK para los programadores de Windows Installer se incluye un ejecutable de bootstrap (Setup.exe) y una herramienta de configuración (Msistuff.exe) configurables.
ms.assetid: 95fcea5c-b107-48b7-9ae8-84629353c554
title: Configuración de los recursos de Setup.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41b7907310ff6efcf41e984bf132bbbaedf38b6a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "105653265"
---
# <a name="configuring-the-setupexe-resources"></a><span data-ttu-id="9d03b-103">Configuración de los recursos de Setup.exe</span><span class="sxs-lookup"><span data-stu-id="9d03b-103">Configuring the Setup.exe Resources</span></span>

<span data-ttu-id="9d03b-104">En los [componentes Windows SDK para los programadores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md)se incluye un ejecutable de bootstrap (Setup.exe) y una herramienta de configuración ( [Msistuff.exe](msistuff-exe.md)) configurables.</span><span class="sxs-lookup"><span data-stu-id="9d03b-104">A configurable bootstrap executable (Setup.exe) and configuration tool ( [Msistuff.exe](msistuff-exe.md)) is included in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="9d03b-105">Mediante el uso de Msistuff.exe para configurar los recursos en Setup.exe, los desarrolladores pueden crear fácilmente una instalación Web de un paquete de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="9d03b-105">By using Msistuff.exe to configure the resources in Setup.exe, developers can easily create a web installation of a Windows Installer package.</span></span> <span data-ttu-id="9d03b-106">Para obtener más información, consulte [arranque de descarga en Internet](internet-download-bootstrapping.md).</span><span class="sxs-lookup"><span data-stu-id="9d03b-106">For more information see [Internet Download Bootstrapping](internet-download-bootstrapping.md).</span></span>

<span data-ttu-id="9d03b-107">Al escribir la siguiente línea de comandos, se configuran los recursos para el ejemplo descrito en [una dirección URL basada Windows Installer ejemplo de instalación](a-url-based-windows-installer-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="9d03b-107">Entering the following command line configures the resources for the sample described in [A URL Based Windows Installer Installation Example](a-url-based-windows-installer-installation-example.md).</span></span>

`MsiStuff setup.exe /u https://www.blueyonderairlines.com/Products/MySetup /d MySetup.msi /n MySetup /v 150 /i https://www.blueyonderairlines.com/Products/Common/InstMsi /a Ansi/Instmsi.exe /w Unicode/Instmsi.exe`

[<span data-ttu-id="9d03b-108">Continuar</span><span class="sxs-lookup"><span data-stu-id="9d03b-108">Continue</span></span>](sign-setup-exe-and-mysetup-msi.md)

 

 



