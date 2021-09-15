---
title: Aplicaciones de inicio
description: Aplicaciones de inicio
ms.assetid: 3519CB52-A6EC-4819-87FE-C144801BDD9F
keywords:
- aplicación de inicio
- Tarea en segundo plano
- Clave de ejecución
- RunOnce
- carpeta de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a12f01dac073712512206a5c432561b4a0b75e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466267"
---
# <a name="startup-apps"></a>Aplicaciones de inicio

## <a name="platform"></a>Plataforma

**Clientes Windows 8**     


## <a name="description"></a>Descripción

Una de las grandes opciones con Windows es la capacidad de encender varios factores de forma, desde los equipos de escritorio y portátiles tradicionales hasta las tabletas de bajo consumo. Para asegurarse de que nuestros clientes mutuos tienen una gran experiencia en cualquier factor de forma que elijan con Windows, dos métricas clave de éxito que deben abordarse son una mayor duración de la batería y una excelente capacidad de respuesta del equipo. Para lograrlos, se han realizado mejoras en varias áreas de Windows incluido el ciclo de vida del proceso, los estados de suspensión y las aplicaciones de inicio (aplicaciones con inicio automatizado después del arranque de la máquina). En este tema se resaltan algunos de los efectos que tienen las aplicaciones de inicio en un dispositivo Windows y se proporcionan instrucciones a los desarrolladores (ISV/IHV) y los OEM para que replanteen los patrones de uso de las aplicaciones de inicio con el fin de mejorar la duración de la batería y la capacidad de respuesta de nuestros clientes mutuos. También se describen los cambios en Windows que ponen a los usuarios en el control de determinar qué aplicaciones de inicio se pueden ejecutar realmente.

Windows Las aplicaciones de la tienda están diseñadas para cumplir los nuevos estándares de consumo y capacidad de respuesta de la batería, y Windows administra su ciclo de vida suspendiendo o finalizando. Sin embargo, las aplicaciones de escritorio diseñadas para versiones anteriores de Windows no se han diseñado necesariamente para conservar la duración de la batería o ser sensibles a la actividad del usuario, y pueden afectar a la capacidad de respuesta del sistema (por ejemplo, cuando una aplicación envía un latido normal de 1 segundo para comprobar si hay actualizaciones o asigna previamente memoria por adelantado en caso de que la necesite más adelante). Esto puede crear una experiencia deficiente para el usuario que compra un pc de tableta Windows con una larga duración de la batería y semanas de espera, pero detecta que la duración de la batería de la tableta no logra estos objetivos. Además, dado que las aplicaciones de inicio se ejecutan en segundo plano, el número de aplicaciones que se ejecutan en el sistema puede ser significativamente mayor que lo que el usuario conoce y afectar a la capacidad de respuesta del sistema. Las aplicaciones de inicio se clasifican para incluir aquellas que aprovechan estos mecanismos para empezar:

-   Ejecutar claves del Registro (hklm, HKCU, nodos wow64 incluidos)
-   Claves del Registro RunOnce
-   Carpetas de inicio en el menú inicio para ubicaciones públicas y de usuario

Se ha agregado nueva funcionalidad a Windows asegurarse de que los usuarios finales siempre tienen el control de las aplicaciones que se ejecutan en sus sistemas. La pestaña Inicio de Administrador de tareas muestra una lista de aplicaciones de inicio, junto con controles que permiten a los usuarios deshabilitar las aplicaciones de inicio. Para ayudar a los usuarios a determinar qué deshabilitar, Administrador de tareas muestra una medida del impacto de cada aplicación de inicio. El impacto se evalúa en función del uso de la CPU y el disco de una aplicación en el inicio. Los valores de impacto se determinan mediante la aplicación de estos criterios:

-   **Alto impacto**   Aplicaciones que usan más de 1 segundo de tiempo de CPU o más de 3 MB de E/S de disco en el inicio
-   **Impacto medio**   Aplicaciones que usan 300 ms - 1000 ms de tiempo de CPU o 300 KB - 3 MB de E/S de disco
-   **Bajo impacto**   Aplicaciones que usan menos de 300 ms de tiempo de CPU y menos de 300 KB de E/S de disco

Microsoft proporciona herramientas para ayudar a los desarrolladores de aplicaciones a evaluar, analizar y tomar medidas para reducir su impacto en el inicio y mejorar la experiencia del usuario. El Kit de evaluación e implementación proporciona la capacidad de ejecutar una evaluación del rendimiento de arranque y medir el impacto de las aplicaciones que se ejecutan en el inicio. Los resultados de la evaluación contienen información detallada de análisis y corrección, si procede, para los componentes de mayor impacto en Windows inicio. Con el Windows Analizador de rendimiento, los desarrolladores de aplicaciones pueden realizar análisis profundos para encontrar la causa principal del impacto en el rendimiento y mejorar Windows de inicio. Instale el Windows ADK desde [aquí.](/previous-versions/windows/hh825494(v=win.10))

## <a name="guidance"></a>Instrucciones

Las aplicaciones de inicio abarcan varias categorías, como se describe en la tabla siguiente. Un conjunto de recomendaciones para desarrolladores se asigna a las categorías de aplicaciones de inicio para alinearse con los Windows funcionales descritos anteriormente.



