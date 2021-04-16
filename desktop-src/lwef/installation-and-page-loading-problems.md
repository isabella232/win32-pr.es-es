---
title: Problemas de instalación y carga de páginas
description: Problemas de instalación y carga de páginas
ms.assetid: 1611c3f1-0411-4631-a64c-e7637fc7edd9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c9775e6a9afa957867d5279b9faaf506e32757f
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2020
ms.locfileid: "105685684"
---
# <a name="installation-and-page-loading-problems"></a>Problemas de instalación y carga de páginas

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

### <a name="when-i-attempt-to-install-microsoft-agent-on-microsoft-windows-nt-i-get-a-message-indicating-that-i-need-to-be-an-administrator"></a>Al intentar instalar el agente de Microsoft en Microsoft Windows NT, aparece un mensaje que indica que es necesario ser administrador.

Dado que el agente de Microsoft escribe archivos en el directorio del sistema cuando se instala, debe tener privilegios de administrador (no de usuario) para instalar.

### <a name="when-i-attempt-to-install-microsoft-agent-i-get-one-of-the-following-errors-process-regsvr32-s-windowsmsagentagentctldll-error-while-creating-this-file-cannot-find-this-file-note-the-directory-location-cited-in-the-error-message-varies-depending-on-how-you-installed-windows-a-required-dll-msvcrtdll-was-not-found-error-creating-process-cwindowsmsagentagentsvrexe-regserver-reason-one-of-the-library-files-needed-to-run-this-application-cannot-be-found-note-the-directory-location-cited-in-the-error-message-varies-depending-on-how-you-installed-windows"></a>Al intentar instalar el agente de Microsoft, obtengo uno de los siguientes errores: Process (regsvr32/s Windows \\ msagent \\AgentCtl.dll). Error al crear este archivo. No se encuentra este archivo. (Nota: la ubicación del directorio citada en el mensaje de error varía en función de cómo haya instalado Windows). No se encontró un MSVCRT.DLL DLL necesario. Error al crear el proceso <c: \\ Windows \\ MSAgent \\agentsvr.exe/regserver>. Motivo: no se encuentra uno de los archivos de biblioteca necesarios para ejecutar esta aplicación. (Nota: la ubicación del directorio citada en el mensaje de error varía en función de cómo haya instalado Windows).

La instalación de Microsoft Agent requiere la instalación adecuada de Regsvr32.exe, Msvcrt.dll (la biblioteca en tiempo de ejecución de Microsoft C) y los archivos dll de OLE actualizados. Vea actualización de DCOM: ( <https://docs.microsoft.com/openspecs/windows_protocols/ms-dcom/4a893f3d-bd29-48cd-9f43-d9777a4415b0> ). La mejor manera de asegurarse de que todos los archivos del sistema correctos están presentes es instalar [Microsoft Internet Explorer 4,0](https://www.microsoft.com/ie/download) o posterior.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-i-get-a-scripting-error-vbscript-runtime-error-object-required"></a>Al intentar cargar una página generada por scripts para el agente de Microsoft, obtengo un error de scripting: "error de tiempo de ejecución de VBScript, objeto necesario".

Una de las condiciones siguientes puede hacer que se muestre el mensaje:

-   Las opciones de seguridad de Microsoft Internet Explorer deben estar configuradas para habilitar controles y complementos de ActiveX. Compruebe la página de seguridad del explorador. En Microsoft Internet Explorer, abra el menú Ver, elija Opciones, haga clic en la pestaña seguridad y asegúrese de que la casilla habilitar controles ActiveX y Plug-Ins está activada.
-   Está ejecutando en un sistema Windows 9x o Windows NT de arranque dual y ha instalado el agente de Microsoft en un sistema operativo pero está intentando obtener acceso a la página desde el otro sistema operativo. Aunque los sistemas operativos pueden compartir directorios y archivos, la información del registro que usa el agente de Microsoft no está compartida, por lo que debe instalar el agente de Microsoft en el sistema operativo que usa para tener acceso a las páginas web generadas con el carácter.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-nothing-happens"></a>Al intentar cargar una página con scripts para el agente de Microsoft, no sucede nada.

Esto puede ocurrir si se cumple alguna de las condiciones siguientes:

-   Compruebe las opciones de seguridad del explorador. El explorador debe estar establecido para habilitar la carga de scripts ActiveX y la reproducción de controles ActiveX.
-   Si va a tener acceso a las páginas de scripts con Microsoft Agent y con Microsoft Internet Explorer, debe tener la versión 3,02 o posterior (Descargue la versión más reciente de Internet Explorer en [https://www.microsoft.com/windows/ie/](https://www.microsoft.com/windows/internet-explorer/default.aspx) <https://www.microsoft.com/windows/ie/> ). En Microsoft Internet Explorer, abra el menú Ver, elija Opciones, haga clic en la pestaña seguridad y seleccione todas las casillas de contenido activo.
-   Un applet de Java en la página también puede producir este error. Para ejecutar el agente de Microsoft en la misma página que un applet de Java, se requiere la versión 2,0 de la máquina virtual (VM) de Microsoft. Para obtener más información, vea las [preguntas más frecuentes sobre programación y scripting](programming-scripting-faq.md).

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-i-get-the-message-unable-to-initialize-microsoft-agent"></a>Al intentar cargar una página con scripts para el agente de Microsoft, obtengo el mensaje "no se puede inicializar el agente de Microsoft".

Esto suele ocurrir cuando no tiene Microsoft Agent o algún otro control que la página usa instalado y elige no cuando se le pide que instale el control. Intente actualizar la página, aunque es posible que la página solo funcione si instala todos los componentes que requiere.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-i-get-the-message-the-component-has-been-digitally-signed-by-its-publisher-but-the-signature-does-not-match-the-component-it-is-possible-that-this-component-has-been-damaged-or-tampered-with-do-you-want-to-continue"></a>Al intentar cargar una página con scripts para el agente de Microsoft, obtengo el mensaje "el componente ha sido firmado digitalmente por su publicador, pero la firma no coincide con el componente. ¿Es posible que este componente se haya dañado o alterado? ¿Quiere continuar?".

Esto puede aparecer si intenta instalar Microsoft Agent en Microsoft Internet Explorer 3,02. Puede continuar con la instalación o actualizar el explorador a Internet Explorer 4,0 o posterior.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-using-netscape-navigator-or-other-internet-browsers-i-get-errors"></a>Al intentar cargar una página generada por scripts para el agente de Microsoft con Netscape Navigator (u otros exploradores de Internet), obtengo errores.

El agente de Microsoft se implementa mediante interfaces ActiveX. Solo se puede utilizar con un explorador (por ejemplo, Microsoft Internet Explorer) que admita la incrustación de objetos ActiveX a través de un script en una página y solo en sistemas que ejecuten Microsoft Windows 95, Windows 98 y Windows NT 4,0 (o posterior). Si no usa Microsoft Internet Explorer ( [https://www.microsoft.com/windows/ie/](https://www.microsoft.com/windows/internet-explorer/default.aspx) ), consulte con el proveedor del explorador para obtener más información sobre la compatibilidad con ActiveX.

 

 




