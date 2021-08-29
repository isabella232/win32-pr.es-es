---
title: Seguimiento de red en la Windows 7
description: En la ilustración siguiente se muestra la arquitectura básica de seguimiento de red Windows 7.
ms.assetid: b3023469-0f98-451c-b39f-c3eae771eacc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f23567d109da96c234fc0982746458cd54c46ef87eb4cae5158cc1b14aedeea9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801984"
---
# <a name="network-tracing-in-windows-7-architecture"></a>Seguimiento de red en Windows 7: Arquitectura

En la ilustración siguiente se muestra la arquitectura básica de seguimiento de red Windows 7.

![diagrama de arquitectura de seguimiento de red](images/ut1.png)

El seguimiento de red utiliza el marco de seguimiento de eventos Windows (ETW) disponible en Windows. Los componentes de red (como Winsock, TCP/IP, NDIS, captura de paquetes, etc.) se registran como proveedores de seguimiento ETW y emiten eventos relacionados con la actividad de red. Cualquier actividad registrable de importancia puede ser un evento registrado en ETW. El seguimiento de estos componentes de red y capturas de paquetes se puede habilitar mediante el **contexto de seguimiento netsh** que actúa como controlador ETW.

Los seguimientos generados se recopilan en un archivo de registro de seguimiento de eventos (ETL). Estos archivos ETL se pueden analizar mediante una serie de herramientas, como Monitor de red 3.2 y versiones posteriores, Visor de eventos, **netsh trace convert** o Tracerpt.exe.

Cada evento ETW tiene un encabezado común donde ETW almacena información como las propiedades del evento, las marcas de tiempo y el identificador de actividad. (Para obtener más información sobre los IDs de actividad, vea Escribir eventos relacionados en un escenario [de un extremo a otro).](../etw/writing-related-events-in-an-end-to-end-scenario.md) El identificador de actividad se usa para correlacionar eventos. En el modo de usuario, los identificadores de actividad se almacenan en subprocesos y todos los eventos registrados en un subproceso se etiquetarán automáticamente con el mismo identificador de actividad. En el modo kernel, el identificador de actividad se debe pasar explícitamente cuando se registra un evento. De forma predeterminada, los archivos ETL se correlacionan con eventos de grupo juntos en los IDs de actividad específicos.

Para obtener más información sobre Windows Events y ETW, vea [Windows Events](../events/windows-events.md).

## <a name="etw-components-in-network-tracing"></a>Componentes de ETW en el seguimiento de red

El seguimiento de red usa ETW como mecanismo de seguimiento principal para proporcionar información sobre lo que hacen los subsistemas de red. Hay cuatro componentes principales en ETW: sesiones de seguimiento de eventos, proveedores de eventos, controladores de eventos y consumidores de eventos.

El almacenamiento en búfer y el registro tienen lugar en sesiones *de seguimiento de* eventos , que aceptan eventos de proveedores y crean archivos de seguimiento.

Un *proveedor de eventos* es una entidad lógica que escribe eventos en sesiones ETW. Un proveedor de eventos puede ser una aplicación en modo de usuario, una aplicación administrada, un controlador o cualquier otra entidad de software. Los proveedores de eventos se registran con ETW y escriben eventos desde varios puntos del código mediante la invocación de la API de registro de ETW. Debido al aumento de la instrumentación de eventos en muchos componentes del sistema operativo, incluso una aplicación o un escenario simple en Windows contendrá varios componentes que son proveedores de eventos.

Un controlador *de eventos* inicia y detiene las sesiones de seguimiento de eventos y habilita los proveedores. Cuando la aplicación del controlador de eventos habilita dinámicamente un proveedor de eventos, este envía eventos a una sesión de seguimiento de eventos específica designada por el controlador de eventos. Cada evento enviado por el proveedor de eventos a la sesión de seguimiento de eventos consta de un encabezado fijo, que incluye metadatos de eventos y cualquier dato personalizado adicional registrado por el proveedor.

Un *consumidor de eventos* es una aplicación que lee archivos de registro o que escucha una sesión de seguimiento de eventos para eventos en tiempo real y los procesa. Un ejemplo de consumidor de eventos es Monitor de red de Microsoft 3.2, que incluye la capacidad de leer y mostrar los archivos de registro generados por el seguimiento de red en Windows 7.

Los eventos se entregan a los consumidores de eventos en orden cronológico y hay varias aplicaciones de consumidor de eventos que muestran los eventos en formatos específicos. Cuando se registra un evento en una sesión, ETW agrega información adicional al encabezado del evento, incluida la marca de tiempo, el identificador de proceso y de subproceso, el número de procesador y los datos de uso de CPU del subproceso de registro. A continuación, estos datos se pasan a los consumidores de eventos, junto con los datos personalizados incluidos por el proveedor.

Se espera que los proveedores que usan las [nuevas API](/windows/win32/api/evntprov/nf-evntprov-eventwrite) de registro de eventos proporcionen un archivo XML denominado manifiesto [de evento](../wes/eventschema-schema.md). Este archivo proporciona metadatos para definir todos los datos personalizados y la información de diseño de los eventos escritos por el proveedor. Después, una aplicación consumidora de uso general usa las API del asistente de datos de seguimiento [(TDH)](/windows/win32/api/tdh/) para recuperar los metadatos del evento, descodificar los eventos y mostrarlos.

Con el seguimiento de red en Windows 7, el lado controlador de eventos o consumidor incluye compatibilidad de seguimiento basada en escenarios de un extremo a otro integrada con experiencias generales de diagnóstico y soporte técnico de Windows. Un escenario define una colección de proveedores de eventos implicados en el escenario. El lado controlador de eventos o consumidor define los escenarios (contextos) en los que se puede usar el seguimiento, incluidos los proveedores pertinentes para escenarios determinados en los componentes de red. El lado del proveedor de eventos incluye eventos de seguimiento de red estandarizados de diferentes componentes de la pila de red, que se pueden correlacionar a través de los IDs de actividad ETW. Los proveedores usan un esquema de red común que estandariza el uso de conceptos de ETW como palabras clave, niveles, tareas y códigos de operación. El esquema también define eventos comunes para muchos componentes de red, como eventos de error, eventos de colocación de paquetes, eventos de esquema y eventos de transición de estado.

 

 