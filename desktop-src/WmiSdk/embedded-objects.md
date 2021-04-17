---
description: Un objeto incrustado es un objeto de una clase que existe dentro de una declaración de clase o instancia de otra clase.
ms.assetid: 11a4556b-f682-4850-aedc-793602c5745b
ms.tgt_platform: multiple
title: Incrustar objetos en una clase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39b94296a6869dddca7fd3df08739615a4a0c501
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716641"
---
# <a name="embedding-objects-in-a-class"></a><span data-ttu-id="38849-103">Incrustar objetos en una clase</span><span class="sxs-lookup"><span data-stu-id="38849-103">Embedding Objects in a Class</span></span>

<span data-ttu-id="38849-104">Un objeto incrustado es un objeto de una clase que existe dentro de una declaración de clase o instancia de otra clase.</span><span class="sxs-lookup"><span data-stu-id="38849-104">An embedded object is an object of a class that exists within a class or instance declaration of another class.</span></span> <span data-ttu-id="38849-105">Por ejemplo, la [**clase \_ SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) contiene objetos incrustados de [**\_ confianza de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) .</span><span class="sxs-lookup"><span data-stu-id="38849-105">For example, the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class contains [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) embedded objects.</span></span> <span data-ttu-id="38849-106">Cada uno de los objetos de **\_ confianza de Win32** contiene un objeto [**\_ ACE de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .</span><span class="sxs-lookup"><span data-stu-id="38849-106">Each of the **Win32\_Trustee** objects contains a [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) object.</span></span> <span data-ttu-id="38849-107">WMI no limita la profundidad con la que una clase puede tener objetos incrustados.</span><span class="sxs-lookup"><span data-stu-id="38849-107">WMI does not limit the depth to which a class can have embedded objects.</span></span> <span data-ttu-id="38849-108">Sin embargo, el uso de otro diseño, como la creación de una clase de asociación, puede crear un esquema más fácil de administrar.</span><span class="sxs-lookup"><span data-stu-id="38849-108">However, using another design, such as creating an association class, may make a more manageable schema.</span></span>

<span data-ttu-id="38849-109">Para obtener más información acerca de los objetos incrustados, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="38849-109">For more information about embedded objects, see the following topics:</span></span>

-   [<span data-ttu-id="38849-110">Crear objetos incrustados</span><span class="sxs-lookup"><span data-stu-id="38849-110">Creating Embedded Objects</span></span>](creating-embedded-objects.md)
-   [<span data-ttu-id="38849-111">Consultar objetos incrustados</span><span class="sxs-lookup"><span data-stu-id="38849-111">Querying Embedded Objects</span></span>](querying-embedded-objects.md)

## <a name="related-topics"></a><span data-ttu-id="38849-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="38849-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38849-113">Diseñar clases de Managed Object Format (MOF)</span><span class="sxs-lookup"><span data-stu-id="38849-113">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
