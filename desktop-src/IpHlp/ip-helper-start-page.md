---
description: La API de la aplicación auxiliar de protocolo de Internet (aplicación auxiliar de IP) permite la recuperación y modificación de la configuración de red del equipo local.
ms.assetid: 4896a9f8-0486-4380-bf49-d1c9ef114acc
title: Asistente de IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1d50153e1ad890063f33a473058f6a850a9f171
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907889"
---
# <a name="ip-helper"></a>Asistente de IP

## <a name="purpose"></a>Propósito

La API de la aplicación auxiliar de protocolo de Internet (aplicación auxiliar de IP) permite la recuperación y modificación de la configuración de red del equipo local.

## <a name="where-applicable"></a>Donde sea aplicable

La API de la aplicación auxiliar IP es aplicable en cualquier entorno informático en el que sea útil manipular mediante programación la configuración de red y TCP/IP. Las aplicaciones típicas incluyen los protocolos de enrutamiento IP y los agentes del Protocolo simple de administración de redes (SNMP).

## <a name="developer-audience"></a>Audiencia de desarrolladores

La API de la aplicación auxiliar de IP está diseñada para que la usen los programadores de C/C++. Los programadores también deben estar familiarizados con las redes de Windows y los conceptos de red TCP/IP.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

La API auxiliar de IP se puede usar en todas las plataformas de Windows. No todos los sistemas operativos admiten todas las funciones. En los casos en los que existen ciertas implementaciones o funcionalidades de las restricciones de la plataforma Windows Sockets 2, se indican claramente en la documentación. Si se llama a una función auxiliar de IP en una plataforma que no admite la función, \_ se devuelve el error no \_ compatible. Para obtener información más específica acerca de los sistemas operativos que admiten una función determinada, consulte las secciones de requisitos en la documentación de.

## <a name="in-this-section"></a>En esta sección



| Tema                                                              | Descripción                                                                                                                                                                                                       |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Novedades de la aplicación auxiliar de IP](what-s-new-in-ip-helper.md)<br/>  | Información sobre las nuevas características de la aplicación auxiliar de IP.<br/>                                                                                                                                                             |
| [Acerca de la aplicación auxiliar de IP](about-ip-helper.md)<br/>                  | Información general sobre las consideraciones de programación de la aplicación auxiliar IP y las capacidades disponibles para los desarrolladores.<br/>                                                                                               |
| [Usar la aplicación auxiliar de IP](using-ip-helper.md)<br/>                  | Procedimientos y técnicas de programación que se usan con la aplicación auxiliar de IP. Esta sección incluye técnicas básicas de programación de aplicaciones auxiliares de IP, como [Introducción con la aplicación auxiliar de IP](getting-started-with-ip-helper.md).<br/> |
| [Referencia de aplicación auxiliar IP](ip-helper-function-reference.md)<br/> | Documentación de referencia de las funciones auxiliares de IP, estructuras y enumeraciones.<br/>                                                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Sockets 2](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[Servicio de acceso remoto y enrutamiento](../rras/routing-start-page.md)
</dt> </dl>

 

