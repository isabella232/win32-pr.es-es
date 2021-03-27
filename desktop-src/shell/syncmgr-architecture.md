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
# <a name="synchronization-manager-architecture"></a><span data-ttu-id="d8d1c-103">Arquitectura del administrador de sincronización</span><span class="sxs-lookup"><span data-stu-id="d8d1c-103">Synchronization Manager Architecture</span></span>

<span data-ttu-id="d8d1c-104">El administrador de sincronización incluye componentes de la interfaz de usuario, como los cuadros de diálogo con pestañas en el servicio SyncMgr, cuadros de diálogo de error y cuadros de diálogo de progreso.</span><span class="sxs-lookup"><span data-stu-id="d8d1c-104">The Synchronization Manager includes user interface components, such as the tabbed dialog boxes in the SyncMgr service, error dialogs, and progress dialogs.</span></span> <span data-ttu-id="d8d1c-105">Con los componentes de la interfaz de usuario, el usuario final puede programar aplicaciones para la sincronización y configurar la sincronización automática para que se produzca junto con los eventos del sistema especificados.</span><span class="sxs-lookup"><span data-stu-id="d8d1c-105">With the user interface components the end user can schedule applications for synchronization and set up automatic synchronization to occur in conjunction with specified system events.</span></span> <span data-ttu-id="d8d1c-106">Por ejemplo, el SyncMgr se puede invocar cuando el usuario inicia sesión o se apaga el sistema.</span><span class="sxs-lookup"><span data-stu-id="d8d1c-106">For example, the SyncMgr can be invoked at user logon or system shutdown.</span></span> <span data-ttu-id="d8d1c-107">El usuario también puede invocar una sincronización manual.</span><span class="sxs-lookup"><span data-stu-id="d8d1c-107">The user can also invoke a manual synchronization.</span></span>

<span data-ttu-id="d8d1c-108">El usuario selecciona una aplicación y especifica los elementos de la aplicación que se van a sincronizar y establece un evento de desencadenador.</span><span class="sxs-lookup"><span data-stu-id="d8d1c-108">The user selects an application and specifies the items within the application to be synchronized and sets a trigger event.</span></span> <span data-ttu-id="d8d1c-109">Por ejemplo, en una aplicación de correo electrónico, la bandeja de entrada, la bandeja de salida o cualquier otra carpeta que contenga mensajes puede ser un elemento independiente para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d8d1c-109">For example, within an email application, the Inbox, the Outbox, or some other folder containing messages can be a separate item for the application.</span></span>

<span data-ttu-id="d8d1c-110">SyncMgr también incluye una interfaz de programación para que las aplicaciones puedan registrarse para usar las características de sincronización, pueden procesar errores y recibir información y notificaciones de progreso durante el proceso de sincronización.</span><span class="sxs-lookup"><span data-stu-id="d8d1c-110">SyncMgr also includes a programming interface so that applications can register to use synchronization features, can process errors, and can receive progress information and notifications during the synchronization process.</span></span>

 

 



