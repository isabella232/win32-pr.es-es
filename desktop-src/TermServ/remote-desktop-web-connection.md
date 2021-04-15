---
title: Conexión web a Escritorio remoto
description: Conexión web a Escritorio remoto es una aplicación web formada por un control ActiveX y una página de conexión de ejemplo.
ms.assetid: f9d252b0-205a-47df-9eca-d5744c09e079
ms.tgt_platform: multiple
keywords:
- Conexión web a Escritorio remoto Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Protocolo de escritorio remoto (RDP), información general sobre Conexión web a Escritorio remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41bb1e8f562e3e5c47c6050f550fe3c7090446be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676419"
---
# <a name="remote-desktop-web-connection"></a>Conexión web a Escritorio remoto

Conexión web a Escritorio remoto es una aplicación web formada por un control ActiveX y una página de conexión de ejemplo. Al implementar Conexión web a Escritorio remoto en un servidor Web, puede proporcionar conectividad de cliente a los servidores host de sesión de Escritorio remoto (host de sesión de escritorio remoto) y a otros equipos con Internet Explorer y TCP/IP.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md)
</dt> <dd>

Enumera los requisitos de un Conexión web a Escritorio remoto.

</dd> <dt>

[Canales virtuales con scripts](scriptable-virtual-channels.md)
</dt> <dd>

Describe los cambios en el modelo de programación para implementar aplicaciones de canal virtual proporcionadas por el Terminal Services Cliente avanzado (TSAC).

</dd> </dl>

El material de referencia de Conexión web a Escritorio remoto se incluye en la sección de [referencia de conexión web a escritorio remoto](remote-desktop-web-connection-reference.md) .

Para más información, consulte los temas siguientes:

-   [Implementación de canales virtuales con scripts mediante Conexión web a Escritorio remoto](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md)
-   [Incrustar el control ActiveX Escritorio remoto en una página web](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
-   [Descargar y usar el control ActiveX Escritorio remoto](/previous-versions//aa380808(v=vs.85))
-   [Usar el control ActiveX Escritorio remoto con canales virtuales](using-the-remote-desktop-activex-control-with-virtual-channels.md)
-   [Proporcionar seguridad de cliente RDP](providing-for-rdp-client-security.md)
-   [Deshabilitar características de Servicios de Escritorio remoto](disabling-terminal-services-features.md)

## <a name="installing-remote-desktop-web-connection"></a>Instalación de Conexión web a Escritorio remoto

En los pasos siguientes se instala el control ActiveX de Escritorio remoto y la Página Web de ejemplo en el directorio% SystemRoot% \\ Web \\ TSWeb. Comparten la página web en el directorio TSWeb del servidor, por ejemplo,*en https:///TSWeb.* El control (Msrdp. ocx) y el código Conexión web a Escritorio remoto se encuentran en Msrdp.cab.

**Para instalar Conexión web a Escritorio remoto**

1.  En el elemento agregar o quitar programas del panel de control, en Agregar o quitar componentes de Windows, instale Microsoft Internet Information Services (IIS).
2.  Instale el subcomponente servicio de World Wide Web de IIS.
3.  Instale el subcomponente Conexión web a Escritorio remoto del servicio World Wide Web.

Para obtener una descripción de la página web que se incluye con la instalación de Conexión web a Escritorio remoto, vea [Página Web de ejemplo que se incluye con el control ActiveX escritorio remoto](sample-web-page-included-with-the-remote-desktop-activex-control.md).

 

 