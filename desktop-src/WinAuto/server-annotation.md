---
title: Anotación de servidor
description: En esta sección se proporciona información sobre el uso de la anotación de servidor.
ms.assetid: d8de90af-f5ed-42ef-bd74-e383360e8128
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe1b8fba9849b25a29c50ea1f55507e61eb69f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075332"
---
# <a name="server-annotation"></a><span data-ttu-id="5fdc7-103">Anotación de servidor</span><span class="sxs-lookup"><span data-stu-id="5fdc7-103">Server Annotation</span></span>

<span data-ttu-id="5fdc7-104">En esta sección se proporciona información sobre el uso de la anotación de servidor.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-104">This section provides information about using server annotation.</span></span>

## <a name="summary"></a><span data-ttu-id="5fdc7-105">Resumen</span><span class="sxs-lookup"><span data-stu-id="5fdc7-105">Summary</span></span>

<span data-ttu-id="5fdc7-106">Defina una clase que implemente [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver), cree una instancia de ella e indique al sistema que desea invalidar propiedades específicas en elementos de interfaz de usuario específicos.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-106">You define a class that implements [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver), create an instance of it, and tell the system that you want it to override specific properties on specific UI elements.</span></span> <span data-ttu-id="5fdc7-107">Cuando un cliente solicita una de las propiedades de uno de los elementos de la interfaz de usuario, se llama al objeto y se le da la oportunidad de proporcionar un valor.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-107">When a client requests one of the properties from one of the UI elements, your object is called and given an opportunity to provide a value.</span></span> <span data-ttu-id="5fdc7-108">Si el objeto devuelve un valor, dicho valor se devuelve al cliente.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-108">If your object returns a value, that value is passed back to the client.</span></span> <span data-ttu-id="5fdc7-109">Si el objeto no devuelve un valor, el valor predeterminado para ese elemento de la interfaz de usuario se devuelve al cliente.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-109">If your object does not return a value, the default value for that UI element is returned to the client.</span></span>

## <a name="when-to-use-this-technique"></a><span data-ttu-id="5fdc7-110">Cuándo usar esta técnica</span><span class="sxs-lookup"><span data-stu-id="5fdc7-110">When to Use This Technique</span></span>

<span data-ttu-id="5fdc7-111">Use esta técnica Si desea invalidar las propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para un objeto.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-111">Use this technique when you want to override the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties for an object.</span></span> <span data-ttu-id="5fdc7-112">Esta técnica es mucho más sencilla que las técnicas de **IAccessible** anteriores.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-112">This technique is much simpler than previous **IAccessible** techniques.</span></span> <span data-ttu-id="5fdc7-113">Para obtener más información, vea [alternativas a la anotación dinámica](alternatives-to-dynamic-annotation.md).</span><span class="sxs-lookup"><span data-stu-id="5fdc7-113">For more information, see [Alternatives to Dynamic Annotation](alternatives-to-dynamic-annotation.md).</span></span>

<span data-ttu-id="5fdc7-114">No se puede usar la anotación del servidor para modificar la estructura del objeto expuesto.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-114">You cannot use server annotation to alter the exposed object structure.</span></span> <span data-ttu-id="5fdc7-115">Para cambiar la estructura de un objeto, debe implementar un puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) completo.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-115">To change the structure of an object, you must implement a full [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span>

<span data-ttu-id="5fdc7-116">Para obtener más información sobre la anotación del servidor, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="5fdc7-116">For more information on server annotation, see the following topics:</span></span>

-   [<span data-ttu-id="5fdc7-117">Usar la anotación del servidor</span><span class="sxs-lookup"><span data-stu-id="5fdc7-117">Using Server Annotation</span></span>](using-server-annotation.md)
-   [<span data-ttu-id="5fdc7-118">Ejemplo de anotación de servidor</span><span class="sxs-lookup"><span data-stu-id="5fdc7-118">Server Annotation Sample</span></span>](server-annotation-sample.md)

 

 




