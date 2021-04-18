---
description: .
ms.assetid: 872c2a33-327e-41a8-81db-905c46673f13
title: Prácticas recomendadas para el rendimiento activado/desactivado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fda45cb1ec7fb66b8afdcdebab7c92bdb071a79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717134"
---
# <a name="best-practices-for-onoff-performance"></a>Prácticas recomendadas para el rendimiento activado/desactivado

## <a name="platform"></a>Plataforma

**Clientes-** Windows Vista \| Windows 7  
**Servidores:** Windows Server 2008 \| Windows server 2008 R2  

## <a name="description"></a>Descripción

Los Estados de energía del sistema (o Estados S), tal y como se define en la especificación de la interfaz avanzada de energía de equipo (ACPI), se suele denominan Estados ON/OFF, ya que la transición de estado S más común es un equipo que se activa y desactiva. Las transiciones de estado ON/OFF diferentes en un sistema que ejecuta Windows Vista o Windows 7 son el arranque, la suspensión (ACPI S3), hibernación (ACPI S4) y el apagado.

Un buen rendimiento durante estas transiciones ON/OFF no solo mejora la calidad percibida de un equipo, sino que también afecta en gran medida a los patrones de uso del equipo y la confiabilidad del sistema diarios. Los clientes pueden ser frustrados por los sistemas que tardan demasiado tiempo en arrancarse o cerrarse. Los sistemas móviles que tienen transiciones largas de suspensión e hibernación pueden agotar innecesariamente la duración de la batería. Las horas de apagado más largas también pueden afectar negativamente a la confiabilidad de los sistemas móviles. Por ejemplo, aumentan el riesgo de que se produzcan cortes de energía inesperados.

Las extensiones del sistema como los controladores, las aplicaciones y los servicios pueden tener un impacto significativo en los tiempos de transición ON/OFF. En esta sección se describen algunas de las prácticas recomendadas que los desarrolladores de aplicaciones y servicios pueden seguir para evitar retrasos durante el arranque, el modo de espera y el apagado, y para garantizar una experiencia de usuario posterior al arranque y posterior a la reanudación. Para obtener más información sobre cómo identificar problemas de rendimiento activados o desactivados con el kit de herramientas de rendimiento de Windows e implementar las recomendaciones siguientes para su aplicación o servicio, consulte las notas del producto en la sección "vínculos a otros recursos".

## <a name="best-practices"></a>Prácticas recomendadas

-   Use el kit de herramientas de rendimiento de Windows para medir el rendimiento durante todas las transiciones de encendido o apagado.
-   Realizar pruebas de forma controlada y realizar comparaciones con una línea base válida:
    -   Obtener una medida de base de referencia en un sistema con el menor número de extensiones del sistema posibles
    -   Agregar aplicaciones y servicios de uno en uno
    -   Prueba de regresiones no aceptables en los tiempos de transición ON/OFF
-   Evite el uso de código administrado para aplicaciones en la ruta de acceso de arranque crítica.
-   Asegúrese de que todas las aplicaciones responden rápidamente a las notificaciones de cierre ( \_ mensajes WM QUERYENDSESSION y WM \_ ENDSESSION).
-   Reduzca los retrasos en la ruta de acceso de apagado de servicios y aplicaciones minimizando la actividad de la CPU, el disco y la red en respuesta a las notificaciones de cierre.
-   Evite retrasos en el procesamiento de la notificación de suspensión (mensaje de POWERBROADCAST de WM \_ ).
-   Responda rápidamente para reanudar eventos y minimizar el uso posterior de la CPU, el disco y la red.
-   Reduzca el consumo de recursos de la aplicación después del arranque.
-   No inicie aplicaciones desde la clave RunOnce en cada arranque.
-   Convierta todos los servicios no esenciales en Inicio de petición o en iniciar desencadenador para que los recursos del sistema estén disponibles durante el arranque.
-   Evite el uso de grupos de pedidos de carga para expresar las dependencias de servicio.
-   Asegúrese de que todos los servicios en ejecución informan de este estado lo antes posible durante el arranque para evitar el bloqueo del administrador de control de servicios (SCM).
-   Evite el uso de código administrado para servicios en la ruta de acceso de inicio.
-   No permita que los servicios participen para recibir notificaciones de apagado y cierre (códigos de control de cierre de control de servicio y apagado de control de servicio \_ \_ \_ \_ ) a menos que sea absolutamente necesario.
-   Asegúrese de que todos los servicios que han optado por recibir notificaciones de apagado responden rápidamente al SCM.
-   Compruebe que los servicios no participen para recibir notificaciones de suspensión a menos que sea absolutamente necesario.
-   Asegúrese de que todos los servicios responden rápidamente para reanudar eventos y minimizar el uso posterior de la CPU, el disco y la red.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   -   [Guía de soluciones de las transiciones de Windows on/off](/windows-hardware/test/assessments/onoff-transition-performance)
-   [Análisis de rendimiento de transición activado o desactivado de Windows Vista](/windows-hardware/test/assessments/onoff-transition-performance)
-   [Análisis de rendimiento de Windows](https://msdn.microsoft.com/performance/default.aspx)
-   [Documentación del kit de herramientas de rendimiento de Windows en MSDN](/previous-versions/windows/desktop/xperf/windows-performance-analyzer--wpa-)
-   [Foro de análisis de rendimiento de Windows](https://social.msdn.microsoft.com/Forums/wptk_v4/threads/)
-   [Seguimiento de eventos para Windows en MSDN](../etw/event-tracing-portal.md)

 

 
