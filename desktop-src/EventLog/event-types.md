---
description: Hay cinco tipos de eventos que se pueden registrar. Todos ellos tienen datos comunes bien definidos y, opcionalmente, pueden incluir datos específicos del evento.
ms.assetid: 4ab4a284-a4cd-4cf7-a9d2-e4a75fce01b9
title: Tipos de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3832f90ccdb8dafc676c139f92665efde732533c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908862"
---
# <a name="event-types"></a>Tipos de eventos

Hay cinco tipos de eventos que se pueden registrar. Todos ellos tienen datos comunes bien definidos y, opcionalmente, pueden incluir datos específicos del evento.

La aplicación indica el tipo de evento cuando informa de un evento. Cada evento debe ser de un tipo único. En el Visor de eventos se muestra un icono diferente para cada tipo en la vista de lista del registro de eventos.

En la tabla siguiente se describen los cinco tipos de eventos que se usan en el registro de eventos.



| Tipo de evento        | Descripción                                                                                                                                                                                                                                                                                              |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Error**         | Evento que indica un problema importante, como la pérdida de datos o la pérdida de funcionalidad. Por ejemplo, si un servicio no se carga durante el inicio, se registra un evento de error.                                                                                                                           |
| **Warning (ADVERTENCIA)**       | Un evento que no es necesariamente significativo, pero puede indicar un posible problema futuro. Por ejemplo, si el espacio en disco es bajo, se registra un evento de advertencia. Si una aplicación puede recuperarse de un evento sin pérdida de funcionalidad o datos, generalmente puede clasificar el evento como un evento de advertencia.     |
| **Información**   | Evento que describe el funcionamiento correcto de una aplicación, un controlador o un servicio. Por ejemplo, cuando un controlador de red se carga correctamente, puede ser adecuado registrar un evento de información. Tenga en cuenta que, por lo general, no es apropiado que una aplicación de escritorio registre un evento cada vez que se inicie. |
| **Auditoría de aciertos** | Evento que registra un intento de acceso de seguridad auditado que se realiza correctamente. Por ejemplo, el intento de inicio de sesión correcto de un usuario en el sistema se registra como un evento de auditoría correcta.                                                                                                                        |
| **Auditoría de errores** | Evento que registra un intento de acceso de seguridad auditado que produce un error. Por ejemplo, si un usuario intenta obtener acceso a una unidad de red y se produce un error, el intento se registra como un evento de auditoría de errores.                                                                                                                   |



 

Se puede realizar un seguimiento de las actividades seleccionadas de los usuarios mediante la auditoría de eventos de seguridad y la colocación de entradas en el registro de seguridad de un equipo.

 

 



