---
description: Procedimientos recomendados para la eficiencia energética
ms.assetid: 355abd0e-928e-442e-a724-855d9dd946fc
title: Procedimientos recomendados para la eficiencia energética
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d9a348b9df49531358de2db50acc0936622c36
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088393"
---
# <a name="best-practices-for-energy-efficiency"></a>Procedimientos recomendados para la eficiencia energética

## <a name="platform"></a>Plataforma

 **Clientes:** Windows XP \| Windows Vista Windows \| 7  

## <a name="description"></a>Descripción

Los equipos portátiles basados en Windows deben cumplir los requisitos normativos de eficiencia energética, como los del programa energy star Estados Unidos Environmental Protection Agency (ENERGY Star). Además, las encuestas han demostrado que una mayor duración de la batería sigue siendo lo que más quieren y necesitan los consumidores en los portátiles. Para satisfacer las demandas de los consumidores, los equipos portátiles Windows deben avanzar continuamente en las siguientes áreas:

-   Eficiencia energética en todos los escenarios de uso, incluidas las cargas de trabajo inactivas, las cargas de trabajo de productividad, la reproducción de DVD y multimedia, y las pruebas comparativas del sector
-   Duración de la batería de pc móvil: para plataformas de hardware y para Windows

La plataforma Windows es altamente confiable y permite un rendimiento rápido de inicio y apagado. Sin embargo, las extensiones proporcionadas con sistemas de PC móviles, como servicios, applets de bandeja del sistema, controladores y otro software, pueden afectar significativamente al rendimiento, la confiabilidad y la eficiencia energética.

La eficiencia energética es un problema complejo, con factores afectados por y que afectan a todos los elementos del ecosistema de PC. Las pequeñas mejoras en varios escenarios pueden mejorar la eficiencia energética, pero una única característica de aplicación, dispositivo o sistema de bajo rendimiento puede aumentar significativamente el consumo de energía.

