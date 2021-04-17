---
description: Es posible desarrollar una aplicación que realice operaciones que requieran privilegios de administrador y que se ejecuten como usuario estándar.
ms.assetid: 78099b59-b09b-43c0-91f5-adb5c9e0e191
title: Desarrollo de aplicaciones que requieren privilegios de administrador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d22687dad0a8914c5dcaebe8ea85a525529a34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652897"
---
# <a name="developing-applications-that-require-administrator-privilege"></a><span data-ttu-id="18943-103">Desarrollo de aplicaciones que requieren privilegios de administrador</span><span class="sxs-lookup"><span data-stu-id="18943-103">Developing Applications that Require Administrator Privilege</span></span>

<span data-ttu-id="18943-104">Es posible desarrollar una aplicación que realice operaciones que requieran privilegios de administrador y que se ejecuten como usuario estándar.</span><span class="sxs-lookup"><span data-stu-id="18943-104">It is possible to develop an application that performs operations that require administrator privilege yet runs as a standard user.</span></span>

<span data-ttu-id="18943-105">Hay varios modelos para lograr esto.</span><span class="sxs-lookup"><span data-stu-id="18943-105">There are several models for accomplishing this.</span></span>



| <span data-ttu-id="18943-106">Tema</span><span class="sxs-lookup"><span data-stu-id="18943-106">Topic</span></span>                                                                | <span data-ttu-id="18943-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="18943-107">Description</span></span>                                                                                                                                                                                          |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="18943-108">Modelo de tareas elevado</span><span class="sxs-lookup"><span data-stu-id="18943-108">Elevated Task Model</span></span>](elevated-task-model.md)                       | <span data-ttu-id="18943-109">Una aplicación que se ejecuta como usuario estándar realiza operaciones que requieren privilegios de administrador iniciando una tarea programada.</span><span class="sxs-lookup"><span data-stu-id="18943-109">An application running as a standard user performs operations that require administrator privilege by starting a scheduled task.</span></span>                                                                     |
| [<span data-ttu-id="18943-110">Modelo de servicio del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="18943-110">Operating System Service Model</span></span>](operating-system-service-model.md) | <span data-ttu-id="18943-111">Una aplicación que se ejecuta como un usuario estándar se comunica con un servicio que se ejecuta como **sistema** mediante la [llamada a procedimiento remoto](/windows/desktop/Rpc/rpc-start-page) (RPC).</span><span class="sxs-lookup"><span data-stu-id="18943-111">An application running as a standard user communicates with a service running as **SYSTEM** by using [Remote Procedure Call](/windows/desktop/Rpc/rpc-start-page) (RPC).</span></span>                                              |
| [<span data-ttu-id="18943-112">Modelo de agente de administrador</span><span class="sxs-lookup"><span data-stu-id="18943-112">Administrator Broker Model</span></span>](administrator-broker-model.md)         | <span data-ttu-id="18943-113">La aplicación se divide en dos programas.</span><span class="sxs-lookup"><span data-stu-id="18943-113">The application is divided into two programs.</span></span> <span data-ttu-id="18943-114">Uno de los programas se ejecuta como un usuario estándar y el otro con privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="18943-114">One of the programs runs as a standard user, and the other runs with administrator privilege.</span></span>                                                          |
| [<span data-ttu-id="18943-115">Modelo de objetos COM de administrador</span><span class="sxs-lookup"><span data-stu-id="18943-115">Administrator COM Object Model</span></span>](administrator-com-object-model.md) | <span data-ttu-id="18943-116">Una aplicación que se ejecuta como un usuario estándar realiza operaciones que requieren privilegios de administrador mediante la creación de un objeto de [modelo de objetos de componente](/windows/desktop/com/component-object-model--com--portal) elevado.</span><span class="sxs-lookup"><span data-stu-id="18943-116">An application running as a standard user performs operations that require administrator privilege by creating an elevated [Component Object Model](/windows/desktop/com/component-object-model--com--portal) object.</span></span> |



 

 

 
