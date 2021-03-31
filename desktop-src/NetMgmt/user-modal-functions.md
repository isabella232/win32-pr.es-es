---
title: Funciones modales de usuario
description: Las funciones modales del usuario de administración de redes obtienen y establecen parámetros en todo el sistema relacionados con el comportamiento del sistema de seguridad.
ms.assetid: e655b9f6-2808-4bd4-998c-c8a2e980920b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c65595f78a412196b9fd54030ec1ac1f1fb8ae59
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995562"
---
# <a name="user-modal-functions"></a><span data-ttu-id="855dd-103">Funciones modales de usuario</span><span class="sxs-lookup"><span data-stu-id="855dd-103">User Modal Functions</span></span>

<span data-ttu-id="855dd-104">Las funciones modales del usuario de administración de redes obtienen y establecen parámetros en todo el sistema relacionados con el comportamiento del sistema de seguridad.</span><span class="sxs-lookup"><span data-stu-id="855dd-104">The network management user modal functions get and set system-wide parameters related to security system behavior.</span></span>

<span data-ttu-id="855dd-105">A continuación se enumeran las funciones modales de usuario.</span><span class="sxs-lookup"><span data-stu-id="855dd-105">The user modal functions are listed following.</span></span>



| <span data-ttu-id="855dd-106">Función</span><span class="sxs-lookup"><span data-stu-id="855dd-106">Function</span></span>                                     | <span data-ttu-id="855dd-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="855dd-107">Description</span></span>                                                                                                                                                                                             |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="855dd-108">**NetUserModalsGet**</span><span class="sxs-lookup"><span data-stu-id="855dd-108">**NetUserModalsGet**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget) | <span data-ttu-id="855dd-109">Devuelve información global de todos los usuarios y grupos globales en la base de datos de seguridad, que es la base de datos del administrador de cuentas de seguridad (SAM) o, en el caso de los controladores de dominio, el Active Directory.</span><span class="sxs-lookup"><span data-stu-id="855dd-109">Returns global information for all users and global groups in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.</span></span> |
| [<span data-ttu-id="855dd-110">**NetUserModalsSet**</span><span class="sxs-lookup"><span data-stu-id="855dd-110">**NetUserModalsSet**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) | <span data-ttu-id="855dd-111">Establece la información global de todos los usuarios y grupos globales en la base de datos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="855dd-111">Sets global information for all users and global groups in the security database.</span></span>                                                                                                                       |



 

<span data-ttu-id="855dd-112">Las funciones **NetUserModalsGet** y **NetUserModalsSet** examinan y modifican la configuración modal, que son parámetros globales que afectan a todas las cuentas de la base de datos de seguridad (por ejemplo, la longitud mínima de contraseña permitida).</span><span class="sxs-lookup"><span data-stu-id="855dd-112">The **NetUserModalsGet** and **NetUserModalsSet** functions examine and modify the modal settings, which are global parameters that affect every account in the security database (for example, the minimum allowable password length).</span></span> <span data-ttu-id="855dd-113">Se puede modificar toda la configuración modal llamando a **NetUserModalsSet**.</span><span class="sxs-lookup"><span data-stu-id="855dd-113">All modal settings can be altered by calling **NetUserModalsSet**.</span></span> <span data-ttu-id="855dd-114">La mayoría de los modales también se pueden modificar mediante el comando **net accounts** .</span><span class="sxs-lookup"><span data-stu-id="855dd-114">Most of the modals can also be altered by using the **net accounts** command.</span></span> <span data-ttu-id="855dd-115">Las funciones modales del usuario de administración de redes no requieren que el servidor tenga seguridad de nivel de usuario.</span><span class="sxs-lookup"><span data-stu-id="855dd-115">The network management user modal functions do not require the server to have user-level security.</span></span>

<span data-ttu-id="855dd-116">La información modal del usuario está disponible en los siguientes niveles:</span><span class="sxs-lookup"><span data-stu-id="855dd-116">User modal information is available at the following levels:</span></span>

-   [<span data-ttu-id="855dd-117">**Información sobre los modos de usuario \_ \_ \_ 0**</span><span class="sxs-lookup"><span data-stu-id="855dd-117">**USER\_MODALS\_INFO\_0**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_0)
-   [<span data-ttu-id="855dd-118">**Información sobre los modos de usuario \_ \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="855dd-118">**USER\_MODALS\_INFO\_1**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1)
-   [<span data-ttu-id="855dd-119">**Información sobre los modos de usuario \_ \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="855dd-119">**USER\_MODALS\_INFO\_2**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_2)
-   [<span data-ttu-id="855dd-120">**Información sobre los modos de usuario \_ \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="855dd-120">**USER\_MODALS\_INFO\_3**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_3)

<span data-ttu-id="855dd-121">Los siguientes niveles de información solo son válidos para [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) y reemplazan la forma más antigua de pasar un *Parmnum* para establecer un campo específico:</span><span class="sxs-lookup"><span data-stu-id="855dd-121">The following information levels are valid only for [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) and replace the older way of passing in a *Parmnum* to set a specific field:</span></span>

-   [<span data-ttu-id="855dd-122">**Información sobre los modos de usuario \_ \_ \_ 1001**</span><span class="sxs-lookup"><span data-stu-id="855dd-122">**USER\_MODALS\_INFO\_1001**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1001)
-   [<span data-ttu-id="855dd-123">**Información sobre los modos de usuario \_ \_ \_ 1002**</span><span class="sxs-lookup"><span data-stu-id="855dd-123">**USER\_MODALS\_INFO\_1002**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1002)
-   [<span data-ttu-id="855dd-124">**Información sobre los modos de usuario \_ \_ \_ 1003**</span><span class="sxs-lookup"><span data-stu-id="855dd-124">**USER\_MODALS\_INFO\_1003**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1003)
-   [<span data-ttu-id="855dd-125">**Información sobre los modos de usuario \_ \_ \_ 1004**</span><span class="sxs-lookup"><span data-stu-id="855dd-125">**USER\_MODALS\_INFO\_1004**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1004)
-   [<span data-ttu-id="855dd-126">**Información sobre los modos de usuario \_ \_ \_ 1005**</span><span class="sxs-lookup"><span data-stu-id="855dd-126">**USER\_MODALS\_INFO\_1005**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1005)
-   [<span data-ttu-id="855dd-127">**Información sobre los modos de usuario \_ \_ \_ 1006**</span><span class="sxs-lookup"><span data-stu-id="855dd-127">**USER\_MODALS\_INFO\_1006**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1006)
-   [<span data-ttu-id="855dd-128">**Información sobre los modos de usuario \_ \_ \_ 1007**</span><span class="sxs-lookup"><span data-stu-id="855dd-128">**USER\_MODALS\_INFO\_1007**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1007)

<span data-ttu-id="855dd-129">Si programa para Active Directory, es posible que pueda llamar a determinados métodos de la interfaz de servicio Active Directory (ADSI) para lograr la misma funcionalidad que puede lograr llamando a las funciones modales del usuario de administración de redes.</span><span class="sxs-lookup"><span data-stu-id="855dd-129">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management user modal functions.</span></span> <span data-ttu-id="855dd-130">Para obtener más información, vea [**IADsDomain**](/windows/desktop/api/iads/nn-iads-iadsdomain).</span><span class="sxs-lookup"><span data-stu-id="855dd-130">For more information, see [**IADsDomain**](/windows/desktop/api/iads/nn-iads-iadsdomain).</span></span>

 

 