---
title: Aplicaciones de inicio
description: Aplicaciones de inicio
ms.assetid: 3519CB52-A6EC-4819-87FE-C144801BDD9F
keywords:
- aplicación de inicio
- Tarea en segundo plano
- Tecla ejecutar
- RunOnce
- carpeta de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a12f01dac073712512206a5c432561b4a0b75e
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "103797122"
---
# <a name="startup-apps"></a>Aplicaciones de inicio

## <a name="platform"></a>Plataforma

**Clientes**   de   Windows 8  


## <a name="description"></a>Descripción

Una de las grandes e/////////////////////////////////////////// Para asegurarse de que nuestros clientes mutuos tengan una gran experiencia en cualquier factor de forma que elijan con Windows, dos métricas de éxito clave que deben abordarse son una mayor duración de la batería y una excelente capacidad de respuesta del equipo. Para lograrlo, se han realizado mejoras en varias áreas de Windows, como el ciclo de vida de proceso, los Estados de suspensión y las aplicaciones de inicio (aplicaciones con inicio automatizado después del arranque de la máquina). En este tema se resaltan algunos de los impactos que tienen las aplicaciones de inicio en un dispositivo Windows y se proporciona orientación a los desarrolladores (ISV/IHV) y los OEM para que reconsideren los patrones de uso de las aplicaciones de inicio con el fin de mejorar la duración de la batería y la capacidad de respuesta de nuestros clientes mutuos. También describe los cambios en Windows que ponen a los usuarios en el control de cómo determinar qué aplicaciones de inicio realmente se ejecutan.

Las aplicaciones de la tienda Windows están diseñadas para cumplir con los nuevos estándares de consumo de la batería y capacidad de respuesta, y Windows administra su ciclo de vida mediante su suspensión o terminación. Sin embargo, las aplicaciones de escritorio diseñadas para versiones anteriores de Windows no se han diseñado necesariamente para conservar la duración de la batería o son sensibles a la actividad del usuario, y pueden afectar a la capacidad de respuesta del sistema (por ejemplo, cuando una aplicación envía un latido de 1 segundo normal para comprobar si hay actualizaciones, o preasigna la memoria por delante en caso de que la necesite). Esto puede crear una experiencia deficiente para el usuario que adquiere un equipo con Windows Tablet PC con una larga esperanza de duración de la batería y semanas de espera, pero detecta la duración de la batería de Tablet PC no logra estos objetivos. Además, dado que las aplicaciones de inicio se ejecutan en segundo plano, el número de aplicaciones que se ejecutan en el sistema puede ser mucho mayor de lo que el usuario es consciente y que afecta a la capacidad de respuesta del sistema. Las aplicaciones de inicio se clasifican para incluir las que aprovechan estos mecanismos para iniciarse:

-   Ejecutar claves del registro (nodos HKLM, HKCU, WOW64 incluidos)
-   Claves del registro de RunOnce
-   Carpetas de inicio en el menú Inicio para cada usuario y ubicación pública

Se ha agregado una nueva funcionalidad a Windows para garantizar que los usuarios finales siempre controlen las aplicaciones que se ejecutan en sus sistemas. En la pestaña Inicio del administrador de tareas se muestra una lista de aplicaciones de inicio, junto con controles que permiten a los usuarios deshabilitar las aplicaciones de inicio. Para ayudar a los usuarios a determinar qué deshabilitar, el administrador de tareas muestra una medida de cada impacto de la aplicación de inicio. El impacto se calcula en función del uso de la CPU y del disco de la aplicación en el inicio. Los valores de impacto se determinan aplicando estos criterios:

-   **Gran impacto**   Aplicaciones que usan más de un segundo de tiempo de CPU o más de 3 MB de e/s de disco en el inicio
-   **Impacto medio**   Aplicaciones que usan 300 ms-1000 ms de tiempo de CPU o 300 KB-3 MB de e/s de disco
-   **Impacto bajo**   Aplicaciones que usan menos de 300 ms de tiempo de CPU y menos de 300 KB de e/s de disco

Microsoft proporciona herramientas para ayudar a los desarrolladores de aplicaciones a evaluar, analizar y tomar medidas para reducir su impacto en el inicio y mejorar la experiencia del usuario. El kit de evaluación e implementación proporciona la capacidad de ejecutar una evaluación del rendimiento de arranque y medir el impacto de las aplicaciones que se ejecutan en el inicio. Los resultados de la evaluación contienen análisis detallados e información de corrección, si procede, para los componentes de mayor impacto en el inicio de Windows. Con el analizador de rendimiento de Windows, los desarrolladores de aplicaciones pueden realizar análisis profundos para encontrar la causa raíz del impacto en el rendimiento y mejorar el rendimiento de inicio de Windows. Instale Windows ADK desde [aquí](/previous-versions/windows/hh825494(v=win.10)).

## <a name="guidance"></a>Instrucciones

Las aplicaciones de inicio abarcan varias categorías, como se describe en la tabla siguiente. Un conjunto de recomendaciones para desarrolladores se asigna a las categorías de aplicaciones de inicio para que se alineen con los cambios funcionales de Windows descritos anteriormente.



