---
title: Plataforma de filtrado de Windows
description: Windows Plataforma de filtrado (WFP) es un conjunto de servicios de API y del sistema que proporcionan una plataforma para crear aplicaciones de filtrado de red.
ms.assetid: 0436f559-20e6-4199-8391-10eb7d85df23
keywords:
- Plataforma de filtrado de Windows
- Windows Página de inicio de la plataforma de filtrado, página de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9c1f0e412426dd2bae7e5861d3b328d4e285c303aef046970e725a02965b974
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766495"
---
# <a name="windows-filtering-platform"></a>Plataforma de filtrado de Windows

## <a name="purpose"></a>Propósito

Windows Plataforma de filtrado (WFP) es un conjunto de servicios de API y del sistema que proporcionan una plataforma para crear aplicaciones de filtrado de red. La API de WFP permite a los desarrolladores escribir código que interactúa con el procesamiento de paquetes que tiene lugar en varios niveles de la pila de red del sistema operativo. Se pueden filtrar y modificar datos de red antes de que lleguen a su destino.

Al proporcionar una plataforma de desarrollo más sencilla, WFP está diseñado para reemplazar las tecnologías de filtrado de paquetes anteriores, como los filtros de Interfaz de controlador de transporte (TDI), los filtros de especificación de interfaz de controlador de red (NDIS) y los proveedores de servicios en capas (LSP) de Winsock. A partir Windows Server 2008 y Windows Vista, el enlace de firewall y los controladores de enlace de filtro no están disponibles; Las aplicaciones que usaban estos controladores deben usar WFP en su lugar.

Con la API de WFP, los desarrolladores pueden implementar firewalls, sistemas de detección de intrusiones, programas antivirus, herramientas de supervisión de red y controles parentales. WFP se integra con y proporciona compatibilidad con características de firewall, como la comunicación autenticada y la configuración dinámica del firewall basada en el uso por parte de las aplicaciones de la API de sockets (directiva basada en aplicaciones). WFP también proporciona infraestructura para la administración de directivas IPsec, las notificaciones de cambios, los diagnósticos de red y el filtrado con estado.

Windows La plataforma de filtrado es una plataforma de desarrollo y no un firewall en sí. La aplicación de firewall integrada en Windows Vista, Windows Server 2008 y sistemas operativos posteriores Windows Firewall con seguridad avanzada (WFAS) se implementa mediante WFP. Por lo tanto, las aplicaciones desarrolladas con la API de WFP o la [API de WFAS](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) usan la lógica común de arbitraje de filtrado integrada en WFP.

La API de WFP consta de una API en modo de usuario y una API en modo kernel. En esta sección se proporciona información general de todo el WFP y se describe en detalle solo la parte en modo de usuario de la API de WFP. Para obtener una descripción detallada de la API WFP en modo kernel, consulte la ayuda en línea [Windows Driver Kit.](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)

## <a name="developer-audience"></a>Audiencia de desarrolladores

La API Windows Filtering Platform está diseñada para su uso por los programadores que usan software de desarrollo de C/C++. Los programadores deben estar familiarizados con los conceptos de red y el diseño de sistemas que usan componentes de modo de usuario y modo kernel.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

La plataforma Windows filtrado se admite en clientes que ejecutan Windows Vista y versiones posteriores, y en servidores que ejecutan Windows Server 2008 y versiones posteriores. Para obtener información sobre los requisitos en tiempo de ejecución para un elemento de programación específico, vea la sección Requisitos de la página de referencia de ese elemento.





 

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                               | Descripción                                                                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Novedades de la plataforma Windows filtrado de datos](what-s-new-in-windows-filtering-platform.md)<br/> | Información sobre las nuevas características y API en Windows de filtrado.<br/>                    |
| [Acerca de Windows de filtrado de datos](about-windows-filtering-platform.md)<br/>                 | Información general sobre la plataforma Windows filtrado de datos.<br/>                                             |
| [Uso de Windows de filtrado de datos](using-windows-filtering-platform.md)<br/>                 | Código de ejemplo que usa Windows Filtering Platform API. <br/>                                |
| [Windows Referencia de API de la plataforma de filtrado](fwp-reference.md)<br/>                            | Documentación de las Windows, estructuras y constantes de la plataforma de filtrado de datos.<br/> |



 

## <a name="additional-resources"></a>Recursos adicionales

Para hacer preguntas y tener discusiones sobre el uso de la API de WFP, visite el foro de Windows [Filtering Platform](https://social.msdn.microsoft.com/forums/wfp/threads/).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Kernel-Mode Windows Filtering Platform API : Guía de diseño](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[Kernel-Mode Windows Filtering Platform API : referencia](/windows-hardware/drivers/ddi/_netvista/)
</dt> <dt>

[Firewall de Windows con seguridad avanzada](/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page)
</dt> <dt>

[Clase auxiliar extensible de diagnósticos WFP](/windows/desktop/NDF/windows-filtering-platform-extensible-helper-class)
</dt> <dt>

[Extensiones de socket seguro de Winsock](/windows/desktop/WinSock/winsock-secure-socket-extensions)
</dt> </dl>

 

