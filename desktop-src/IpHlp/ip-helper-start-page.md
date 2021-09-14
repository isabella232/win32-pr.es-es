---
description: La API del asistente de protocolos de Internet (asistente de IP) permite la recuperación y modificación de los valores de configuración de red para el equipo local.
ms.assetid: 4896a9f8-0486-4380-bf49-d1c9ef114acc
title: Asistente de IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1d50153e1ad890063f33a473058f6a850a9f171
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272519"
---
# <a name="ip-helper"></a>Asistente de IP

## <a name="purpose"></a>Propósito

La API del asistente de protocolos de Internet (asistente de IP) permite la recuperación y modificación de los valores de configuración de red para el equipo local.

## <a name="where-applicable"></a>Donde sea aplicable

La API del asistente de IP es aplicable en cualquier entorno informático en el que sea útil manipular la red mediante programación y la configuración de TCP/IP. Las aplicaciones típicas incluyen protocolos de enrutamiento IP y agentes de Protocolo simple de administración de redes (SNMP).

## <a name="developer-audience"></a>Audiencia de desarrolladores

La API del asistente de IP está diseñada para su uso por los programadores de C/C++. Los programadores también deben estar familiarizados con los Windows de red y de redes TCP/IP.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

La API del asistente de IP se puede usar en todas Windows plataformas. No todos los sistemas operativos admiten todas las funciones. Cuando existen ciertas implementaciones o funcionalidades de Windows sockets 2 de la plataforma, se anotan claramente en la documentación. Si se llama a una función auxiliar de IP en una plataforma que no admite la función, se devuelve ERROR \_ NOT \_ SUPPORTED. Para obtener información más específica sobre qué sistemas operativos admiten una función determinada, consulte las secciones Requisitos de la documentación.

## <a name="in-this-section"></a>En esta sección



| Tema                                                              | Descripción                                                                                                                                                                                                       |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Novedades del asistente de IP](what-s-new-in-ip-helper.md)<br/>  | Información sobre las nuevas características del asistente de IP.<br/>                                                                                                                                                             |
| [Acerca del asistente de IP](about-ip-helper.md)<br/>                  | Información general sobre las consideraciones y funcionalidades de programación del asistente de IP disponibles para los desarrolladores.<br/>                                                                                               |
| [Uso del asistente de IP](using-ip-helper.md)<br/>                  | Procedimientos y técnicas de programación que se usan con el asistente de IP. En esta sección se incluyen técnicas básicas de programación del asistente de IP, como [Tareas iniciales con el asistente de IP](getting-started-with-ip-helper.md).<br/> |
| [Referencia de aplicación auxiliar IP](ip-helper-function-reference.md)<br/> | Documentación de referencia para las funciones, estructuras y enumeraciones del asistente de IP.<br/>                                                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Sockets 2](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[Servicio de acceso remoto y enrutamiento](../rras/routing-start-page.md)
</dt> </dl>

 

