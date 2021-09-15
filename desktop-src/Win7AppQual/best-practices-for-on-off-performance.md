---
description: Procedimientos recomendados para el rendimiento de encendido y apagado
ms.assetid: 872c2a33-327e-41a8-81db-905c46673f13
title: Procedimientos recomendados para el rendimiento de encendido y apagado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c88eaf5175db43061e57bc4689d8bf256e6881
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571037"
---
# <a name="best-practices-for-onoff-performance"></a>Procedimientos recomendados para el rendimiento de encendido y apagado

## <a name="platform"></a>Plataforma

**Clientes:** Windows Vista \| Windows 7  
**Servidores:** Windows Server 2008 \| Windows Server 2008 R2  

## <a name="description"></a>Descripción

Los estados de energía del sistema (o estados S), tal como se define en la especificación de advanced computer power interface (ACPI), se denominan coloquialmente estados de encendido y apagado, ya que la transición de estado S más común es un equipo que se encienda y apague. Las distintas transiciones de estado de encendido y apagado en un sistema que ejecuta Windows Vista o Windows 7 son arranque, suspensión (ACPI S3), hibernación (ACPI S4) y apagado.

Un buen rendimiento durante estas transiciones de encendido y apagado no solo mejora la calidad percibida de un equipo, sino que también afecta en gran medida a los patrones de uso diario del equipo y a la confiabilidad del sistema. Los clientes pueden sentirse frustrados por sistemas que tarden demasiado tiempo en arrancarse o apagarse. Los sistemas móviles que tienen transiciones de suspensión e hibernación largas pueden agotar innecesariamente la duración de la batería. Los tiempos de apagado más largos también pueden afectar negativamente a la confiabilidad de los sistemas móviles. Por ejemplo, aumentan el riesgo de cortes de energía inesperados.

Las extensiones del sistema como controladores, aplicaciones y servicios pueden tener un impacto significativo en los tiempos de transición de encendido y apagado. En esta sección se de abordan algunos de los procedimientos recomendados que los desarrolladores de aplicaciones y servicios pueden seguir para evitar retrasos durante el arranque, el modo de espera y el apagado, y para garantizar una experiencia de usuario posterior al arranque y posterior a la reanudación. Para obtener más información sobre cómo identificar los problemas de rendimiento de encendido y apagado mediante el Toolkit de rendimiento de Windows e implementar las siguientes recomendaciones para la aplicación o el servicio, consulte las whitepapers de la sección "Vínculos a otros recursos".

## <a name="best-practices"></a>Prácticas recomendadas

-   Use el Windows rendimiento Toolkit para medir el rendimiento durante todas las transiciones de encendido y apagado.
-   Realice pruebas de forma controlada y realice comparaciones con una línea base válida:
    -   Obtención de una medida de línea base en un sistema con el menor número de extensiones del sistema posible
    -   Agregar aplicaciones y servicios de una en una
    -   Prueba de regresiones inaceptables en los tiempos de transición de encendido y apagado
-   Evite el uso de código administrado para aplicaciones en la ruta de acceso de arranque crítica.
-   Asegúrese de que todas las aplicaciones responden rápidamente a las notificaciones de cierre (mensajes \_ WM QUERYENDSESSION y WM \_ ENDSESSION).
-   Reduzca los retrasos en la ruta de acceso de apagado de servicios y aplicaciones minimizando la actividad de CPU, disco y red en respuesta a las notificaciones de apagado.
-   Evite retrasos en el procesamiento de la notificación de suspensión (mensaje \_ DE WM POWERBROADCAST).
-   Responda rápidamente para reanudar eventos y minimizar el uso posterior a la CPU, el disco y la red.
-   Reducir el consumo de recursos de aplicación después del arranque.
-   No inicie aplicaciones desde la clave RunOnce en cada arranque.
-   Convierta todos los servicios no esenciales en iniciar o desencadenar a petición para que los recursos del sistema estén disponibles durante el arranque.
-   Evite el uso de grupos de pedidos de carga para expresar las dependencias del servicio.
-   Asegúrese de que todos los servicios en ejecución informan de este estado tan pronto como sea posible durante el arranque para evitar el bloqueo de Service Control Manager (SCM).
-   Evite el uso de código administrado para los servicios en la ruta de inicio.
-   No permita que los servicios opten por recibir notificaciones de apagado previo y apagado (códigos de \_ control SERVICE CONTROL PRESHUTDOWN y SERVICE CONTROL SHUTDOWN) a menos que sea \_ \_ \_ absolutamente necesario.
-   Asegúrese de que todos los servicios que han optado por recibir notificaciones de cierre respondan rápidamente al SCM.
-   Compruebe que los servicios no opten por recibir notificaciones de suspensión a menos que sea absolutamente necesario.
-   Asegúrese de que todos los servicios responden rápidamente para reanudar eventos y minimizar el uso posterior a la CPU, el disco y la red.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   -   [Windows Guía de soluciones de transiciones de encendido y apagado](/windows-hardware/test/assessments/onoff-transition-performance)
-   [On/Off Transition Performance Analysis of Windows Vista](/windows-hardware/test/assessments/onoff-transition-performance)
-   [Windows Análisis de rendimiento](https://msdn.microsoft.com/performance/default.aspx)
-   [Windows Documentación de Toolkit rendimiento en MSDN](/previous-versions/windows/desktop/xperf/windows-performance-analyzer--wpa-)
-   [Windows Foro de análisis de rendimiento](https://social.msdn.microsoft.com/Forums/wptk_v4/threads/)
-   [Seguimiento de eventos para Windows en MSDN](../etw/event-tracing-portal.md)

 

 
