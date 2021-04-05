---
description: Las siguientes funciones las implementa una DLL de proveedor de red para comunicarse con el enrutador de proveedor múltiple (MPR).
ms.assetid: ebdaec3d-6335-4bdf-b150-91e538068f2b
title: Funciones implementadas por los proveedores de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8122d8e06e92f66958f597c8fbe26f8e1c7abdd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002762"
---
# <a name="functions-implemented-by-network-providers"></a><span data-ttu-id="27f58-103">Funciones implementadas por los proveedores de red</span><span class="sxs-lookup"><span data-stu-id="27f58-103">Functions Implemented by Network Providers</span></span>

<span data-ttu-id="27f58-104">Las siguientes funciones las implementa una DLL de proveedor de red para comunicarse con el [*enrutador de proveedor múltiple*](/windows/desktop/SecGloss/m-gly) (MPR).</span><span class="sxs-lookup"><span data-stu-id="27f58-104">The following functions are implemented by a network provider DLL to communicate with the [*Multiple Provider Router*](/windows/desktop/SecGloss/m-gly) (MPR).</span></span> <span data-ttu-id="27f58-105">Tenga en cuenta que solo las [funciones de funcionalidad](capabilities-functions.md) deben ser implementadas por un proveedor de red.</span><span class="sxs-lookup"><span data-stu-id="27f58-105">Note that only the [Capabilities Functions](capabilities-functions.md) must be implemented by a network provider.</span></span> <span data-ttu-id="27f58-106">La implementación de los demás tipos de funciones es opcional y depende de los requisitos del proveedor de red.</span><span class="sxs-lookup"><span data-stu-id="27f58-106">Implementation of the other types of functions is optional and depends on the requirements of the network provider.</span></span>



| <span data-ttu-id="27f58-107">Conjunto de funciones</span><span class="sxs-lookup"><span data-stu-id="27f58-107">Function set</span></span>                                                                                    | <span data-ttu-id="27f58-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="27f58-108">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="27f58-109">Funciones de funcionalidad</span><span class="sxs-lookup"><span data-stu-id="27f58-109">Capabilities Functions</span></span>](capabilities-functions.md)<br/>                                 | <span data-ttu-id="27f58-110">Permite al llamador determinar las capacidades del proveedor de red.</span><span class="sxs-lookup"><span data-stu-id="27f58-110">Allows the caller to determine the capabilities of the network provider.</span></span><br/>                                                                |
| [<span data-ttu-id="27f58-111">Funciones de nombre de usuario</span><span class="sxs-lookup"><span data-stu-id="27f58-111">User Name Functions</span></span>](user-name-functions.md)<br/>                                       | <span data-ttu-id="27f58-112">Solicita al proveedor de red el nombre de usuario asociado a una conexión.</span><span class="sxs-lookup"><span data-stu-id="27f58-112">Prompts the network provider for the user name associated with a connection.</span></span><br/>                                                            |
| [<span data-ttu-id="27f58-113">Funciones de redireccionamiento de dispositivos</span><span class="sxs-lookup"><span data-stu-id="27f58-113">Device-Redirecting Functions</span></span>](device-redirecting-functions.md)<br/>                     | <span data-ttu-id="27f58-114">Permite a un proveedor de red redirigir dispositivos, Letras de unidad y puertos LPT que son estándar en el sistema operativo Microsoft MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="27f58-114">Allows a network provider to redirect devices, drive letters, and LPT ports that are standard on the Microsoft MS-DOS operating system.</span></span><br/> |
| [<span data-ttu-id="27f58-115">Funciones del cuadro de diálogo específicas del proveedor</span><span class="sxs-lookup"><span data-stu-id="27f58-115">Provider-Specific Dialog Box Functions</span></span>](provider-specific-dialog-box-functions.md)<br/> | <span data-ttu-id="27f58-116">Permite a un proveedor de red mostrar o actuar en la información específica de la red.</span><span class="sxs-lookup"><span data-stu-id="27f58-116">Allows a network provider to display or act on network-specific information.</span></span><br/>                                                            |
| [<span data-ttu-id="27f58-117">Funciones administrativas</span><span class="sxs-lookup"><span data-stu-id="27f58-117">Administrative Functions</span></span>](administrative-functions.md)<br/>                             | <span data-ttu-id="27f58-118">Permite que un proveedor de red muestre o actúe en directorios de red especiales.</span><span class="sxs-lookup"><span data-stu-id="27f58-118">Allows a network provider to display or act on special network directories.</span></span><br/>                                                             |
| [<span data-ttu-id="27f58-119">Funciones de enumeración</span><span class="sxs-lookup"><span data-stu-id="27f58-119">Enumeration Functions</span></span>](enumeration-functions.md)<br/>                                   | <span data-ttu-id="27f58-120">Permite al usuario examinar los recursos de red.</span><span class="sxs-lookup"><span data-stu-id="27f58-120">Allows the user to browse network resources.</span></span><br/>                                                                                            |



 

<span data-ttu-id="27f58-121">Para obtener más información acerca de cómo crear y registrar un proveedor de red, consulte [implementación de un proveedor de red](implementing-a-network-provider.md) y [registro de proveedores de redes y administradores de credenciales](registering-network-providers-and-credential-managers.md).</span><span class="sxs-lookup"><span data-stu-id="27f58-121">For more information about how to create and register a network provider, see [Implementing a Network Provider](implementing-a-network-provider.md) and [Registering Network Providers and Credential Managers](registering-network-providers-and-credential-managers.md).</span></span>

 

