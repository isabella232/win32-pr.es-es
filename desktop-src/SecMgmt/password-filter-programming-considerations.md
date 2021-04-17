---
description: Explica las consideraciones para la implementación de funciones de exportación de filtros de contraseñas.
ms.assetid: ec7c1e7e-844a-43d4-b756-02bc1062d7b8
title: Consideraciones sobre la programación de filtros de contraseña
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad13a52f66c29142248ca07179d8692887b1acb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666399"
---
# <a name="password-filter-programming-considerations"></a><span data-ttu-id="57a44-103">Consideraciones sobre la programación de filtros de contraseña</span><span class="sxs-lookup"><span data-stu-id="57a44-103">Password Filter Programming Considerations</span></span>

<span data-ttu-id="57a44-104">Al implementar funciones de exportación de [*filtros de contraseña*](/windows/desktop/SecGloss/p-gly) , tenga en cuenta las consideraciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="57a44-104">When implementing [*password filter*](/windows/desktop/SecGloss/p-gly) export functions, keep the following considerations in mind:</span></span>

-   <span data-ttu-id="57a44-105">Tenga mucho cuidado al trabajar con contraseñas de [*texto sin formato*](/windows/desktop/SecGloss/p-gly) .</span><span class="sxs-lookup"><span data-stu-id="57a44-105">Take great care when working with [*plaintext*](/windows/desktop/SecGloss/p-gly) passwords.</span></span> <span data-ttu-id="57a44-106">El envío de contraseñas sin formato a través de redes podría poner en peligro la seguridad.</span><span class="sxs-lookup"><span data-stu-id="57a44-106">Sending plaintext passwords over networks could compromise security.</span></span> <span data-ttu-id="57a44-107">Los "rastreadores" de red pueden ver fácilmente el tráfico de contraseñas sin formato.</span><span class="sxs-lookup"><span data-stu-id="57a44-107">Network "sniffers" can easily watch for plaintext password traffic.</span></span>
-   <span data-ttu-id="57a44-108">Borre toda la memoria usada para almacenar las contraseñas mediante una llamada a la función [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) antes de liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="57a44-108">Erase all memory used to store passwords by calling the [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function before freeing memory.</span></span>
-   <span data-ttu-id="57a44-109">Todos los búferes pasados a las rutinas de filtro y notificación de contraseña deben tratarse como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="57a44-109">All buffers passed into password notification and filter routines should be treated as read-only.</span></span> <span data-ttu-id="57a44-110">La escritura de datos en estos búferes puede provocar un comportamiento inestable.</span><span class="sxs-lookup"><span data-stu-id="57a44-110">Writing data to these buffers may cause unstable behavior.</span></span>
-   <span data-ttu-id="57a44-111">Todas las rutinas de filtrado y notificación de contraseña deben ser seguras para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="57a44-111">All password notification and filter routines should be thread-safe.</span></span> <span data-ttu-id="57a44-112">Use secciones críticas u otras técnicas de programación sincrónicas para proteger los datos cuando corresponda.</span><span class="sxs-lookup"><span data-stu-id="57a44-112">Use critical sections or other synchronous programming techniques to protect data where appropriate.</span></span>
-   <span data-ttu-id="57a44-113">La notificación y el filtrado de contraseñas tienen lugar solo en el equipo que aloja la cuenta.</span><span class="sxs-lookup"><span data-stu-id="57a44-113">Password notification and filtering take place only on the computer that houses the account.</span></span>
-   <span data-ttu-id="57a44-114">Todos los controladores de dominio son grabables, por lo que los paquetes de filtros de contraseña deben estar presentes en todos los controladores de dominio.</span><span class="sxs-lookup"><span data-stu-id="57a44-114">All domain controllers are writeable, therefore password filter packages must be present on all domain controllers.</span></span>

    <span data-ttu-id="57a44-115">**Dominios de Windows NT 4,0:** La notificación en las cuentas de dominio solo tiene lugar en el controlador de dominio principal.</span><span class="sxs-lookup"><span data-stu-id="57a44-115">**Windows NT 4.0 domains:** Notification on domain accounts takes place only on the primary domain controller.</span></span> <span data-ttu-id="57a44-116">Además del controlador de dominio principal, los paquetes de filtro de contraseña deben instalarse en todos los controladores de dominio de copia de seguridad para permitir que las notificaciones continúen en caso de que se realicen cambios en el rol de servidor.</span><span class="sxs-lookup"><span data-stu-id="57a44-116">In addition to the primary domain controller, the password filter packages should be installed on all backup domain controllers to allow notifications to continue in the event of server role changes.</span></span>

-   <span data-ttu-id="57a44-117">Todos los archivos dll de filtro de contraseña se ejecutan en el [*contexto de seguridad*](/windows/desktop/SecGloss/s-gly) de la cuenta de sistema local.</span><span class="sxs-lookup"><span data-stu-id="57a44-117">All password filter DLLs run in the [*security context*](/windows/desktop/SecGloss/s-gly) of the local system account.</span></span>



| <span data-ttu-id="57a44-118">Para información acerca de</span><span class="sxs-lookup"><span data-stu-id="57a44-118">For information about</span></span>                                                                                                                     | <span data-ttu-id="57a44-119">Vea</span><span class="sxs-lookup"><span data-stu-id="57a44-119">See</span></span>                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57a44-120">Cómo instalar y registrar su propia DLL de [*filtro de contraseñas*](/windows/desktop/SecGloss/p-gly) .</span><span class="sxs-lookup"><span data-stu-id="57a44-120">How to install and register your own [*password filter*](/windows/desktop/SecGloss/p-gly) DLL.</span></span> | [<span data-ttu-id="57a44-121">Instalación y registro de un archivo DLL de filtro de contraseñas</span><span class="sxs-lookup"><span data-stu-id="57a44-121">Installing and Registering a Password Filter DLL</span></span>](installing-and-registering-a-password-filter-dll.md) |
| <span data-ttu-id="57a44-122">El archivo DLL de filtro de contraseña proporcionado por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="57a44-122">The password filter DLL provided by Microsoft.</span></span>                                                                                            | [<span data-ttu-id="57a44-123">Aplicación segura de contraseñas y Passfilt.dll</span><span class="sxs-lookup"><span data-stu-id="57a44-123">Strong Password Enforcement and Passfilt.dll</span></span>](strong-password-enforcement-and-passfilt-dll.md)         |
| <span data-ttu-id="57a44-124">Exportar funciones implementadas por un archivo DLL de filtro de contraseñas.</span><span class="sxs-lookup"><span data-stu-id="57a44-124">Export functions implemented by a password filter DLL.</span></span>                                                                                    | [<span data-ttu-id="57a44-125">Funciones de filtro de contraseñas</span><span class="sxs-lookup"><span data-stu-id="57a44-125">Password Filter Functions</span></span>](management-functions.md)                          |



 

 

 
