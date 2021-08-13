---
description: Se incluye un ejecutable de arranque configurable (Setup.exe) y una herramienta de configuración (Msistuff.exe) en los componentes del SDK de Windows para desarrolladores Windows Installer.
ms.assetid: 95fcea5c-b107-48b7-9ae8-84629353c554
title: Configuración de los Setup.exe recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3c181453f689b7f2c273ba8726097e5d1cd134d1b9675c8ffc42de42d902b89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638734"
---
# <a name="configuring-the-setupexe-resources"></a>Configuración de los Setup.exe recursos

Se incluye un ejecutable de arranque configurable (Setup.exe) y una herramienta de configuración [(Msistuff.exe](msistuff-exe.md)) en los componentes del SDK de Windows para desarrolladores [Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Mediante el Msistuff.exe para configurar los recursos de Setup.exe, los desarrolladores pueden crear fácilmente una instalación web de un paquete Windows Installer. Para obtener más información, [vea Internet Download Bootstrapping](internet-download-bootstrapping.md).

Al escribir la siguiente línea de comandos, se configuran los recursos para el ejemplo descrito en [A URL Based Windows Installer Installation Example](a-url-based-windows-installer-installation-example.md).

`MsiStuff setup.exe /u https://www.blueyonderairlines.com/Products/MySetup /d MySetup.msi /n MySetup /v 150 /i https://www.blueyonderairlines.com/Products/Common/InstMsi /a Ansi/Instmsi.exe /w Unicode/Instmsi.exe`

[Continuar](sign-setup-exe-and-mysetup-msi.md)

 

 



