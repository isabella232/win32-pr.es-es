---
title: Buscar un objeto remoto
description: Buscar un objeto remoto
ms.assetid: b329de53-646b-42a2-afa3-06473c3483d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0ce1b2280faaed7be3b5afb25a48438ff1a2b7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103904861"
---
# <a name="locating-a-remote-object"></a><span data-ttu-id="b92d1-103">Buscar un objeto remoto</span><span class="sxs-lookup"><span data-stu-id="b92d1-103">Locating a Remote Object</span></span>

<span data-ttu-id="b92d1-104">Con la llegada de COM para sistemas distribuidos, COM usa el modelo básico para la creación de objetos descrito en [objetos de clase com y CLSID](com-class-objects-and-clsids.md) y agrega más de una manera de buscar un objeto que puede residir en otro sistema de una red, sin sobrecargar la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="b92d1-104">With the advent of COM for distributed systems, COM uses the basic model for object creation described in [COM Class Objects and CLSIDs](com-class-objects-and-clsids.md) and adds more than one way to locate an object that might reside on another system in a network, without overburdening the client application.</span></span>

<span data-ttu-id="b92d1-105">COM ha agregado claves del registro que permiten que un servidor registre el nombre del equipo en el que reside o el equipo en el que se encuentra un almacenamiento existente.</span><span class="sxs-lookup"><span data-stu-id="b92d1-105">COM has added registry keys that permit a server to register the name of the machine on which it resides or the machine where an existing storage is located.</span></span> <span data-ttu-id="b92d1-106">Por lo tanto, las aplicaciones cliente solo necesitan conocer el CLSID del servidor.</span><span class="sxs-lookup"><span data-stu-id="b92d1-106">Therefore, client applications need know only the CLSID of the server.</span></span>

<span data-ttu-id="b92d1-107">Sin embargo, para los casos en los que se desea, COM ha reemplazado a un parámetro reservado previamente de [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) con una estructura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) , que permite a un cliente especificar la ubicación de un servidor.</span><span class="sxs-lookup"><span data-stu-id="b92d1-107">However, for cases where it is desired, COM has replaced a previously reserved parameter of [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) with a [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) structure, which allows a client to specify the location of a server.</span></span> <span data-ttu-id="b92d1-108">Otro valor importante de la función **CoGetClassObject** es la enumeración [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) , que especifica si el objeto esperado se va a ejecutar en proceso, local fuera de proceso o remoto fuera de proceso.</span><span class="sxs-lookup"><span data-stu-id="b92d1-108">Another important value in the **CoGetClassObject** function is the [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) enumeration, which specifies whether the expected object is to be run in-process, out-of-process local, or out-of-process remote.</span></span> <span data-ttu-id="b92d1-109">En conjunto, estos dos valores y los valores del registro determinan cómo y dónde se va a ejecutar el objeto.</span><span class="sxs-lookup"><span data-stu-id="b92d1-109">Taken together, these two values and the values in the registry determine how and where the object is to be run.</span></span>

> [!Note]  
> <span data-ttu-id="b92d1-110">Las llamadas de creación de instancia, cuando especifican una ubicación de servidor, pueden invalidar una configuración del registro.</span><span class="sxs-lookup"><span data-stu-id="b92d1-110">Instance creation calls, when they specify a server location, can override a registry setting.</span></span> <span data-ttu-id="b92d1-111">El algoritmo que utiliza COM para ello se describe en la referencia de la enumeración [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) .</span><span class="sxs-lookup"><span data-stu-id="b92d1-111">The algorithm COM uses for doing this is described in the reference for the [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) enumeration.</span></span>

 

<span data-ttu-id="b92d1-112">La activación remota depende de la relación de seguridad entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="b92d1-112">Remote activation depends on the security relationship between client and server.</span></span> <span data-ttu-id="b92d1-113">Para obtener más información, vea [seguridad en com](security-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="b92d1-113">For more information, see [Security in COM](security-in-com.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b92d1-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b92d1-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b92d1-115">Objetos de clase COM y CLSID</span><span class="sxs-lookup"><span data-stu-id="b92d1-115">COM Class Objects and CLSIDs</span></span>](com-class-objects-and-clsids.md)
</dt> <dt>

[<span data-ttu-id="b92d1-116">Crear un objeto a través de un objeto de clase</span><span class="sxs-lookup"><span data-stu-id="b92d1-116">Creating an Object Through a Class Object</span></span>](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 