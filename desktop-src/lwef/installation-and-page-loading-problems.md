---
title: Problemas de instalación y carga de páginas
description: Problemas de instalación y carga de páginas
ms.assetid: 1611c3f1-0411-4631-a64c-e7637fc7edd9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3139a9224f88f49a31b1f71a981d1b49b3e42127
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481950"
---
# <a name="installation-and-page-loading-problems"></a>Problemas de instalación y carga de páginas

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

### <a name="when-i-attempt-to-install-microsoft-agent-on-microsoft-windows-nt-i-get-a-message-indicating-that-i-need-to-be-an-administrator"></a>Cuando intento instalar Microsoft Agent en Microsoft Windows NT, aparece un mensaje que indica que tengo que ser administrador.

Dado que Microsoft Agent escribe archivos en el directorio del sistema cuando se instala, debe tener privilegios de administrador (no de usuario) para instalar.

### <a name="when-i-attempt-to-install-microsoft-agent-i-get-one-of-the-following-errors-process-regsvr32-s-windowsmsagentagentctldll-error-while-creating-this-file-cannot-find-this-file-note-the-directory-location-cited-in-the-error-message-varies-depending-on-how-you-installed-windows-a-required-dll-msvcrtdll-was-not-found-error-creating-process-cwindowsmsagentagentsvrexe-regserver-reason-one-of-the-library-files-needed-to-run-this-application-cannot-be-found-note-the-directory-location-cited-in-the-error-message-varies-depending-on-how-you-installed-windows"></a>Al intentar instalar Microsoft Agent, se obtiene uno de los siguientes errores: Process (Regsvr32 /s windows \\ msagent \\AgentCtl.dll). Error al crear este archivo. No se encuentra este archivo. (Nota: La ubicación del directorio mencionada en el mensaje de error varía en función de cómo se haya instalado Windows). No se encontró MSVCRT.DLL dll necesaria. Error al crear el <c: \\ windows \\ msagent \\agentsvr.exe /regserver>. Motivo: no se encuentra uno de los archivos de biblioteca necesarios para ejecutar esta aplicación. (Nota: La ubicación del directorio mencionada en el mensaje de error varía en función de cómo se haya instalado Windows).

La instalación de Microsoft Agent requiere la instalación adecuada de archivos Regsvr32.exe, Msvcrt.dll (la biblioteca en tiempo de ejecución de Microsoft C) y dlls OLE actualizados. Vea Actualización de DCOM: ( <https://docs.microsoft.com/openspecs/windows_protocols/ms-dcom/4a893f3d-bd29-48cd-9f43-d9777a4415b0> ). La mejor manera de asegurarse de que todos los archivos del sistema correctos están presentes es instalar [Microsoft Internet Explorer 4.0](https://www.microsoft.com/ie/download) o posterior.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-i-get-a-scripting-error-vbscript-runtime-error-object-required"></a>Cuando intento cargar una página con script para Microsoft Agent, aparece un error de scripting: "Error en tiempo de ejecución de VBScript, se requiere objeto".

Una de las siguientes condiciones puede hacer que se muestre el mensaje:

-   Las opciones de seguridad de Microsoft Internet Explorer deben establecerse para habilitar ActiveX controles y complementos. Compruebe la página de seguridad del explorador. En Microsoft Internet Explorer, abra el menú Ver, elija Opciones, haga clic en el ficha Seguridad y asegúrese de que la casilla Habilitar controles ActiveX y Plug-Ins está activada.
-   Se ejecuta en un sistema de arranque doble Windows 9x o Windows NT y ha instalado Microsoft Agent en un sistema operativo, pero está intentando acceder a la página desde el otro sistema operativo. Aunque los sistemas operativos pueden compartir directorios y archivos, la información del Registro utilizada por Microsoft Agent no se comparte, por lo que debe instalar Microsoft Agent en el sistema operativo que usa para acceder a las páginas web con el carácter .

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-nothing-happens"></a>Cuando intento cargar una página con script para Microsoft Agent, no ocurre nada.

Esto puede ocurrir si existe una de las condiciones siguientes:

-   Compruebe las opciones de seguridad del explorador. El explorador debe establecerse para habilitar la carga de scripts ActiveX y la reproducción de ActiveX controles.
-   Si está accediendo a páginas con scripts con Microsoft Agent y usa Microsoft Internet Explorer, debe tener la versión 3.02 o posterior (descargue la versión más reciente de Internet Explorer en [https://www.microsoft.com/windows/ie/](https://www.microsoft.com/windows/internet-explorer/default.aspx) <https://www.microsoft.com/windows/ie/> ). En Microsoft Internet Explorer, abra el menú Ver, elija Opciones, haga clic en ficha Seguridad y active todas las casillas Contenido activo.
-   Un applet de Java en la página también puede producir este error. Para ejecutar Microsoft Agent en la misma página que un applet de Java, se requiere la versión 2.0 de la máquina virtual (VM) de Microsoft. Para obtener más información, vea Las preguntas más frecuentes [sobre programación y scripting.](programming-scripting-faq.yml)

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-i-get-the-message-unable-to-initialize-microsoft-agent"></a>Cuando intento cargar una página con script para Microsoft Agent, aparece el mensaje "No se puede inicializar Microsoft Agent".

Esto suele ocurrir cuando no tiene instalado Microsoft Agent ni ningún otro control que la página use y elija No cuando se le pida que instale el control. Pruebe a actualizar la página, aunque la página puede funcionar solo si instala todos los componentes que requiere.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-i-get-the-message-the-component-has-been-digitally-signed-by-its-publisher-but-the-signature-does-not-match-the-component-it-is-possible-that-this-component-has-been-damaged-or-tampered-with-do-you-want-to-continue"></a>Cuando intento cargar una página con script para Microsoft Agent, aparece el mensaje "El componente ha sido digitalmente "firmado" por su publicador, pero la firma no coincide con el componente. ¿Es posible que este componente se haya dañado o alterado? ¿Quiere continuar?".

Esto puede aparecer si intenta instalar Microsoft Agent en Microsoft Internet Explorer 3.02. Puede continuar con la instalación o actualizar el explorador a Internet Explorer 4.0 o posterior.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-using-netscape-navigator-or-other-internet-browsers-i-get-errors"></a>Cuando intento cargar una página con scripts para Microsoft Agent mediante Netscape Navigator (u otros exploradores de Internet), se producen errores.

Microsoft Agent se implementa mediante ActiveX interfaces. Solo se puede usar con un explorador (como Microsoft Internet Explorer) que admita la inserción de objetos de ActiveX a través de un script en una página y solo en sistemas que ejecutan Microsoft Windows 95, Windows 98 y Windows NT 4.0 (o posterior). Si no usa Microsoft Internet Explorer ( ), consulte con el proveedor del explorador para obtener más información sobre ActiveX [https://www.microsoft.com/windows/ie/](https://www.microsoft.com/windows/internet-explorer/default.aspx) compatibilidad.

 

 




