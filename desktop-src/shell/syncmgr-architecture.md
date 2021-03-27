---
description: El administrador de sincronización incluye componentes de la interfaz de usuario, como los cuadros de diálogo con pestañas en el servicio SyncMgr, cuadros de diálogo de error y cuadros de diálogo de progreso.
title: Arquitectura del administrador de sincronización
ms.topic: article
ms.date: 05/31/2018
ms.assetid: db338835-ca8d-4e9f-973a-8eb081feda2b
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f178b407c1f7d568c9de2ce7c81d937e7d1cdef4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819035"
---
# <a name="synchronization-manager-architecture"></a>Arquitectura del administrador de sincronización

El administrador de sincronización incluye componentes de la interfaz de usuario, como los cuadros de diálogo con pestañas en el servicio SyncMgr, cuadros de diálogo de error y cuadros de diálogo de progreso. Con los componentes de la interfaz de usuario, el usuario final puede programar aplicaciones para la sincronización y configurar la sincronización automática para que se produzca junto con los eventos del sistema especificados. Por ejemplo, el SyncMgr se puede invocar cuando el usuario inicia sesión o se apaga el sistema. El usuario también puede invocar una sincronización manual.

El usuario selecciona una aplicación y especifica los elementos de la aplicación que se van a sincronizar y establece un evento de desencadenador. Por ejemplo, en una aplicación de correo electrónico, la bandeja de entrada, la bandeja de salida o cualquier otra carpeta que contenga mensajes puede ser un elemento independiente para la aplicación.

SyncMgr también incluye una interfaz de programación para que las aplicaciones puedan registrarse para usar las características de sincronización, pueden procesar errores y recibir información y notificaciones de progreso durante el proceso de sincronización.

 

 