Categorías de aplicaciones de inicio

Descripción

Recomendación

**Actualizadores**

Supervisar y actualizar usuarios para actualizaciones en línea

**Tarea de mantenimiento**

> [!Note]  
> Todas las actualizaciones deben ser tareas de mantenimiento, sin requisitos de interacción con la interfaz de usuario. Las aplicaciones solo deben actualizarse de modo silencioso y revertir en caso de error

<br/>

$ {ROWSPAN2} $**asistencia de hardware**$ {Remove} $  

Puntos de acceso alternativos

Proporcionar acceso a las características y aplicaciones de Windows a las que se puede acceder a través de otros puntos de acceso de Windows

**Remove**

> [!Note]  
> La clave consiste en reducir las características duplicadas que existen en Windows

<br/>

Notificadores

Proporcionar a los usuarios notificaciones acerca de sus dispositivos

**Remove**

> [!Note]  
> Windows proporciona notificaciones a los usuarios acerca de sus dispositivos

<br/>

**Iniciadores previos**

Algunas de las actividades preliminares necesarias para las aplicaciones se descargan en una aplicación de inicio durante el inicio de sesión del usuario

**Remove**

> [!Note]  
> Windows 8 está optimizado para una experiencia rápida para los lanzamientos de aplicaciones.

<br/>

$ {ROWSPAN4} $**utilidad**$ {Remove} $  

Sincronización de PC

Proporcionar funcionalidad de sincronización en varios sistemas

**Inicio** (actualizaciones potenciales en la versión beta)

Copia de seguridad y recuperación

Punto de entrada para guardar y restaurar el estado de los archivos, la configuración o los sistemas completos

**Aplicación de la tienda Windows para interactuar con los usuarios**

Telemetría

Recopile y envíe información sobre la experiencia del usuario y el entorno

**Tarea de mantenimiento**

Supervisión de equipos

Proporcionar supervisión de estado del sistema no solicitada y notificaciones que dupliquen la funcionalidad de bandeja de entrada existente

**Remove**

> [!Note]  
> La clave consiste en reducir las características duplicadas que existen en Windows

<br/>

$ {ROWSPAN2} $**Security**$ {Remove} $  

Filtros de & de control parental

Aplicar reglas y restricciones establecidas para el acceso y el uso de Internet

**Startup**

Configuración y administración

Permitir a los usuarios controlar las opciones de diagnóstico y corrección para la supervisión de la seguridad del sistema notificar a los usuarios de los hallazgos y las acciones de seguridad

**Aplicación de la tienda Windows para interactuar con los usuarios**

**Comunicación & Internet** (im & VoIP)

Envío y recepción de mensajes y llamadas

**Aplicación de la tienda Windows**

**Música & MP3**

Reproducir, almacenar y administrar música

**Aplicación de la tienda Windows**

**Vídeo de & de fotos**

Detección, registro, representación, almacenamiento y administración de fotos y vídeos

**Aplicación de la tienda Windows**

**Juegos de equipos**

Iniciar juegos en varios dominios

**Aplicación de la tienda Windows**

**& anuncio de venta incremental**

Atraer la atención a los productos y servicios disponibles para su compra

**Remove**



 

> [!Note]  
> Las directrices de las aplicaciones de accesibilidad están descubridas por las interacciones directas con los ISV. Consulte [*programación para facilitar el acceso*](../winauto/ease-of-access---assistive-technology-registration.md) para obtener más información.

 

**Aplicaciones de la Tienda Windows**

Las aplicaciones de la tienda Windows mejoran la experiencia del usuario al introducir un espacio de Windows con nuevas coordenadas: un nuevo modelo de aplicación, una nueva interfaz de usuario y una tienda Windows. Estas opciones de lenguaje y presentación están disponibles para desarrollar aplicaciones de la tienda Windows:

-   HTML/JavaScript/CSS
-   XAML/C #
-   XAML/C++

La información agregada para desarrollar aplicaciones de la tienda Windows está disponible en el [centro de desarrollo de Windows](https://msdn.microsoft.com/windows/apps/).

Ejemplos:

-   [Desarrollo de juegos de la tienda Windows](/previous-versions/windows/apps/hh452744(v=win.10))
-   [Desarrollo de una aplicación de la tienda Windows que usa medios](/previous-versions/windows/apps/hh465132(v=win.10))

**Tareas de mantenimiento automático**

La actividad en segundo plano periódica debe diseñarse como tareas de mantenimiento automático. Se programan en tiempo de inactividad del sistema para aumentar la capacidad de respuesta y la eficiencia energética de los equipos Windows. Las tareas de mantenimiento pueden crearse y configurarse con una aplicación de escritorio en el momento de la instalación, mediante el SDK de escritorio. Consulte el tema de mantenimiento automático que se muestra a continuación para obtener más información.

## <a name="resources"></a>Recursos

-   [Directrices de accesibilidad](../winauto/ease-of-access---assistive-technology-registration.md)
-   [Centro de desarrollo de Windows](https://msdn.microsoft.com/windows/apps/)
-   [Windows ADK](/previous-versions/windows/hh825494(v=win.10))

 

