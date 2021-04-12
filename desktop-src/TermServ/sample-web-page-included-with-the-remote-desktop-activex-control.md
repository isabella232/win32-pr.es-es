---
title: Página Web de ejemplo incluida con el control ActiveX Escritorio remoto
description: Una página web de ejemplo (Default.htm) está en el directorio donde está instalado Conexión web a Escritorio remoto.
ms.assetid: 3137f58b-1aec-4bd6-a3b2-d1db6c8b96e4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec07ee86dcb5d10dc289e8095c83771ebe9a8b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357204"
---
# <a name="sample-webpage-included-with-the-remote-desktop-activex-control"></a>Página Web de ejemplo incluida con el control ActiveX Escritorio remoto

Al instalar el control ActiveX Escritorio remoto de Conexión web a Escritorio remoto, se copia una página web de ejemplo (Default.htm) en el directorio donde está instalado Conexión web a Escritorio remoto. Esta página puede ejecutarse tal cual o personalizarse para adaptarse a las necesidades de un usuario o de una organización.

La Página Web de ejemplo debe instalarse en un servidor Web que ejecute Windows Server e Internet Information Server 4,0 o posterior. Además, el explorador del equipo cliente debe ser Internet Explorer versión 4,0 o posterior. Para obtener más información, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).

Default.htm es una página web de inicio de sesión predeterminada que recopila información de conexión del usuario. La página de inicio de sesión contiene un campo obligatorio en el que el usuario escribe el nombre del servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto) o del equipo remoto al que se va a conectar. La página de inicio de sesión también incluye campos opcionales para el tamaño de pantalla y la información de inicio de sesión de usuario, incluido el nombre de usuario y el dominio.

Después de recopilar los datos de usuario, Default.htm pasa al control ActiveX Escritorio remoto (Msrdp. ocx) para iniciar una sesión de escritorio remoto. Los pasos necesarios para iniciar la sesión son los siguientes:

1.  Si es necesario, Internet Explorer descarga el archivo. cab y lo instala en el equipo del usuario.
2.  El usuario escribe el nombre de dominio completo o la dirección IP del equipo remoto en el campo correspondiente.

    -   Opcionalmente, el usuario puede especificar un tamaño de pantalla para la conexión. Si el usuario no especifica un tamaño de pantalla, la sesión se abre en modo de pantalla completa si el usuario está en una zona de seguridad de dirección URL de confianza. De lo contrario, la sesión se abre en modo de ventana.
    -   Opcionalmente, el usuario puede proporcionar información de inicio de sesión automática (nombre de usuario, dominio) para la sesión remota.

3.  Cuando el usuario hace clic en el botón **conectar** , Default.htm pasa los datos proporcionados por el usuario como parámetros al control ActiveX escritorio remoto.
4.  El escritorio remoto se abre en la ventana del explorador o en el modo de pantalla completa, según lo especificado por el usuario.

Cuando Default.htm se abre por primera vez con Internet Explorer, aparece un cuadro de diálogo que permite al usuario descargar el control ActiveX Escritorio remoto (Msrdp. ocx). El cuadro de diálogo aparece en las siguientes condiciones:

-   El equipo que tuvo acceso a la página web no tiene una instalación completa del cliente de Conexión web a Escritorio remoto (o el Cliente avanzado de Servicios de Escritorio remoto) con compatibilidad Web.
-   La versión instalada del archivo. cab en el equipo cliente es anterior a la versión de la página web Default.htm.

El tamaño de la sesión de escritorio remoto que aparece en la ventana del explorador es el tamaño especificado en la Página Web de Default.htm. Para cambiar el tamaño de la pantalla, el usuario debe desconectarse de la sesión, volver a la página web Default.htm y editar la información de conexión. Si no se ha especificado ningún tamaño de pantalla, la sesión se abre en la ventana del explorador en el modo de pantalla completa predeterminado. En esta resolución, el escritorio remoto se expande para que coincida con las dimensiones completas de la pantalla del usuario y no se muestran las barras de herramientas del explorador de Internet Explorer y los marcos de ventana. Al igual que con el cliente de Conexión a Escritorio remoto completo, el usuario puede alternar entre la pantalla completa y el modo de ventana presionando la combinación de [teclas de método abreviado](terminal-services-shortcut-keys.md) del modo de pantalla completa (Ctrl + Alt + inter).

Por motivos de seguridad, algunas opciones que están disponibles en el administrador de conexiones de Servicios de Escritorio remoto están restringidas en el control ActiveX Escritorio remoto a determinadas zonas de seguridad de direcciones URL de Internet Explorer. Consulte [proporcionar seguridad de cliente RDP](providing-for-rdp-client-security.md) para obtener más información acerca de estas opciones y sobre cómo especificar un programa para que se ejecute tras la conexión.

 

 




