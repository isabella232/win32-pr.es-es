---
description: .
ms.assetid: 355abd0e-928e-442e-a724-855d9dd946fc
title: Prácticas recomendadas para la eficiencia energética
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a9980d199e2d95c6dbd01c642a1f00f45e584c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697780"
---
# <a name="best-practices-for-energy-efficiency"></a>Prácticas recomendadas para la eficiencia energética

## <a name="platform"></a>Plataforma

 **Clientes** : Windows XP Windows \| vista Windows \| 7  

## <a name="description"></a>Descripción

Los equipos portátiles basados en Windows deben cumplir con los requisitos normativos de eficiencia energética, como los del programa de Estados Unidos Energy Star de la Agencia de protección ambiental (EPA). Además, las encuestas han demostrado que la mayor duración de la batería sigue siendo lo que los consumidores más desean y necesitan en los equipos portátiles. Para satisfacer las demandas de los consumidores, los equipos portátiles de Windows deben avanzar continuamente en las áreas siguientes:

-   Eficiencia energética en todos los escenarios de uso, como inactivos, cargas de trabajo de productividad, reproducción de DVD y medios y pruebas comparativas del sector
-   Duración de la batería del PC móvil: para plataformas de hardware y para Windows

La plataforma de Windows es muy confiable y permite un rendimiento rápido y sin interrupción. Sin embargo, las extensiones proporcionadas con sistemas de PC móviles, como los servicios, las applets de la bandeja del sistema, los controladores y otro software, pueden afectar significativamente al rendimiento, la confiabilidad y la eficacia energética.

La eficiencia energética es un problema complejo, con factores afectados por y que afectan a todos los elementos del ecosistema de PC. Las pequeñas mejoras en varios escenarios pueden mejorar la eficacia de la energía, pero una sola aplicación, dispositivo o característica del sistema de bajo rendimiento puede aumentar considerablemente el consumo energético.

