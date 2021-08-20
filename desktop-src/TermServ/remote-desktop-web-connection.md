---
title: Conexión web a Escritorio remoto
description: Conexión web a Escritorio remoto es una aplicación web que consta de un control ActiveX y una página de conexión de ejemplo.
ms.assetid: f9d252b0-205a-47df-9eca-d5744c09e079
ms.tgt_platform: multiple
keywords:
- Conexión web a Escritorio remoto Servicios de Escritorio remoto
- Protocolo de escritorio remoto (RDP) Servicios de Escritorio remoto , Conexión web a Escritorio remoto información general
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17260f76f1906be8adbb627cb4a1aa5e43e2b288ba70bec2e64da60f2af039f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117940491"
---
# <a name="remote-desktop-web-connection"></a>Conexión web a Escritorio remoto

Conexión web a Escritorio remoto es una aplicación web que consta de un control ActiveX y una página de conexión de ejemplo. Al implementar Conexión web a Escritorio remoto en un servidor web, puede proporcionar conectividad de cliente a servidores de host de sesión de Escritorio remoto (host de sesión de Escritorio remoto) y a otros equipos mediante Internet Explorer y TCP/IP.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md)
</dt> <dd>

Enumera los requisitos de un Conexión web a Escritorio remoto.

</dd> <dt>

[Canales virtuales que se pueden incluir en scripts](scriptable-virtual-channels.md)
</dt> <dd>

Describe los cambios en el modelo de programación para implementar aplicaciones de canal virtual proporcionadas por terminal Services Cliente avanzado (TSAC).

</dd> </dl>

El material de referencia Conexión web a Escritorio remoto se incluye en la [Conexión web a Escritorio remoto referencia.](remote-desktop-web-connection-reference.md)

Para más información, consulte los temas siguientes:

-   [Implementación de canales virtuales con scripts mediante Conexión web a Escritorio remoto](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md)
-   [Inserción del control Escritorio remoto ActiveX en una página web](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
-   [Descargar y usar el control Escritorio remoto ActiveX control](/previous-versions//aa380808(v=vs.85))
-   [Uso del control Escritorio remoto ActiveX con canales virtuales](using-the-remote-desktop-activex-control-with-virtual-channels.md)
-   [Proporcionar seguridad de cliente RDP](providing-for-rdp-client-security.md)
-   [Deshabilitación de Servicios de Escritorio remoto características](disabling-terminal-services-features.md)

## <a name="installing-remote-desktop-web-connection"></a>Instalación de Conexión web a Escritorio remoto

Los pasos siguientes instalan el control Escritorio remoto ActiveX y la página web de ejemplo en el directorio %systemroot% \\ \\ Web Tsweb. Comparten la página web en el directorio Tsweb del servidor, por ejemplo, en https://*MyServer*/tsweb. El control (Msrdp.ocx) y el Conexión web a Escritorio remoto se encuentran en Msrdp.cab.

**Para instalar Conexión web a Escritorio remoto**

1.  En el elemento Agregar o quitar programas de Panel de control, en Agregar o quitar Windows componentes, instale Microsoft Internet Information Services (IIS).
2.  Instale el subcomponente World Wide Web Service de IIS.
3.  Instale el Conexión web a Escritorio remoto subcomponente de World Wide Web Service.

Para obtener una descripción de la página web que se incluye con la instalación de Conexión web a Escritorio remoto, vea Página web de ejemplo incluida [con Escritorio remoto ActiveX Control](sample-web-page-included-with-the-remote-desktop-activex-control.md).

 

 