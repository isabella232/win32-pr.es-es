---
description: Se incluye un ejecutable de arranque configurable (Setup.exe) y una herramienta de configuración (Msistuff.exe) en los componentes del SDK de Windows para desarrolladores Windows Installer.
ms.assetid: 95fcea5c-b107-48b7-9ae8-84629353c554
title: Configuración de los Setup.exe recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41b7907310ff6efcf41e984bf132bbbaedf38b6a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158782"
---
# <a name="configuring-the-setupexe-resources"></a>Configuración de los Setup.exe recursos

Se incluye un ejecutable de arranque configurable (Setup.exe) y una herramienta de configuración [(Msistuff.exe](msistuff-exe.md)) en los componentes del SDK de Windows para Windows [Desarrolladores del instalador](platform-sdk-components-for-windows-installer-developers.md). Mediante el Msistuff.exe para configurar los recursos de Setup.exe, los desarrolladores pueden crear fácilmente una instalación web de un paquete Windows Installer. Para obtener más información, [vea Internet Download Bootstrapping](internet-download-bootstrapping.md).

Al escribir la siguiente línea de comandos, se configuran los recursos para el ejemplo descrito en [A URL Based Windows Installer Installation Example](a-url-based-windows-installer-installation-example.md).

`MsiStuff setup.exe /u https://www.blueyonderairlines.com/Products/MySetup /d MySetup.msi /n MySetup /v 150 /i https://www.blueyonderairlines.com/Products/Common/InstMsi /a Ansi/Instmsi.exe /w Unicode/Instmsi.exe`

[Continuar](sign-setup-exe-and-mysetup-msi.md)

 

 



