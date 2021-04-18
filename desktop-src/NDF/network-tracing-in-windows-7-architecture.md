---
title: Seguimiento de red en la arquitectura de Windows 7
description: En la ilustración siguiente se muestra la arquitectura básica de seguimiento de red en Windows 7.
ms.assetid: b3023469-0f98-451c-b39f-c3eae771eacc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41221ebf434c05a8c9b7c8489e861128029b5320
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676495"
---
# <a name="network-tracing-in-windows-7-architecture"></a>Seguimiento de red en Windows 7: arquitectura

En la ilustración siguiente se muestra la arquitectura básica de seguimiento de red en Windows 7.

![diagrama de la arquitectura de seguimiento de red](images/ut1.png)

El seguimiento de red emplea el marco de seguimiento de eventos para Windows (ETW) disponible en Windows. Los componentes de red (como Winsock, TCP/IP, NDIS, captura de paquetes, etc.) se registran como proveedores de seguimiento de ETW y emiten eventos relacionados con la actividad de red. Cualquier actividad grabable de importancia puede ser un evento registrado en ETW. El seguimiento de estos componentes de red y capturas de paquetes se puede habilitar mediante el contexto de **seguimiento de Netsh** que actúa como controlador ETW.

Los seguimientos generados se recopilan en un archivo de registro de seguimiento de eventos (ETL). A continuación, estos archivos ETL se pueden analizar mediante una serie de herramientas, como Monitor de red 3,2 y versiones posteriores, Visor de eventos, la **conversión de seguimiento de Netsh** o Tracerpt.exe.

Cada evento ETW tiene un encabezado común donde ETW almacena información como las propiedades del evento, las marcas de tiempo y el ID. de actividad. (Para obtener más información acerca de los identificadores de actividad, consulte [escribir eventos relacionados en un escenario de un extremo a otro](../etw/writing-related-events-in-an-end-to-end-scenario.md)). El ID. de actividad se usa para correlacionar eventos. En el modo de usuario, los identificadores de actividad se almacenan en subprocesos y todos los eventos registrados en un subproceso se etiquetarán automáticamente con el mismo ID. de actividad. En el modo kernel, el ID. de actividad se debe pasar explícitamente cuando se registra un evento. De forma predeterminada, los archivos ETL se correlacionan con los eventos de grupo juntos en los identificadores de actividad específicos.

Para obtener más información sobre los eventos de Windows y ETW, vea [eventos de Windows](../events/windows-events.md).

## <a name="etw-components-in-network-tracing"></a>Componentes de ETW en el seguimiento de red

El seguimiento de red usa ETW como mecanismo de seguimiento principal para proporcionar información acerca de lo que hacen los subsistemas de red. Hay cuatro componentes principales en ETW: sesiones de seguimiento de eventos, proveedores de eventos, controladores de eventos y consumidores de eventos.

El almacenamiento en búfer y el registro tienen lugar en *sesiones de seguimiento de eventos*, que aceptan eventos de proveedores y crean archivos de seguimiento.

Un *proveedor de eventos* es una entidad lógica que escribe los eventos en las sesiones de ETW. Un proveedor de eventos puede ser una aplicación de modo de usuario, una aplicación administrada, un controlador o cualquier otra entidad de software. Los proveedores de eventos se registran con ETW y escriben eventos de varios puntos en el código mediante la invocación de la API de registro de ETW. Debido a la instrumentación de eventos en aumento en muchos componentes del sistema operativo, incluso una aplicación o un escenario sencillos de Windows contendrán varios componentes que son proveedores de eventos.

Un *controlador de eventos* inicia y detiene las sesiones de seguimiento de eventos y habilita los proveedores. Cuando la aplicación del controlador de eventos habilita un proveedor de eventos de forma dinámica, el proveedor envía eventos a una sesión de seguimiento de eventos específica designada por el controlador de eventos. Cada evento enviado por el proveedor de eventos a la sesión de seguimiento de eventos está compuesto de un encabezado fijo, que incluye metadatos de evento y cualquier dato personalizado adicional registrado por el proveedor.

Un *consumidor de eventos* es una aplicación que lee los archivos de registro o que escucha una sesión de seguimiento de eventos para los eventos en tiempo real y los procesa. Un ejemplo de consumidor de eventos es Monitor de red de Microsoft 3,2, que incluye la capacidad de leer y mostrar los archivos de registro generados por el seguimiento de red en Windows 7.

Los eventos se entregan a los consumidores de eventos en orden cronológico, y hay varias aplicaciones de consumidor de eventos que muestran los eventos en formatos concretos. Cuando se registra un evento en una sesión, ETW agrega información adicional al encabezado del evento, incluidos los datos de la marca de tiempo, el proceso y el identificador del subproceso, el número de procesador y los datos de uso de CPU del subproceso de registro. Después, estos datos se pasan a los consumidores de eventos, junto con los datos personalizados que incluye el proveedor.

Se espera que los proveedores que usan las nuevas [API de registro de eventos](/windows/win32/api/evntprov/nf-evntprov-eventwrite) suministren un archivo XML denominado manifiesto de [evento](../wes/eventschema-schema.md). Este archivo proporciona metadatos para definir todos los datos personalizados e información de diseño para los eventos escritos por el proveedor. Después, una aplicación de consumidor de uso general utiliza las API del [ayudante de datos de seguimiento (TDH)](/windows/win32/api/tdh/) para recuperar los metadatos del evento, descodificar los eventos y mostrarlos.

Con el seguimiento de red en Windows 7, el lado del controlador de eventos o del consumidor incluye compatibilidad con el seguimiento basado en escenarios de un extremo a otro integrado con las experiencias generales de diagnóstico y soporte técnico de Windows. Un escenario define una colección de proveedores de eventos implicados en el escenario. El lado del controlador de eventos/consumidor define los escenarios (contextos) en los que se puede usar el seguimiento, incluidos los proveedores pertinentes para los escenarios determinados en los componentes de red. El lado del proveedor de eventos incluye eventos de seguimiento de red normalizados de distintos componentes de la pila de red, que se pueden correlacionar a través de identificadores de actividad de ETW. Los proveedores usan un esquema de red común que normaliza el uso de conceptos de ETW como palabras clave, niveles, tareas y códigos de procedimientos. El esquema también define eventos que son comunes para muchos componentes de red como eventos de error, eventos de eliminación de paquetes, eventos de esquema y eventos de transición de estado.

 

 