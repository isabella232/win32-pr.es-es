---
description: Una aplicación que se ejecuta como un usuario estándar realiza operaciones que requieren privilegios de administrador mediante la creación de un objeto de modelo de objetos de componente elevado.
ms.assetid: 246fdf74-cc5b-47b1-b3a8-20441544e7be
title: Modelo de objetos COM de administrador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6c7d73cf31ce86c4788675374f34d04f6acf106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911842"
---
# <a name="administrator-com-object-model"></a><span data-ttu-id="e7eda-103">Modelo de objetos COM de administrador</span><span class="sxs-lookup"><span data-stu-id="e7eda-103">Administrator COM Object Model</span></span>

<span data-ttu-id="e7eda-104">En el modelo de objetos COM de administrador, una aplicación que se ejecuta como un usuario estándar realiza operaciones que requieren privilegios de administrador mediante la creación de un objeto de [modelo de objetos de componente](/windows/desktop/com/component-object-model--com--portal) elevado.</span><span class="sxs-lookup"><span data-stu-id="e7eda-104">In the administrator COM object model, an application running as a standard user performs operations that require administrator privilege by creating an elevated [Component Object Model](/windows/desktop/com/component-object-model--com--portal) object.</span></span> <span data-ttu-id="e7eda-105">Para obtener información sobre cómo crear un objeto COM con privilegios elevados, vea [el moniker de elevación com](../com/the-com-elevation-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="e7eda-105">For information about creating an elevated COM object, see [The COM Elevation Moniker](../com/the-com-elevation-moniker.md).</span></span>

<span data-ttu-id="e7eda-106">Un inconveniente de usar el modelo de objetos COM de administrador es que se solicita al usuario cada vez que se realiza una operación con privilegios.</span><span class="sxs-lookup"><span data-stu-id="e7eda-106">One drawback to using the administrator COM object model is that the user is prompted each time a privileged operation is performed.</span></span>

<span data-ttu-id="e7eda-107">Cualquier interfaz de usuario que pueda controlar el objeto COM debe ser presentada por el propio objeto COM.</span><span class="sxs-lookup"><span data-stu-id="e7eda-107">Any user interface that can control the COM object must be presented by the COM object itself.</span></span> <span data-ttu-id="e7eda-108">De lo contrario, un proceso sin privilegios podría hacer que el objeto COM elevado realice operaciones con privilegios sin que se le solicite al usuario.</span><span class="sxs-lookup"><span data-stu-id="e7eda-108">Otherwise, an unprivileged process could cause the elevated COM object to perform privileged operations without the user being prompted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7eda-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e7eda-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7eda-110">Desarrollo de aplicaciones que requieren privilegios de administrador</span><span class="sxs-lookup"><span data-stu-id="e7eda-110">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[<span data-ttu-id="e7eda-111">Modelo de agente de administrador</span><span class="sxs-lookup"><span data-stu-id="e7eda-111">Administrator Broker Model</span></span>](administrator-broker-model.md)
</dt> <dt>

[<span data-ttu-id="e7eda-112">Modelo de tareas elevado</span><span class="sxs-lookup"><span data-stu-id="e7eda-112">Elevated Task Model</span></span>](elevated-task-model.md)
</dt> <dt>

[<span data-ttu-id="e7eda-113">Modelo de servicio del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="e7eda-113">Operating System Service Model</span></span>](operating-system-service-model.md)
</dt> </dl>

 

 
