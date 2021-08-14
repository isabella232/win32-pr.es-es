---
description: En Telefonía de Microsoft, los proveedores de servicios de telefonía se ejecutan en un proceso independiente de las aplicaciones de telefonía.
ms.assetid: ccc40d3c-6764-469a-baac-fa625d664ea7
title: Interfaz DLL de la interfaz de usuario del proveedor de servicios de telefonía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6aea6dfd68773dcd96602803230bd160552eab1414135b75a3205a0fac88dd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119403945"
---
# <a name="the-telephony-service-provider-ui-dll-interface"></a>Interfaz DLL de la interfaz de usuario del proveedor de servicios de telefonía

En Telefonía de Microsoft, los proveedores de servicios de telefonía se ejecutan en un proceso independiente de las aplicaciones de telefonía. Los proveedores de servicios se comunican con TAPISRV a través de la interfaz del proveedor de servicios de telefonía (TSPI) y se ejecutan en su proceso. interfaz de aplicaciones para TAPI, que se cargan en el contexto de la aplicación.

Los componentes de TAPI usan diversos mecanismos de comunicación entre procesos para transmitir solicitudes de función y mensajes entre aplicaciones y proveedores de servicios. Las aplicaciones y los proveedores de servicios pueden estar ejecutándose no solo en procesos independientes, sino en sistemas completamente independientes. Por lo tanto, los proveedores de servicios no pueden mostrar cuadros de diálogo en el proceso o incluso en el equipo en el que se ejecutan. La interfaz de usuario se debe invocar desde dentro del contexto de la aplicación, en el equipo en el que se ejecuta la aplicación.

En esta sección se define el mecanismo por el que las funciones de interfaz de usuario del proveedor de servicios se cargan e invocan en el contexto de la aplicación. También se define un mecanismo por el que los proveedores de servicios pueden abrir de forma desabrida cuadros de diálogo en el contexto de la aplicación cuando la aplicación no los esperaría de otro modo. Un ejemplo de este último caso sería el cuadro de diálogo **Talk/Hangup** que muestra un proveedor de servicios de módem de datos cuando el módem se usa como marcador para llamadas de voz interactivas, y se debe indicar al usuario que recoge el teléfono e informa al proveedor de servicios cuándo debe colocar el módem en elhook.

 

 



