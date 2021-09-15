---
description: El Administrador de sincronización incluye componentes de la interfaz de usuario, como los cuadros de diálogo con pestañas en el servicio SyncMgr, los diálogos de error y los diálogos de progreso.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571485"
---
# <a name="synchronization-manager-architecture"></a>Arquitectura del administrador de sincronización

El Administrador de sincronización incluye componentes de la interfaz de usuario, como los cuadros de diálogo con pestañas en el servicio SyncMgr, los diálogos de error y los diálogos de progreso. Con los componentes de la interfaz de usuario, el usuario final puede programar aplicaciones para la sincronización y configurar la sincronización automática para que se produzca junto con los eventos del sistema especificados. Por ejemplo, SyncMgr se puede invocar al iniciar sesión del usuario o apagar el sistema. El usuario también puede invocar una sincronización manual.

El usuario selecciona una aplicación y especifica los elementos dentro de la aplicación que se sincronizarán y establece un evento desencadenador. Por ejemplo, dentro de una aplicación de correo electrónico, la Bandeja de entrada, la Bandeja de salida o alguna otra carpeta que contenga mensajes puede ser un elemento independiente para la aplicación.

SyncMgr también incluye una interfaz de programación para que las aplicaciones puedan registrarse para usar características de sincronización, puedan procesar errores y puedan recibir información de progreso y notificaciones durante el proceso de sincronización.

 

 



