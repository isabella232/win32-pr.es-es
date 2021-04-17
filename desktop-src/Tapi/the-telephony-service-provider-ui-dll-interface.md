---
description: En telefonía de Microsoft, los proveedores de servicios de telefonía se ejecutan en un proceso independiente de las aplicaciones de telefonía.
ms.assetid: ccc40d3c-6764-469a-baac-fa625d664ea7
title: La interfaz DLL de la interfaz de usuario del proveedor de servicios de telefonía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdab33dd9c9630aed7d7aed168982cfac2daee2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677790"
---
# <a name="the-telephony-service-provider-ui-dll-interface"></a>La interfaz DLL de la interfaz de usuario del proveedor de servicios de telefonía

En telefonía de Microsoft, los proveedores de servicios de telefonía se ejecutan en un proceso independiente de las aplicaciones de telefonía. Los proveedores de servicios se comunican con TAPISRV a través de la interfaz del proveedor de servicios de telefonía (TSPI) y se ejecutan en su proceso. interfaz de aplicaciones a TAPI, que se cargan en el contexto de la aplicación.

Los componentes de TAPI usan varios mecanismos de comunicación entre procesos para transmitir solicitudes de función y mensajes entre aplicaciones y proveedores de servicios. Las aplicaciones y los proveedores de servicios se pueden estar ejecutando no solo en procesos independientes, sino también en sistemas completamente independientes. Por lo tanto, los proveedores de servicios no pueden mostrar cuadros de diálogo en el proceso ni siquiera en el equipo en el que se ejecutan; La interfaz de usuario debe invocarse desde dentro del contexto de la aplicación, en el equipo en el que se ejecuta la aplicación.

En esta sección se define el mecanismo por el que las funciones de la interfaz de usuario del proveedor de servicios se cargan y se invocan en el contexto de la aplicación. También se define un mecanismo mediante el cual los proveedores de servicios pueden abrir cuadros de diálogo espontáneamente en el contexto de la aplicación cuando no serían esperados por la aplicación. Un ejemplo de este último caso sería el cuadro de diálogo **Talk/colgar** que muestra un proveedor de servicios de módem de datos cuando el módem se usa como marcador para llamadas de voz interactivas, y se debe indicar al usuario que recoja el teléfono e informará al proveedor de servicios de Cuándo debe colocar el módem.

 

 



