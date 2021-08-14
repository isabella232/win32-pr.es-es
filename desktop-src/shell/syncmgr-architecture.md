---
description: El Administrador de sincronización incluye componentes de la interfaz de usuario, como los cuadros de diálogo con pestañas en el servicio SyncMgr, los diálogos de error y los diálogos de progreso.
title: Arquitectura de Synchronization Manager
ms.topic: article
ms.date: 05/31/2018
ms.assetid: db338835-ca8d-4e9f-973a-8eb081feda2b
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 584329a06ee9df80558d9961b734b62a57d5ebccd83f200690812fa99132b06d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451871"
---
# <a name="synchronization-manager-architecture"></a>Arquitectura de Synchronization Manager

El Administrador de sincronización incluye componentes de la interfaz de usuario, como los cuadros de diálogo con pestañas en el servicio SyncMgr, los diálogos de error y los diálogos de progreso. Con los componentes de la interfaz de usuario, el usuario final puede programar aplicaciones para la sincronización y configurar la sincronización automática para que se produzca junto con los eventos del sistema especificados. Por ejemplo, SyncMgr se puede invocar durante el inicio de sesión del usuario o el cierre del sistema. El usuario también puede invocar una sincronización manual.

El usuario selecciona una aplicación y especifica los elementos de la aplicación que se sincronizarán y establece un evento desencadenador. Por ejemplo, dentro de una aplicación de correo electrónico, la Bandeja de entrada, la Bandeja de salida o alguna otra carpeta que contenga mensajes puede ser un elemento independiente para la aplicación.

SyncMgr también incluye una interfaz de programación para que las aplicaciones se puedan registrar para usar características de sincronización, puedan procesar errores y puedan recibir información de progreso y notificaciones durante el proceso de sincronización.

 

 



