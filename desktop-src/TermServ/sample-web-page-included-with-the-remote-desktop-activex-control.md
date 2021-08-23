---
title: Página web de ejemplo incluida con el control Escritorio remoto ActiveX ejemplo
description: Una página web de ejemplo (Default.htm) se encuentra en el directorio donde Conexión web a Escritorio remoto está instalado.
ms.assetid: 3137f58b-1aec-4bd6-a3b2-d1db6c8b96e4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c175bafe1ebde3367c20529a6d76d7933a42f343de56216649735c942105aa65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058543"
---
# <a name="sample-webpage-included-with-the-remote-desktop-activex-control"></a>Página web de ejemplo incluida con el control Escritorio remoto ActiveX ejemplo

Al instalar el control Escritorio remoto ActiveX de Conexión web a Escritorio remoto, se copia una página web de ejemplo (Default.htm) en el directorio donde Conexión web a Escritorio remoto está instalado. Esta página se puede ejecutar tal y como está o personalizarse para ajustarse a las necesidades de un usuario o una organización.

La página web de ejemplo debe instalarse en un servidor web que ejecute Windows Server e Internet Information Server 4.0 o posterior. Además, el explorador del equipo cliente debe Internet Explorer versión 4.0 o posterior. Para obtener más información, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

Default.htm es una página web de inicio de sesión predeterminada que recopila información de conexión del usuario. La página de inicio de sesión contiene un campo obligatorio en el que el usuario escribe el nombre del servidor de host de sesión de Escritorio remoto (host de sesión de Escritorio remoto) o del equipo remoto al que conectarse. La página de inicio de sesión también incluye campos opcionales para el tamaño de pantalla y la información de inicio de sesión del usuario, incluidos el nombre de usuario y el dominio.

Después de recopilar los datos del usuario, Default.htm los pasa al control Escritorio remoto ActiveX (Msrdp.ocx) para iniciar una sesión de Escritorio remoto. Los pasos necesarios para iniciar la sesión son los siguientes:

1.  Si es necesario, Internet Explorer descarga .cab archivo y lo instala en el equipo del usuario.
2.  El usuario escribe el nombre de dominio completo o la dirección IP del equipo remoto en el campo adecuado.

    -   Opcionalmente, el usuario puede especificar un tamaño de pantalla para la conexión. Si el usuario no especifica un tamaño de pantalla, la sesión se abre en modo de pantalla completa si el usuario está en una zona de seguridad de direcciones URL de confianza. De lo contrario, la sesión se abre en modo de ventana.
    -   Opcionalmente, el usuario puede proporcionar información de inicio de sesión automático (nombre de usuario, dominio) para la sesión remota.

3.  Cuando el usuario hace clic en **el Conectar,** Default.htm los datos proporcionados por el usuario como parámetros al control Escritorio remoto ActiveX usuario.
4.  El escritorio remoto se abre en la ventana del explorador o en modo de pantalla completa, según lo especificado por el usuario.

Cuando Default.htm por primera vez mediante Internet Explorer, aparece un cuadro de diálogo que ofrece al usuario la opción de descargar el control Escritorio remoto ActiveX (Msrdp.ocx). El cuadro de diálogo aparece en las condiciones siguientes:

-   El equipo que ha accedido a la página web no tiene una instalación completa del cliente de Conexión web a Escritorio remoto (o el Servicios de Escritorio remoto Cliente avanzado) con compatibilidad web.
-   La versión instalada del archivo .cab en el equipo cliente es anterior a la versión de la página Default.htm web.

El tamaño de la sesión de Escritorio remoto que aparece en la ventana del explorador es el tamaño especificado en la página Default.htm web. Para cambiar el tamaño de la pantalla, el usuario debe desconectarse de la sesión, volver a la página web Default.htm web y editar la información de conexión. Si no se ha especificado ningún tamaño de pantalla, la sesión se abre en la ventana del explorador en el modo de pantalla completa predeterminado. Con esta resolución, el escritorio remoto se expande para que coincida con las dimensiones completa de la pantalla del usuario y las barras de herramientas del explorador Internet Explorer y los marcos de ventana no se muestran. Al igual que con el cliente de Conexión a Escritorio remoto, el usuario puede alternar entre el [](terminal-services-shortcut-keys.md) modo de pantalla completa y el modo de ventana presionando la combinación de teclas de método abreviado de modo de pantalla completa (CTRL+ALT+BREAK).

Por motivos de seguridad, algunas opciones que están disponibles en el Servicios de Escritorio remoto Connection Manager están restringidas en el control Escritorio remoto ActiveX a determinadas zonas de seguridad de Internet Explorer URL. Consulte Proporcionar [seguridad de cliente RDP](providing-for-rdp-client-security.md) para obtener más información sobre estas opciones y sobre cómo especificar un programa para ejecutarse tras la conexión.

 

 




