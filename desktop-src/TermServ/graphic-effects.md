---
title: Efectos gráficos
description: Una lista de características que deben deshabilitarse cuando se ejecuta como una sesión remota en un entorno de Servicios de Escritorio remoto.
ms.assetid: 229a1058-acba-4d4b-ba52-824dda4f91a5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711f850b8bac5d084419b1f15c2e0efe619da5b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994271"
---
# <a name="graphic-effects"></a>Efectos gráficos

Un servidor de Servicios de Escritorio remoto se basa en la red para transmitir todas las entradas y salidas a sus terminales de cliente. Por lo tanto, las aplicaciones que hacen un uso excesivo de efectos gráficos pueden afectar al rendimiento de todos los clientes Servicios de Escritorio remoto ralentizando la red. Además, la velocidad de transmisión más lenta a través de una red puede hacer que estos efectos especiales parezcan menos agradables que en un entorno de vídeo local.

En concreto, las aplicaciones deben deshabilitar o minimizar el uso de las características siguientes cuando se ejecutan en un entorno de Servicios de Escritorio remoto como una sesión remota:

-   Pantallas de presentación: información gráfica del producto o de la compañía que se muestra mientras se inicia una aplicación. La transmisión de una pantalla de presentación a un cliente de Conexión a Escritorio remoto (RDC) consume ancho de banda de red adicional y obliga al usuario a esperar antes de tener acceso a la aplicación.
-   Animaciones, que consumen tanto el tiempo de CPU como el ancho de banda de red.
-   Entrada o salida directa en la pantalla. Si necesita leer bits de la pantalla, mantenga una copia independiente y fuera de la pantalla del búfer de vídeo. Del mismo modo, si necesita realizar una salida de pantalla elaborada (por ejemplo, superponiendo varias imágenes para llegar a una pantalla compuesta final), hágalo en un búfer fuera de pantalla y, a continuación, envíe los resultados al búfer de vídeo real.

Para obtener más información acerca de cómo detectar sesiones remotas, consulte [detectar el entorno de servicios de escritorio remoto](detecting-the-terminal-services-environment.md).

Use la biblioteca MFC (Microsoft Foundation Class) o MFC siempre que sea posible. MFC tiene una larga lista de clases probadas y verdaderas para realizar una amplia variedad de tareas. La mayoría de estas clases funcionan bien en un entorno de Servicios de Escritorio remoto, normalmente mucho mejor que las soluciones que se vuelven a diseñar. Un buen ejemplo es la clase que proporciona texto de ayuda contextual, el texto de ayuda que aparece en la pantalla cuando el puntero del mouse se desplaza sobre un botón o un elemento de menú. Si una aplicación utiliza la implementación de MFC para proporcionar esta característica, funcionará bastante bien en el sistema de escritorio. Pero si la aplicación implementa esta característica mediante el uso de cuadros de diálogo o un enfoque alternativo, el resultado final podría no funcionar también en un entorno de Servicios de Escritorio remoto.

 

 