Categorías de aplicaciones de inicio

Descripción

Recomendación

**Actualizadores**

Supervisión y actualización de usuarios para actualizaciones en línea

**Tarea de mantenimiento**

> [!Note]  
> Todas las actualizaciones deben ser tareas de mantenimiento, sin requisitos de interacción con la interfaz de usuario. Las aplicaciones solo deben actualizarse de forma silenciosa y revertir en caso de error

<br/>

${ROWSPAN2}$**Asistencia de hardware**${REMOVE}$  

Puntos de acceso alternativos

Proporcione acceso a Windows y aplicaciones que son accesibles a través de otros puntos de acceso de Windows

**Remove**

> [!Note]  
> La clave es reducir las características duplicadas que existen en Windows

<br/>

Notificadores

Proporcionar a los usuarios notificaciones relativas a sus dispositivos

**Remove**

> [!Note]  
> Windows proporciona notificaciones a los usuarios sobre sus dispositivos

<br/>

**Iniciadores previos**

Algunas de las actividades preliminares necesarias para las aplicaciones se descargan en una aplicación de inicio durante el inicio de sesión del usuario.

**Remove**

> [!Note]  
> Windows 8 está optimizado para una experiencia rápida para los inicios de aplicaciones.

<br/>

${ROWSPAN4}$**Utilidad**${REMOVE}$  

Sincronización de PC

Proporcionar funcionalidad de sincronización en varios sistemas

**Inicio** (posibles actualizaciones en beta)

Copia de seguridad y recuperación

Punto de entrada para guardar y restaurar el estado de los archivos, la configuración o todos los sistemas

**Windows Aplicación de la Tienda para la interacción con los usuarios**

Telemetría

Recopilación y envío de información sobre la experiencia y el entorno del usuario

**Tarea de mantenimiento**

Supervisión de PC

Proporcionar notificaciones y supervisión del estado del sistema no solicitados que duplican la funcionalidad de bandeja de entrada existente

**Remove**

> [!Note]  
> La clave es reducir las características duplicadas que existen en Windows

<br/>

${ROWSPAN2}$**Seguridad**${REMOVE}$  

Filtros de & control parental

Aplicación de reglas y restricciones establecidas para el acceso a Internet y el uso

**Startup**

Configuración y administración

Permitir a los usuarios controlar las opciones de diagnóstico y corrección para la supervisión de seguridad del sistema Notificar a los usuarios los resultados y las acciones de seguridad

**Windows Aplicación de la Tienda para la interacción con los usuarios**

**Comunicación & Internet** (IM & VoIP)

Envío y recepción de mensajes y llamadas

**Windows Aplicación de la Tienda**

**Música & MP3**

Reproducir, almacenar y administrar música

**Windows Aplicación de la Tienda**

**Photo & Video**

Detección, grabación, representación, almacenamiento y administración de fotos y vídeos

**Windows Aplicación de la Tienda**

**Juegos de PC**

Inicio de juegos en varios dominios

**Windows Aplicación de la Tienda**

**Anuncio de ventas & ventas**

Llamar la atención sobre los bienes y servicios disponibles para la compra

**Remove**



 

> [!Note]  
> Las directrices de las aplicaciones de accesibilidad están cubiertas por interacciones directas independientes con ISV. Vea [*Programming for Accesibilidad (Programación*](../winauto/ease-of-access---assistive-technology-registration.md) para Accesibilidad para obtener más información).

 

**Aplicaciones de la Tienda Windows**

Windows Las aplicaciones de la Tienda mejoran la experiencia del usuario mediante la introducción de un espacio Windows nuevas coordenadas: un nuevo modelo de aplicación, una nueva interfaz de usuario y una Windows Store. Estas opciones de lenguaje y marco de presentación están disponibles para desarrollar aplicaciones Windows Store:

-   HTML/JavaScript/CSS
-   XAML/C #
-   XAML/C++

La información agregada para desarrollar aplicaciones Windows Store está disponible en el [Windows Centro de desarrollo](https://msdn.microsoft.com/windows/apps/).

Ejemplos:

-   [Desarrollo de Windows Store](/previous-versions/windows/apps/hh452744(v=win.10))
-   [Desarrollo de Windows store que usan medios](/previous-versions/windows/apps/hh465132(v=win.10))

**Tareas de mantenimiento automático**

La actividad en segundo plano periódica debe diseñarse Mantenimiento automático tareas. Se programan en tiempo de inactividad del sistema para aumentar la capacidad de respuesta y la eficiencia energética de Windows equipos. Las tareas de mantenimiento se pueden crear y configurar mediante una aplicación de escritorio en el momento de la instalación, mediante el SDK de escritorio. Consulte el Mantenimiento automático siguiente para obtener más información.

## <a name="resources"></a>Recursos

-   [Directrices de accesibilidad](../winauto/ease-of-access---assistive-technology-registration.md)
-   [Centro de desarrollo de Windows](https://msdn.microsoft.com/windows/apps/)
-   [Windows ADK](/previous-versions/windows/hh825494(v=win.10))

 

