---
description: Las clases de dispositivos simplifican el desarrollo al permitir que los programadores traten los dispositivos que tienen propiedades similares de manera similar.
ms.assetid: 061f3037-1c71-4da1-88d7-29906c136d7b
title: Dispositivo (clase) (TAPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 560f95b40ffa34f5e02ee7857928b75425fc7ed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001933"
---
# <a name="device-class"></a>Clase de dispositivo

Las clases de dispositivos simplifican el desarrollo al permitir que los programadores traten los dispositivos que tienen propiedades similares de manera similar. Por ejemplo, un teléfono digital de una oficina normalmente tiene más capacidades que un auricular estándar en casa, pero ambos responden de forma muy similar a un conjunto básico de funciones y ambos pertenecen a una clase de dispositivo de teléfono. Las clases de dispositivos ayudan a que TAPI sea extensible al proporcionar un marco desde el que clasificar y admitir nuevos equipos.

Vea [clases de dispositivos TAPI](./tapi-device-classes.md) para las clases que TAPI ha predefinido. Un proveedor de servicios puede implementar y definir clases de dispositivo adicionales para el equipo que admite. Una aplicación nunca necesita saber qué proveedor de servicios controla qué dispositivo, pero puede requerir información sobre el control de las nuevas clases de dispositivos.

Un proveedor de servicios implementa una clase de dispositivo mediante la asignación de solicitudes a comandos de dispositivo reales. Por ejemplo, cuando el proveedor de servicios para un módem compatible con Hayes recibe un comando que se pasa a través de TAPISVR para realizar una llamada, envía los comandos clásicos AT al módem.

La interfaz del proveedor de servicios se puede asignar a una amplia gama de entornos, incluidos los que tradicionalmente no se han considerado como pertenecientes a la telefonía. Un ejemplo es la conferencia multimedia a través de una red basada en IP, como Internet.

Los desarrolladores de aplicaciones deben tener en cuenta la existencia de otras aplicaciones que pueden compartir servicios de telefonía.

 

 
