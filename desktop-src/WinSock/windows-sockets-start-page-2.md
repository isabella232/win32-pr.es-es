---
description: Windows Sockets 2 (Winsock) permite a los programadores crear aplicaciones avanzadas de Internet, intranet y otras aplicaciones compatibles con la red para transmitir datos de aplicación a través de la conexión, independientemente del protocolo de red que se esté utilizando.
ms.assetid: 1ec8758a-40fd-4c98-b839-c2409ef712d6
title: Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df253572d2fca117dbc8b45b451f8c3bacc2f360
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967272"
---
# <a name="windows-sockets-2"></a>Windows Sockets 2

## <a name="purpose"></a>Propósito

Windows Sockets 2 (Winsock) permite a los programadores crear aplicaciones avanzadas de Internet, intranet y otras aplicaciones compatibles con la red para transmitir datos de aplicación a través de la conexión, independientemente del protocolo de red que se esté utilizando. Con Winsock, a los programadores se les proporciona acceso a funcionalidades de red avanzadas de Microsoft® Windows® como multidifusión y calidad de servicio (QoS).

Winsock sigue el Windows arquitectura de sistema abierto (WOSA). define una interfaz de proveedor de servicios (SPI) estándar entre la interfaz de programación de aplicaciones (API), con sus funciones exportadas y las pilas de protocolos. Usa el paradigma de sockets que fue popularizado por primera vez por La distribución de software de Berkeley (BSD) UNIX. Más adelante se adaptó para Windows en Windows Sockets 1.1, con el que las aplicaciones Windows Sockets 2 son compatibles con versiones anteriores. La programación de Winsock anteriormente se centraba en TCP/IP. Algunas prácticas de programación que funcionaban con TCP/IP no funcionan con todos los protocolos. Como resultado, la API Windows Sockets 2 agrega funciones cuando sea necesario para controlar varios protocolos.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Windows Sockets 2 está diseñado para su uso por programadores de C/C++. Es necesario estar Windows con las redes.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Windows Los sockets 2 se pueden usar en todas Windows plataformas. Cuando existen ciertas implementaciones o funcionalidades de Windows sockets 2, se anotan claramente en la documentación.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                             | Descripción                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Novedades de Windows Sockets](what-s-new-for-windows-sockets-2.md)<br/>                 | Información sobre las nuevas características de Windows Sockets.<br/>                                                                                                                                                                                                                                 |
| [Compatibilidad con el protocolo de red winsock en Windows](network-protocol-support-in-windows.md)<br/> | Información sobre la compatibilidad del protocolo de red Windows Sockets en diferentes versiones de Windows.<br/>                                                                                                                                                                                    |
| [Acerca de Winsock](about-winsock.md)<br/>                                                     | Información general sobre las consideraciones Windows programación, la arquitectura y las funcionalidades de sockets disponibles para los desarrolladores.<br/>                                                                                                                                                       |
| [Uso de Winsock](using-winsock.md)<br/>                                                     | Procedimientos y técnicas de programación que se usan Windows Sockets. En esta sección se incluyen técnicas de programación básicas de Winsock, como [Tareas iniciales With Winsock,](getting-started-with-winsock.md)así como técnicas avanzadas útiles para desarrolladores experimentados de Winsock.<br/> |
| [Referencia de Winsock](winsock-reference.md)<br/>                                             | Documentación de Windows Sockets API.<br/>                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asistente IP](../iphlp/ip-helper-start-page.md)
</dt> <dt>

[Calidad de servicio](/previous-versions/windows/desktop/qos/qos-start-page)
</dt> </dl>

 

 
