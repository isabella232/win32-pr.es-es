---
description: El sistema utiliza objetos y controladores para regular el acceso a los recursos del sistema por dos motivos principales.
ms.assetid: 122acb9e-2a1b-480b-9207-5cc6bbe6b6d4
title: Acerca de los identificadores y objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c7474c11298166cc8d63032c6e1d8f84e6db249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002067"
---
# <a name="about-handles-and-objects"></a><span data-ttu-id="6164c-103">Acerca de los identificadores y objetos</span><span class="sxs-lookup"><span data-stu-id="6164c-103">About Handles and Objects</span></span>

<span data-ttu-id="6164c-104">El sistema utiliza objetos y controladores para regular el acceso a los recursos del sistema por dos motivos principales.</span><span class="sxs-lookup"><span data-stu-id="6164c-104">The system uses objects and handles to regulate access to system resources for two main reasons.</span></span> <span data-ttu-id="6164c-105">En primer lugar, el uso de objetos garantiza que Microsoft puede actualizar la funcionalidad del sistema, siempre que se mantenga la interfaz de objeto original.</span><span class="sxs-lookup"><span data-stu-id="6164c-105">First, the use of objects ensures that Microsoft can update system functionality, as long as the original object interface is maintained.</span></span> <span data-ttu-id="6164c-106">Cuando se lancen versiones posteriores del sistema, puede usar el objeto actualizado con pocos o ningún trabajo adicional.</span><span class="sxs-lookup"><span data-stu-id="6164c-106">When subsequent versions of the system are released, you can use the updated object with little or no additional work.</span></span>

<span data-ttu-id="6164c-107">En segundo lugar, el uso de objetos le permite aprovechar la seguridad de Windows.</span><span class="sxs-lookup"><span data-stu-id="6164c-107">Secondly, the use of objects enables you to take advantage of Windows security.</span></span> <span data-ttu-id="6164c-108">Cada objeto tiene su propia lista de control de acceso (ACL) que especifica las acciones que un proceso puede realizar en el objeto.</span><span class="sxs-lookup"><span data-stu-id="6164c-108">Each object has its own access-control list (ACL) that specifies the actions a process can perform on the object.</span></span> <span data-ttu-id="6164c-109">El sistema examina la ACL de un objeto cada vez que una aplicación crea un identificador para el objeto.</span><span class="sxs-lookup"><span data-stu-id="6164c-109">The system examines an object's ACL each time an application creates a handle to the object.</span></span> <span data-ttu-id="6164c-110">Para obtener más información, consulta [Access Control](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="6164c-110">For more information, see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

-   [<span data-ttu-id="6164c-111">Administrador de objetos</span><span class="sxs-lookup"><span data-stu-id="6164c-111">Object Manager</span></span>](object-manager.md)
-   [<span data-ttu-id="6164c-112">Interfaz de objeto</span><span class="sxs-lookup"><span data-stu-id="6164c-112">Object Interface</span></span>](object-interface.md)
-   [<span data-ttu-id="6164c-113">Espacios de nombres de objetos</span><span class="sxs-lookup"><span data-stu-id="6164c-113">Object Namespaces</span></span>](/windows/desktop/Sync/object-namespaces)
-   [<span data-ttu-id="6164c-114">Solucionar limitaciones</span><span class="sxs-lookup"><span data-stu-id="6164c-114">Handle Limitations</span></span>](handle-limitations.md)
-   [<span data-ttu-id="6164c-115">Controlar la herencia</span><span class="sxs-lookup"><span data-stu-id="6164c-115">Handle Inheritance</span></span>](handle-inheritance.md)

 

 
