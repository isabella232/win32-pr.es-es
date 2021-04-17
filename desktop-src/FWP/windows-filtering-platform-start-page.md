---
title: Plataforma de filtrado de Windows
description: La plataforma de filtrado de Windows (WFP) es un conjunto de servicios de API y de sistema que proporcionan una plataforma para crear aplicaciones de filtrado de red.
ms.assetid: 0436f559-20e6-4199-8391-10eb7d85df23
keywords:
- Plataforma de filtrado de Windows
- Página de inicio de la plataforma de filtrado de Windows, página de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cf63f995b44be607977dd0c70c6c91eed024e81
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "105665881"
---
# <a name="windows-filtering-platform"></a>Plataforma de filtrado de Windows

## <a name="purpose"></a>Propósito

La plataforma de filtrado de Windows (WFP) es un conjunto de servicios de API y de sistema que proporcionan una plataforma para crear aplicaciones de filtrado de red. La API de WFP permite a los desarrolladores escribir código que interactúa con el procesamiento de paquetes que tiene lugar en varios niveles de la pila de red del sistema operativo. Se pueden filtrar y modificar datos de red antes de que lleguen a su destino.

Al proporcionar una plataforma de desarrollo más sencilla, WFP está diseñado para reemplazar las tecnologías de filtrado de paquetes anteriores, como los filtros de Interfaz de controlador de transporte (TDI), los filtros de especificación de interfaz de controlador de red (NDIS) y los proveedores de servicios superpuestos (LSP) de Winsock. A partir de Windows Server 2008 y Windows Vista, el enlace de firewall y los controladores de enlace de filtros no están disponibles; en su lugar, las aplicaciones que usaban estos controladores deben usar WFP.

Con la API de WFP, los desarrolladores pueden implementar firewalls, sistemas de detección de intrusiones, programas antivirus, herramientas de supervisión de red y controles parentales. WFP se integra con y proporciona compatibilidad con características de Firewall como la comunicación autenticada y la configuración de Firewall dinámica basada en el uso de las aplicaciones de sockets API (directiva basada en aplicaciones). WFP también proporciona una infraestructura para la administración de directivas IPsec, notificaciones de cambios, diagnósticos de red y filtrado con estado.

La plataforma de filtrado de Windows es una plataforma de desarrollo y no un firewall. La aplicación de Firewall integrada en Windows Vista, Windows Server 2008 y los sistemas operativos posteriores Firewall de Windows con seguridad avanzada (WFAS) se implementa mediante WFP. Por lo tanto, las aplicaciones desarrolladas con la API de WFP o la [API de wfas](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) usan la lógica de arbitraje de filtrado común que está integrada en WFP.

La API de WFP se compone de una API de modo usuario y una API de modo kernel. En esta sección se proporciona información general de la WFP completa y se describe en detalle solo la parte del modo de usuario de la API de WFP. Para obtener una descripción detallada de la API de WFP en modo kernel, vea la ayuda en pantalla del [Kit de controladores de Windows](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) .

## <a name="developer-audience"></a>Audiencia de desarrolladores

La API de la plataforma de filtrado de Windows está diseñada para que la usen los programadores que usan software de desarrollo de C/C++. Los programadores deben estar familiarizados con los conceptos de red y el diseño de sistemas que usan componentes de modo de usuario y de modo kernel.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

La plataforma de filtrado de Windows se admite en clientes que ejecutan Windows Vista y versiones posteriores, y en servidores que ejecutan Windows Server 2008 y versiones posteriores. Para obtener información sobre los requisitos de tiempo de ejecución para un elemento de programación específico, vea la sección de requisitos de la página de referencia de ese elemento.





 

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                               | Descripción                                                                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Novedades de la plataforma de filtrado de Windows](what-s-new-in-windows-filtering-platform.md)<br/> | Información sobre las nuevas características y API de la plataforma de filtrado de Windows.<br/>                    |
| [Acerca de la plataforma de filtrado de Windows](about-windows-filtering-platform.md)<br/>                 | Información general sobre la plataforma de filtrado de Windows.<br/>                                             |
| [Uso de la plataforma de filtrado de Windows](using-windows-filtering-platform.md)<br/>                 | Código de ejemplo que usa la API de la plataforma de filtrado de Windows. <br/>                                |
| [Referencia de API de la plataforma de filtrado de Windows](fwp-reference.md)<br/>                            | Documentación de las funciones, estructuras y constantes de la plataforma de filtrado de Windows.<br/> |



 

## <a name="additional-resources"></a>Recursos adicionales

Para formular preguntas y tener discusiones sobre el uso de la API de WFP, visite el foro de la [plataforma de filtrado de Windows](https://social.msdn.microsoft.com/forums/wfp/threads/).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de plataforma de filtrado de Windows de modo kernel: Guía de diseño](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[API de plataforma de filtrado de Windows de modo kernel-referencia](/windows-hardware/drivers/ddi/_netvista/)
</dt> <dt>

[Firewall de Windows con seguridad avanzada](/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page)
</dt> <dt>

[Clase auxiliar extensible de diagnóstico de WFP](/windows/desktop/NDF/windows-filtering-platform-extensible-helper-class)
</dt> <dt>

[Extensiones Winsock Secure Socket](/windows/desktop/WinSock/winsock-secure-socket-extensions)
</dt> </dl>

 

