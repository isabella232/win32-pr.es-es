---
description: Los componentes Windows de red de Microsoft se han desarrollado para mejorar el rendimiento y la escalabilidad.
ms.assetid: 2160b93e-c126-4592-972c-d9cc14eec745
title: Aplicaciones de sockets de Windows alto rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0496198ef3a8f11e6a840fd75d0083899d23d5a2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063977"
---
# <a name="high-performance-windows-sockets-applications"></a>Aplicaciones de sockets de Windows alto rendimiento

Los componentes Windows de red de Microsoft se han desarrollado para mejorar el rendimiento y la escalabilidad. Esto permite a las aplicaciones maximizar el ancho de banda de red disponible. Windows Los sockets y la Windows pila del protocolo TCP/IP se han optimizado y optimizado. Como resultado, las aplicaciones de Windows correctamente escritas pueden lograr un rendimiento y un rendimiento excepcionales, como se muestra en los hechos siguientes:

-   Windows es capaz de atender más de 200 000 conexiones TCP simultáneas.
-   En una prueba realizada por SPECWeb96, Internet Information Server en Windows atendidas más de 25 000 solicitudes HTTP por segundo.
-   Windows un registro de transmisión de más de 750 Mbps en una red gigabit trans gigabit que consta de 10 saltos.

Estos logros ilustran que Windows TCP/IP procesa los datos muy rápidamente. Sin embargo, muchas aplicaciones no aprovechan las funcionalidades de rendimiento Windows, TCP/IP y Windows Sockets porque, sin saberlo, implementan técnicas que dificultan el rendimiento.

En esta guía, aprenderá a identificar errores de programación comunes y a evitarlos. A continuación, aprenderá técnicas que permiten que las Windows Sockets se ejecuten de forma óptima. Esta guía se presenta en seis secciones. El orden de las secciones es intencionado; Para sacar el máximo partido de esta guía, léala en orden. En la tabla siguiente se proporcionan vínculos a cada sección, así como una breve descripción de cada tema.



| Tema                                                                                            | Descripción                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Terminología de red](network-terminology-2.md)                                                 | Define la terminología de red y las métricas necesarias para comprender el rendimiento de una aplicación de red.                                     |
| [Dimensiones de rendimiento](performance-dimensions-2.md)                                           | Describe las dimensiones de rendimiento que afectan al rendimiento de red percibido y real de una aplicación.                                        |
| [Características de TCP/IP](tcp-ip-characteristics-2.md)                                           | Define las características del protocolo TCP/IP que pueden dar lugar a problemas de rendimiento para una aplicación mal escrita.                                     |
| [Comportamiento de la aplicación](application-behavior-2.md)                                               | Explica cómo reconocer los signos de una aplicación de red con un rendimiento deficiente.                                                                     |
| [Mejora de una aplicación lenta](improving-a-slow-application-2.md)                               | Proporciona ejemplos de problemas de diseño de aplicaciones que contribuyen a una aplicación con un rendimiento deficiente y realiza cambios en el código para mejorar el rendimiento. |
| [Procedimientos recomendados para aplicaciones interactivas](best-practices-for-interactive-applications-2.md) | Enumera los procedimientos recomendados que se deben emplear para desarrollar aplicaciones de red interactivas óptimas.                                                         |



 

 

 



