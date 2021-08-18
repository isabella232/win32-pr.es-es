---
description: Hay cinco tipos de eventos que se pueden registrar. Todos ellos tienen datos comunes bien definidos y, opcionalmente, pueden incluir datos específicos del evento.
ms.assetid: 4ab4a284-a4cd-4cf7-a9d2-e4a75fce01b9
title: Tipos de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e94ae69445f660e54c630734b93297acad593c127f32b9d3abfa94f9cd2fc06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069565"
---
# <a name="event-types"></a>Tipos de eventos

Hay cinco tipos de eventos que se pueden registrar. Todos ellos tienen datos comunes bien definidos y, opcionalmente, pueden incluir datos específicos del evento.

La aplicación indica el tipo de evento cuando notifica un evento. Cada evento debe ser de un solo tipo. El Visor de eventos muestra un icono diferente para cada tipo en la vista de lista del registro de eventos.

En la tabla siguiente se describen los cinco tipos de eventos usados en el registro de eventos.



| Tipo de evento        | Descripción                                                                                                                                                                                                                                                                                              |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Error**         | Evento que indica un problema importante, como la pérdida de datos o la pérdida de funcionalidad. Por ejemplo, si un servicio no se carga durante el inicio, se registra un evento Error.                                                                                                                           |
| **Advertencia**       | Evento que no es necesariamente significativo, pero puede indicar un posible problema futuro. Por ejemplo, cuando el espacio en disco es bajo, se registra un evento Advertencia. Si una aplicación puede recuperarse de un evento sin pérdida de funcionalidad ni datos, generalmente puede clasificarlo como un evento de advertencia.     |
| **Información**   | Evento que describe el funcionamiento correcto de una aplicación, controlador o servicio. Por ejemplo, cuando un controlador de red se carga correctamente, puede ser adecuado registrar un evento de información. Tenga en cuenta que, por lo general, una aplicación de escritorio no puede registrar un evento cada vez que se inicia. |
| **Auditoría de aciertos** | Evento que registra un intento de acceso de seguridad auditado que se realiza correctamente. Por ejemplo, el intento correcto de un usuario de iniciar sesión en el sistema se registra como un evento De auditoría correcta.                                                                                                                        |
| **Auditoría de errores** | Evento que registra un intento de acceso de seguridad auditado que produce un error. Por ejemplo, si un usuario intenta acceder a una unidad de red y produce un error, el intento se registra como un evento de auditoría de errores.                                                                                                                   |



 

Se puede realizar un seguimiento de las actividades seleccionadas de los usuarios mediante la auditoría de eventos de seguridad y, a continuación, la colocación de entradas en el registro de seguridad de un equipo.

 

 



