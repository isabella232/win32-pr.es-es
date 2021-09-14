---
title: Página web de ejemplo incluida con el control Escritorio remoto ActiveX datos
description: Hay una página web de ejemplo (Default.htm) en el directorio donde Conexión web a Escritorio remoto está instalado.
ms.assetid: 3137f58b-1aec-4bd6-a3b2-d1db6c8b96e4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec07ee86dcb5d10dc289e8095c83771ebe9a8b0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374538"
---
# <a name="sample-webpage-included-with-the-remote-desktop-activex-control"></a>Página web de ejemplo incluida con el control Escritorio remoto ActiveX datos

Al instalar el control Escritorio remoto ActiveX de Conexión web a Escritorio remoto, se copia una página web de ejemplo (Default.htm) en el directorio donde Conexión web a Escritorio remoto está instalado. Esta página se puede ejecutar tal y como está o personalizarse para satisfacer las necesidades de un usuario o una organización.

La página web de ejemplo debe instalarse en un servidor web que ejecute Windows Server e Internet Information Server 4.0 o posterior. Además, el explorador del equipo cliente debe estar Internet Explorer versión 4.0 o posterior. Para obtener más información, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

Default.htm es una página web de inicio de sesión predeterminada que recopila información de conexión del usuario. La página de inicio de sesión contiene un campo obligatorio en el que el usuario escribe el nombre del servidor de host de sesión de Escritorio remoto (host de sesión de Escritorio remoto) o del equipo remoto al que se va a conectar. La página de inicio de sesión también incluye campos opcionales para el tamaño de pantalla y la información de inicio de sesión del usuario, incluidos el nombre de usuario y el dominio.

Después de recopilar los datos de usuario, Default.htm los pasa al control Escritorio remoto ActiveX (Msrdp.ocx) para iniciar una sesión de Escritorio remoto. Los pasos necesarios para iniciar la sesión son los siguientes:

1.  Si es necesario, Internet Explorer descarga el .cab archivo y lo instala en el equipo del usuario.
2.  El usuario escribe el nombre de dominio completo o la dirección IP del equipo remoto en el campo adecuado.

    -   Opcionalmente, el usuario puede especificar un tamaño de pantalla para la conexión. Si el usuario no especifica un tamaño de pantalla, la sesión se abre en modo de pantalla completa si el usuario se encuentra en una zona de seguridad de dirección URL de confianza. De lo contrario, la sesión se abre en modo de ventana.
    -   Opcionalmente, el usuario puede proporcionar información de inicio de sesión automático (nombre de usuario, dominio) para la sesión remota.

3.  Cuando el usuario hace clic en **el Conectar,** Default.htm los datos proporcionados por el usuario como parámetros al control Escritorio remoto ActiveX usuario.
4.  El escritorio remoto se abre en la ventana del explorador o en modo de pantalla completa, según lo especificado por el usuario.

Cuando Default.htm por primera vez mediante Internet Explorer, aparece un cuadro de diálogo que ofrece al usuario la opción de descargar el control Escritorio remoto ActiveX (Msrdp.ocx). El cuadro de diálogo aparece en las siguientes condiciones:

-   El equipo que ha accedido a la página web no tiene una instalación completa del cliente de Conexión web a Escritorio remoto (o el Servicios de Escritorio remoto Cliente avanzado) con soporte web.
-   La versión instalada del archivo .cab en el equipo cliente es anterior a la versión de la página Default.htm web.

El tamaño de la sesión de Escritorio remoto que aparece en la ventana del explorador es el tamaño especificado en la página Default.htm web. Para cambiar el tamaño de la pantalla, el usuario debe desconectarse de la sesión, volver a la página web Default.htm web y editar la información de conexión. Si no se ha especificado ningún tamaño de pantalla, la sesión se abre en la ventana del explorador en el modo de pantalla completa predeterminado. En esta resolución, el escritorio remoto se expande para que coincida con las dimensiones completa de la pantalla del usuario y no se muestran las barras de herramientas del explorador Internet Explorer y los marcos de ventana. Al igual que con el cliente de Conexión a Escritorio remoto completo, el usuario puede alternar entre [](terminal-services-shortcut-keys.md) el modo de pantalla completa y el modo de ventana presionando la combinación de teclas de método abreviado de modo de pantalla completa (CTRL+ALT+BREAK).

Por motivos de seguridad, algunas opciones que están disponibles en el Servicios de Escritorio remoto Connection Manager están restringidas en el control de Escritorio remoto ActiveX a determinadas zonas de seguridad de Internet Explorer URL. Consulte Proporcionar [seguridad de cliente RDP](providing-for-rdp-client-security.md) para obtener más información sobre estas opciones y sobre cómo especificar un programa para ejecutarse durante la conexión.

 

 




