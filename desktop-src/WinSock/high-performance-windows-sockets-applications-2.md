---
description: Los componentes de red de Microsoft Windows se han desarrollado para el rendimiento y la escalabilidad.
ms.assetid: 2160b93e-c126-4592-972c-d9cc14eec745
title: Aplicaciones de Windows Sockets de alto rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0496198ef3a8f11e6a840fd75d0083899d23d5a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082120"
---
# <a name="high-performance-windows-sockets-applications"></a>Aplicaciones de Windows Sockets de alto rendimiento

Los componentes de red de Microsoft Windows se han desarrollado para el rendimiento y la escalabilidad. Esto permite a las aplicaciones maximizar el ancho de banda de red disponible. Se han optimizado y simplificado Windows Sockets y la pila del protocolo TCP/IP de Windows. Como resultado, las aplicaciones de Windows escritas correctamente pueden conseguir un rendimiento y rendimiento excepcionales, como se muestra en los siguientes aspectos:

-   Windows es capaz de dar servicio a más de 200.000 conexiones TCP simultáneas.
-   En una prueba realizada por SPECWeb96, Internet Information Server en Windows se ha puesto en servicio en 25.000 solicitudes HTTP por segundo.
-   Windows establece un registro de transmisión de sobre 750Mbps en una red Gigabit de Transcontinental que consta de 10 saltos.

Estos logros muestran que Windows TCP/IP procesa los datos con mucha rapidez. Sin embargo, muchas aplicaciones no aprovechan las capacidades de rendimiento de Windows, TCP/IP y Windows Sockets porque implementan inconscientemente técnicas que dificultan el rendimiento.

En esta guía, aprenderá a identificar errores de programación comunes y cómo evitarlos. A continuación, aprenderá técnicas que permiten que las aplicaciones de Windows Sockets funcionen de forma óptima. Esta guía se presenta en seis secciones. El orden de las secciones es intencionado; para sacar el máximo partido de esta guía, debe leerlo en orden. En la tabla siguiente se proporcionan vínculos a cada sección, así como una breve descripción de cada tema.



| Tema                                                                                            | Descripción                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Terminología de red](network-terminology-2.md)                                                 | Define la terminología y las métricas de red necesarias para comprender el rendimiento de una aplicación de red.                                     |
| [Dimensiones de rendimiento](performance-dimensions-2.md)                                           | Describe las dimensiones de rendimiento que afectan al rendimiento de red percibido y real de una aplicación.                                        |
| [Características de TCP/IP](tcp-ip-characteristics-2.md)                                           | Define las características del protocolo TCP/IP que pueden producir problemas de rendimiento en una aplicación mal escrita.                                     |
| [Comportamiento de la aplicación](application-behavior-2.md)                                               | Explica cómo reconocer los signos de una aplicación de red con un rendimiento deficiente.                                                                     |
| [Mejora de una aplicación lenta](improving-a-slow-application-2.md)                               | Proporciona ejemplos de problemas de diseño de aplicaciones que contribuyen a una aplicación de bajo rendimiento y realiza cambios en el código para mejorar el rendimiento. |
| [Prácticas recomendadas para aplicaciones interactivas](best-practices-for-interactive-applications-2.md) | Enumera los procedimientos recomendados que se emplean para desarrollar aplicaciones de red interactivas óptimas.                                                         |



 

 

 



