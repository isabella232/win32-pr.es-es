---
title: Usar Administración remota de Windows
description: Administración remota de Windows está diseñado para mejorar la administración de hardware en un entorno de red con varios dispositivos que ejecutan diversos sistemas operativos.
ms.assetid: 6ee2b238-5bc2-4274-b7ca-49dbc728d8f1
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0c2934694de5913b467521510179fffdb220b601
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149453"
---
# <a name="using-windows-remote-management"></a>Usar Administración remota de Windows

Administración remota de Windows está diseñado para mejorar la administración de hardware en un entorno de red con varios dispositivos que ejecutan diversos sistemas operativos. Todo el diseño del servicio está orientado a la monitorización y la administración de equipos remotos implementando un protocolo estándar interoperable.

Dado que la [API de scripting de WinRM](winrm-scripting-api.md) y la API de C++ de [WinRM](winrm-c---api.md) implementan y modelan estrechamente las operaciones definidas para el protocolo de WS-Management, los scripts y las aplicaciones reciben secuencias de XML en respuesta a las solicitudes. Los parámetros de entrada para llamadas a métodos se deben construir en XML. Puede usar los métodos de la API de [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) para mostrar o construir cadenas XML. Para obtener un ejemplo, vea [Mostrar la salida XML de los scripts de WinRM](displaying-xml-output-from-winrm-scripts.md).

La lista siguiente incluye temas en los que se describe cómo usar el scripting de WinRM:

-   [Detección de si un equipo remoto admite WS-Management protocolo](detecting-whether-a-remote-computer-supports-ws-management-protocol.md)
-   [Obtención de datos del equipo local](obtaining-data-from-the-local-computer.md)
-   [Obtención de datos de un equipo remoto](obtaining-data-from-a-remote-computer.md)
-   [Enumerar o enumerar todas las instancias de un recurso](enumerating-or-listing-all-instances-of-a-resource.md)
-   [Consultar instancias específicas de un recurso](querying-for-specific-instances-of-a-resource.md)
-   [Mostrar la salida XML de los scripts de WinRM](displaying-xml-output-from-winrm-scripts.md)

## <a name="tracing-winrm-activity"></a>Seguimiento de la actividad de WinRM

Dado que WinRM obtiene datos a través de [instrumental de administración de Windows (WMI)](/windows/desktop/WmiSdk/wmi-start-page), puede realizar un seguimiento de la actividad de WMI resultante de los mensajes de WinRM. A partir de Windows Vista, el servicio WMI ya no utiliza los [archivos de registro de WMI](/windows/desktop/WmiSdk/wmi-log-files). En su lugar, utiliza el [seguimiento de eventos](/windows/desktop/ETW/event-tracing-portal) (ETW) y los eventos están disponibles a través de la interfaz de usuario de **visor de eventos** o la herramienta de línea de comandos Evtutil.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración remota de Windows](portal.md)
</dt> <dt>

[Acerca de Administración remota de Windows](about-windows-remote-management.md)
</dt> <dt>

[Referencia de Administración remota de Windows](windows-remote-management-reference.md)
</dt> <dt>

[Scripting en Administración remota de Windows](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 