El hardware y los dispositivos forman la base de la eficiencia energética. Sin embargo, el software de aplicación y servicio también debe ser eficaz para permitir que el sistema alcance una duración óptima de la batería. Cada componente de software del sistema, incluidos el sistema operativo y las aplicaciones y servicios de valor agregado, deben cumplir las directrices básicas de eficiencia. Una única aplicación o servicio que se comporta de forma errónea puede eliminar las mejoras de eficiencia energética que se lograron con el procesador, los dispositivos o el hardware de la plataforma más recientes. Para obtener información más detallada sobre la duración de la batería y la eficiencia energética, consulte la Guía de soluciones [de duración de la batería](https://docs.microsoft.com/windows-hardware/design/component-guidelines/battery-and-charging#).

Los principales problemas y componentes que afectan a la duración de la batería en un equipo móvil son:

**Características de la batería**

-   El tamaño, el tipo y la calidad de la capacidad de la batería afectan a la duración de la batería
-   Cuanto mayor sea la batería, mayor será la fuente de alimentación.
-   Las baterías más grandes son más costosas y pesadas. los usuarios prefieren sistemas más ligeros

**Componentes de hardware**

-   Frecuencia y profundidad a la que el hardware puede entrar en estados de energía inferiores
-   Compatibilidad de hardware con estados de energía inferiores
-   Optimización del controlador para la eficiencia energética

**Administración de energía dirigida por el sistema operativo**

-   Eficiencia del código de Windows mientras está bajo una carga frente a inactivo
-   Nivel de cooperación de todos los componentes con la administración de energía dirigida a Windows
-   Configuración adecuada del sistema operativo para optimizar la administración de energía a través de la configuración de la directiva de energía

**Software y servicios de aplicaciones**

-   Eficiencia de las aplicaciones, los controladores y los servicios mientras se está bajo una carga frente a la inactividad
-   Nivel de cooperación de las aplicaciones con administración de energía dirigida a Windows
-   Concesión de software del sistema o dispositivos para entrar en estados inactivos de bajo consumo de energía

Un único componente de aplicación o servicio puede impedir que un sistema se dé cuenta de una duración óptima de la batería. Aunque Windows proporciona muchas opciones de configuración de energía, la configuración de directivas de energía o software preinstalada en muchos sistemas no está optimizada para la plataforma de hardware del host.

Un método común para evaluar el impacto de la duración de la batería del software preinstalado es comparar el consumo de energía del sistema con una instalación limpia de Windows frente a una instalación de Windows que incluye software y servicios de valor añadido. Aunque una instalación limpia no representa la plataforma típica que los OEM envían a los clientes, la comparación del consumo de energía puede proporcionar información sobre la eficiencia energética del software preinstalado.

## <a name="best-practices"></a>Prácticas recomendadas

Para asegurarse de que la aplicación está optimizada en plataformas Windows, siga estos procedimientos recomendados al diseñar aplicaciones o servicios:

-   **Evitar el uso de temporizadores periódicos de alta resolución**

<dl> Uso de temporizadores periódicos de alta resolución (<10 ms) reduces the efficiency of processor power-management technologies.  
</dl>

-   **Invertir en optimizaciones de rendimiento**

<dl> Cada optimización del rendimiento es una optimización de la duración de la batería. Las reducciones en los recursos necesarios, como el uso de menos tiempo de procesador o las lecturas de disco de procesamiento por lotes o agrupación en clústeres, permiten que el hardware del sistema se vuelva inactivo y entre en modos de bajo consumo.  
</dl>

-   **Ajuste a la directiva de energía del usuario**

<dl> Windows Vista y versiones posteriores hacen que sea fácil para el usuario elegir el ahorro de energía general o el comportamiento del rendimiento del sistema. La aplicación debe responder a los cambios en la directiva de energía y reducir el uso de recursos o aumentar el rendimiento en consecuencia. Por ejemplo, una aplicación debe deshabilitar la actividad en segundo plano, como la indexación o el examen del sistema, cuando el usuario ha seleccionado un plan de energía de ahorro de energía.  
</dl>

-   **Reducir el uso de recursos cuando el sistema está encendido por batería**

<dl> La aplicación debe reducir su uso de recursos(por ejemplo, la frecuencia de actualización en segundo plano) cuando el sistema está encendido por batería.  
</dl>

-   **No representar en la pantalla cuando está desactivada**

<dl> La pantalla del sistema podría estar desactivada para ahorrar energía. La aplicación no debe realizar una representación de gráficos innecesaria cuando la pantalla está desactivada porque esto desperdicia los recursos y la energía del sistema.  
</dl>

-   **Evitar el sondeo y el giro en bucles ajustados**

<dl> El uso de procesadores pesados reduce la eficacia de las tecnologías de administración de energía del procesador, como los estados de inactividad del procesador y los estados de rendimiento del procesador.  
</dl>

-   **No impida que el sistema apague la pantalla o se apague.**

<dl> La aplicación debe realizar solicitudes de energía con la API SetThreadExecutionState. El sistema debe realizar estas solicitudes solo cuando las operaciones críticas deba retrasar el apagado del sistema de la pantalla o de entrar automáticamente en suspensión.  
</dl>

-   **Respuesta a eventos comunes de administración de energía**

<dl> La aplicación debe registrarse y responder a eventos comunes de administración de energía, como cambios en el origen de energía del sistema y notificaciones de encendido y apagado para la pantalla.  
</dl>

-   **No habilite el registro de depuración de forma predeterminada; use Seguimiento de eventos para Windows en su lugar**

<dl> El registro de depuración periódico puede impedir la rotación del disco.  
</dl>

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [Guía de soluciones de duración de la batería](https://docs.microsoft.com/windows-hardware/design/component-guidelines/battery-and-charging#)
-   [Portal de eficiencia energética](https://www.microsoft.com/whdc/system/pnppwr/mobilepwr.mspx)
-   [Kit de herramientas de rendimiento de Windows](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)

 

 



