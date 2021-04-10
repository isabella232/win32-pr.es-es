---
description: Windows Sockets 2 (Winsock) permite a los programadores crear aplicaciones avanzadas de Internet, intranet y otras aplicaciones compatibles con redes para transmitir datos de la aplicación a través de la conexión, independientemente del Protocolo de red que se use.
ms.assetid: 1ec8758a-40fd-4c98-b839-c2409ef712d6
title: Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df253572d2fca117dbc8b45b451f8c3bacc2f360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155256"
---
# <a name="windows-sockets-2"></a>Windows Sockets 2

## <a name="purpose"></a>Propósito

Windows Sockets 2 (Winsock) permite a los programadores crear aplicaciones avanzadas de Internet, intranet y otras aplicaciones compatibles con redes para transmitir datos de la aplicación a través de la conexión, independientemente del Protocolo de red que se use. Con Winsock, se proporciona a los programadores acceso a funciones avanzadas de redes de Microsoft® Windows®, como la multidifusión y la calidad de servicio (QoS).

Winsock sigue el modelo de Windows Open System Architecture (WOSA). define una interfaz de proveedor de servicios estándar (SPI) entre la interfaz de programación de aplicaciones (API), con sus funciones exportadas y las pilas de protocolos. Usa el paradigma de sockets que se ha usado por primera vez en Berkeley Software Distribution (BSD) UNIX. Más adelante se adaptaba a Windows en Windows Sockets 1,1, con el que las aplicaciones de Windows Sockets 2 son compatibles con versiones anteriores. Programación de Winsock previamente centrada en torno a TCP/IP. Algunas prácticas de programación que funcionan con TCP/IP no funcionan con todos los protocolos. Como resultado, la API de Windows Sockets 2 agrega funciones cuando sea necesario para controlar varios protocolos.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Windows Sockets 2 está diseñado para que lo usen los programadores de C/C++. Es necesario estar familiarizado con las redes de Windows.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Windows Sockets 2 se puede usar en todas las plataformas de Windows. En los casos en los que existen ciertas implementaciones o funcionalidades de las restricciones de la plataforma Windows Sockets 2, se indican claramente en la documentación.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                             | Descripción                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Novedades de Windows Sockets](what-s-new-for-windows-sockets-2.md)<br/>                 | Información sobre las nuevas características de Windows Sockets.<br/>                                                                                                                                                                                                                                 |
| [Compatibilidad del Protocolo de red Winsock en Windows](network-protocol-support-in-windows.md)<br/> | Información sobre la compatibilidad del Protocolo de red con Windows Sockets en diferentes versiones de Windows.<br/>                                                                                                                                                                                    |
| [Acerca de Winsock](about-winsock.md)<br/>                                                     | Información general sobre las consideraciones, la arquitectura y las capacidades de programación de Windows Sockets disponibles para los desarrolladores.<br/>                                                                                                                                                       |
| [Usar WinSock](using-winsock.md)<br/>                                                     | Procedimientos y técnicas de programación que se usan con Windows Sockets. Esta sección incluye técnicas básicas de programación de Winsock, como [Introducción con Winsock](getting-started-with-winsock.md), así como técnicas avanzadas útiles para los desarrolladores de Winsock con experiencia.<br/> |
| [Referencia de Winsock](winsock-reference.md)<br/>                                             | Documentación de la API de Windows Sockets.<br/>                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asistente IP](../iphlp/ip-helper-start-page.md)
</dt> <dt>

[Calidad de servicio](/previous-versions/windows/desktop/qos/qos-start-page)
</dt> </dl>

 

 
