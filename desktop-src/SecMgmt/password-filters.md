---
description: Filtros de contraseña
ms.assetid: 777edb4d-1fb4-4269-8382-8fe73c0c3b23
title: Filtros de contraseña
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f76aad9bb2bb722fe7f84b13dc6b5a6bdb7eb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278984"
---
# <a name="password-filters"></a><span data-ttu-id="ab147-103">Filtros de contraseña</span><span class="sxs-lookup"><span data-stu-id="ab147-103">Password Filters</span></span>

<span data-ttu-id="ab147-104">Los filtros de contraseñas proporcionan una manera de implementar la Directiva de contraseñas y la notificación de cambios.</span><span class="sxs-lookup"><span data-stu-id="ab147-104">Password filters provide a way for you to implement password policy and change notification.</span></span>

<span data-ttu-id="ab147-105">Cuando se realiza una solicitud de cambio de contraseña, la [*autoridad de seguridad local*](/windows/desktop/SecGloss/l-gly) (LSA) llama a los filtros de contraseña registrados en el sistema.</span><span class="sxs-lookup"><span data-stu-id="ab147-105">When a password change request is made, the [*Local Security Authority*](/windows/desktop/SecGloss/l-gly) (LSA) calls the password filters registered on the system.</span></span> <span data-ttu-id="ab147-106">Cada filtro de contraseña se llama dos veces: primero para validar la nueva contraseña y después, después de que todos los filtros hayan validado la nueva contraseña, para notificar a los filtros que se ha realizado el cambio.</span><span class="sxs-lookup"><span data-stu-id="ab147-106">Each password filter is called twice: first to validate the new password and then, after all filters have validated the new password, to notify the filters that the change has been made.</span></span> <span data-ttu-id="ab147-107">En la siguiente ilustración se muestra este proceso.</span><span class="sxs-lookup"><span data-stu-id="ab147-107">The following illustration shows this process.</span></span>

![solicitud de cambio de contraseña](images/pswdfilte.png)

<span data-ttu-id="ab147-109">La notificación de cambio de contraseña se usa para sincronizar los cambios de contraseña en las bases de datos de cuentas externas.</span><span class="sxs-lookup"><span data-stu-id="ab147-109">Password change notification is used to synchronize password changes to foreign account databases.</span></span>

<span data-ttu-id="ab147-110">Los filtros de contraseñas se utilizan para exigir la Directiva de contraseñas.</span><span class="sxs-lookup"><span data-stu-id="ab147-110">Password filters are used to enforce password policy.</span></span> <span data-ttu-id="ab147-111">Los filtros validan nuevas contraseñas e indican si la nueva contraseña se ajusta a la Directiva de contraseñas implementadas.</span><span class="sxs-lookup"><span data-stu-id="ab147-111">Filters validate new passwords and indicate whether the new password conforms to the implemented password policy.</span></span>

<span data-ttu-id="ab147-112">Para obtener información general sobre el uso de filtros de contraseñas, consulte [uso de filtros de contraseñas](using-password-filters.md).</span><span class="sxs-lookup"><span data-stu-id="ab147-112">For an overview of using password filters, see [Using Password Filters](using-password-filters.md).</span></span>

<span data-ttu-id="ab147-113">Para obtener una lista de las funciones de filtro de contraseñas, consulte [funciones de filtro de contraseñas](management-functions.md).</span><span class="sxs-lookup"><span data-stu-id="ab147-113">For a list of password filter functions, see [Password Filter Functions](management-functions.md).</span></span>

<span data-ttu-id="ab147-114">En los temas siguientes se proporciona más información acerca de los filtros de contraseñas:</span><span class="sxs-lookup"><span data-stu-id="ab147-114">The following topics provide more information about password filters:</span></span>

-   [<span data-ttu-id="ab147-115">Consideraciones sobre la programación de filtros de contraseña</span><span class="sxs-lookup"><span data-stu-id="ab147-115">Password Filter Programming Considerations</span></span>](password-filter-programming-considerations.md)
-   [<span data-ttu-id="ab147-116">Aplicación segura de contraseñas y Passfilt.dll</span><span class="sxs-lookup"><span data-stu-id="ab147-116">Strong Password Enforcement and Passfilt.dll</span></span>](strong-password-enforcement-and-passfilt-dll.md)

 

 
