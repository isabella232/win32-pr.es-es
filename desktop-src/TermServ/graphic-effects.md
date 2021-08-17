---
title: Efectos gráficos
description: Lista de características que se deben deshabilitar al ejecutarse como una sesión remota en un Servicios de Escritorio remoto remoto.
ms.assetid: 229a1058-acba-4d4b-ba52-824dda4f91a5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cad01bb7b61c471ba81f382d1fc4031b8c44dcef63a78c5a0cc17641b5e457e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059443"
---
# <a name="graphic-effects"></a>Efectos gráficos

Un Servicios de Escritorio remoto servidor se basa en la red para transmitir todas las entradas y salidas a sus terminales cliente. Por lo tanto, las aplicaciones que hacen un uso excesivo de los efectos gráficos pueden afectar al rendimiento de todos los Servicios de Escritorio remoto clientes mediante la ralentización de la red. Además, la velocidad de transmisión más lenta a través de una red podría hacer que estos efectos especiales parezcan menos agradables de lo que serían en un entorno de vídeo local.

En concreto, las aplicaciones deben deshabilitar o minimizar el uso de las siguientes características al ejecutarse en un entorno Servicios de Escritorio remoto como sesión remota:

-   Pantallas de presentación: información gráfica del producto o de la empresa que se muestra mientras se inicia una aplicación. La transmisión de una pantalla de presentación a un cliente Conexión a Escritorio remoto (RDC) consume ancho de banda de red adicional y obliga al usuario a esperar antes de acceder a la aplicación.
-   Animaciones, que consumen tiempo de CPU y ancho de banda de red.
-   Entrada o salida directas a la pantalla. Si necesita leer bits de la pantalla, mantenga una copia independiente y fuera de pantalla del búfer de vídeo. Del mismo modo, si necesita realizar una salida de pantalla elaborado (por ejemplo, superponer varias imágenes para que lleguen a una pantalla compuesta final), haga que funcione en un búfer fuera de la pantalla y, a continuación, envíe los resultados al búfer de vídeo real.

Para obtener más información sobre la detección de sesiones remotas, vea [Detecting the Servicios de Escritorio remoto Environment](detecting-the-terminal-services-environment.md).

Use la biblioteca Microsoft Foundation Class, o MFC, siempre que sea posible. MFC tiene una larga lista de clases intentadas y verdaderas para realizar una amplia variedad de tareas. La mayoría de estas clases funcionan bien en un entorno Servicios de Escritorio remoto, normalmente mucho mejor que las soluciones de nueva ingeniería. Un buen ejemplo es la clase que proporciona texto de ayuda contextual, texto de ayuda que aparece en pantalla cuando el puntero del mouse mantiene el puntero sobre un botón o elemento de menú. Si una aplicación usa la implementación de MFC para proporcionar esta característica, funcionará razonablemente bien en el sistema de escritorio. Sin embargo, si la aplicación implementa esta característica mediante cuadros de diálogo o un enfoque alternativo, es posible que el resultado final no funcione también en un Servicios de Escritorio remoto trabajo.

 

 