El hardware y los dispositivos constituyen la base de la eficacia energética. Sin embargo, el software de aplicación y servicio también debe ser eficaz para permitir que el sistema alcance la duración óptima de la batería. Cada componente de software del sistema, incluido el sistema operativo y las aplicaciones y servicios de valor agregado, debe cumplir las directrices básicas de eficiencia. Una sola aplicación o servicio con un comportamiento incorrecto puede eliminar cualquier mejora de la eficacia energética que el procesador, los dispositivos o el hardware de la plataforma más recientes alcanzaron. Para obtener información más detallada acerca de la duración de la batería y la eficiencia energética, consulte la [Guía de soluciones](https://docs.microsoft.com/windows-hardware/design/component-guidelines/battery-and-charging#)de batería.

Los principales problemas y componentes que afectan a la duración de la batería en un PC móvil son los siguientes:

**Características de la batería**

-   El tamaño, el tipo y la calidad de la capacidad de la batería afectan a la duración de la batería
-   Cuanto mayor sea la batería, mayor será la fuente de alimentación.
-   Las baterías mayores son más caras y más pesadas. los usuarios prefieren sistemas más claros

**Componentes de hardware**

-   Frecuencia y profundidad en las que el hardware puede entrar en Estados de energía inferiores
-   Compatibilidad de hardware con Estados de energía inferiores
-   Optimización del controlador para la eficiencia energética

**Sistema operativo: administración de energía dirigida**

-   Eficiencia del código de Windows en lugar de una carga frente a mientras está inactivo
-   Nivel de cooperación de todos los componentes con la administración de energía dirigida a Windows
-   Configuración adecuada del sistema operativo para optimizar la administración de energía mediante la configuración de la Directiva de energía

**Software y servicios de aplicaciones**

-   Eficacia de las aplicaciones, los controladores y los servicios mientras se encuentran en una carga frente a mientras están inactivos
-   Nivel de cooperación de las aplicaciones con la administración de energía dirigida a Windows
-   Asignación de software del sistema o de los dispositivos para entrar en Estados inactivos de baja energía

Un único componente de aplicación o servicio puede impedir que un sistema presente una duración óptima de la batería. Aunque Windows proporciona muchas opciones de configuración de energía, el software preinstalado o la configuración de la Directiva de energía en muchos sistemas no están optimizados para la plataforma de hardware del host.

Un método común para evaluar el impacto en la batería del software preinstalado es comparar el consumo de energía del sistema con una instalación limpia de Windows frente a una instalación de Windows que incluye software y servicios de valor añadido. Aunque una instalación limpia no representa la plataforma típica que los OEM envían a los clientes, la comparación del consumo de energía puede proporcionar información sobre la eficacia energética del software preinstalado.

## <a name="best-practices"></a>Prácticas recomendadas

Para asegurarse de que la aplicación está optimizada en las plataformas de Windows, siga estas prácticas recomendadas al diseñar aplicaciones o servicios:

-   **Evitar el uso de temporizadores periódicos de alta resolución**

<dl> Usar temporizadores periódicos de alta resolución (<10 ms) reduces the efficiency of processor power-management technologies.  
</dl>

-   **Invertir en optimizaciones de rendimiento**

<dl> Cada optimización de rendimiento es una optimización de la duración de la batería. Las reducciones en los recursos necesarios, como el uso de menos tiempo de procesador o el procesamiento por lotes o las lecturas de disco de agrupación en clústeres, permiten que el hardware del sistema se vuelva inactivo y escriba modos de baja energía.  
</dl>

-   **Ajustar a la Directiva de energía de usuario**

<dl> Windows Vista y versiones posteriores facilitan al usuario la elección del ahorro de energía general o el comportamiento del rendimiento del sistema. La aplicación debe responder a los cambios en la Directiva de energía y reducir el uso de recursos o aumentar el rendimiento en consecuencia. Por ejemplo, una aplicación debe deshabilitar la actividad en segundo plano como la indexación o el análisis del sistema cuando el usuario ha seleccionado un plan de energía de ahorro de energía.  
</dl>

-   **Reducir el uso de recursos cuando el sistema tiene energía de batería**

<dl> La aplicación debe reducir el uso de recursos, como la frecuencia de actualización en segundo plano, cuando el sistema tiene energía de batería.  
</dl>

-   **No representar en la pantalla cuando está desactivada**

<dl> La pantalla del sistema podría estar desactivada para el ahorro de energía. La aplicación no debe llevar a cabo una representación de gráficos innecesaria cuando la pantalla está desactivada, ya que esto desperdicia recursos del sistema y energía.  
</dl>

-   **Evite el sondeo y el giro en bucles estrechos**

<dl> El uso intensivo del procesador reduce la eficacia de las tecnologías de administración de energía del procesador, como Estados inactivos del procesador y Estados de rendimiento del procesador.  
</dl>

-   **No evitar que el sistema desactive la pantalla o el ralentí en suspensión**

<dl> La aplicación debe hacer solicitudes de energía sensatas con la API de SetThreadExecutionState. El sistema debe realizar estas solicitudes solo cuando las operaciones críticas deben retrasar el apagado del sistema o entrar en suspensión automáticamente.  
</dl>

-   **Respuesta a eventos comunes de administración de energía**

<dl> La aplicación debe registrarse y responder a los eventos comunes de administración de energía, como los cambios de origen de alimentación del sistema y las notificaciones de encendido y apagado de la pantalla.  
</dl>

-   **No habilite el registro de depuración de forma predeterminada; usar el seguimiento de eventos para Windows en su lugar**

<dl> El registro de depuración periódico puede impedir la desactivación del disco.  
</dl>

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [Guía de soluciones de batería](https://docs.microsoft.com/windows-hardware/design/component-guidelines/battery-and-charging#)
-   [Portal de eficiencia energética](https://www.microsoft.com/whdc/system/pnppwr/mobilepwr.mspx)
-   [Kit de herramientas de rendimiento de Windows](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)

 

 



