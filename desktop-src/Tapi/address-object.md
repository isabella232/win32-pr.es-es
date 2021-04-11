---
description: El objeto Address representa una entidad que puede realizar o recibir llamadas.
ms.assetid: ab6db262-f99e-4027-9525-7597fcf02e72
title: Objeto Address
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ae91e70d6d8efb56321ca4619c6eb973799024
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911233"
---
# <a name="address-object"></a><span data-ttu-id="66f94-103">Objeto Address</span><span class="sxs-lookup"><span data-stu-id="66f94-103">Address Object</span></span>

<span data-ttu-id="66f94-104">El objeto Address representa una entidad que puede realizar o recibir llamadas.</span><span class="sxs-lookup"><span data-stu-id="66f94-104">The Address object represents an entity that can make or receive calls.</span></span> <span data-ttu-id="66f94-105">Este objeto expone interfaces y métodos que permiten a una aplicación realizar una serie de operaciones, como:</span><span class="sxs-lookup"><span data-stu-id="66f94-105">This object exposes interfaces and methods that allow an application to perform a number of operations, such as:</span></span>

-   <span data-ttu-id="66f94-106">Detecta si una dirección especificada puede admitir un conjunto determinado de necesidades de tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="66f94-106">Discover whether a specified address can support a particular set of media type needs.</span></span>
-   <span data-ttu-id="66f94-107">Enumerar las llamadas asociadas actualmente a la dirección.</span><span class="sxs-lookup"><span data-stu-id="66f94-107">Enumerate calls currently associated with the address.</span></span>
-   <span data-ttu-id="66f94-108">Crear o reenviar llamadas.</span><span class="sxs-lookup"><span data-stu-id="66f94-108">Create or forward calls.</span></span>
-   <span data-ttu-id="66f94-109">Obtiene el nombre del proveedor de servicios asociado.</span><span class="sxs-lookup"><span data-stu-id="66f94-109">Get the name of the associated service provider.</span></span>
-   <span data-ttu-id="66f94-110">Si existe un proveedor de servicios multimedia, obtenga punteros de interfaz que permitan la manipulación detallada del terminal.</span><span class="sxs-lookup"><span data-stu-id="66f94-110">If a media service provider exists, get interface pointers that allow detailed terminal manipulation.</span></span>
-   <span data-ttu-id="66f94-111">Obtiene y establece otra información, como si un mensaje está en espera.</span><span class="sxs-lookup"><span data-stu-id="66f94-111">Get and set other information, such as whether a message is waiting.</span></span>

<span data-ttu-id="66f94-112">La mayoría de las direcciones están asociadas a un terminal, pero no es el caso de forma uniforme.</span><span class="sxs-lookup"><span data-stu-id="66f94-112">Most addresses are associated with a terminal, but this is not uniformly the case.</span></span> <span data-ttu-id="66f94-113">Por ejemplo, un TSP remoto que proporciona acceso al equipo en un servidor tendrá una dirección en el equipo local, pero no un terminal.</span><span class="sxs-lookup"><span data-stu-id="66f94-113">For example, a remote TSP that provides access to equipment on a server will have an address on the local machine but not a terminal.</span></span> <span data-ttu-id="66f94-114">Un módem sin altavoz tampoco tiene ningún terminal asociado a su dirección.</span><span class="sxs-lookup"><span data-stu-id="66f94-114">A speakerless modem also has no terminal associated with its address.</span></span>

<span data-ttu-id="66f94-115">Si una dirección no tiene un terminal asociado, la interfaz [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) no se expone en el objeto.</span><span class="sxs-lookup"><span data-stu-id="66f94-115">If an address does not have an associated terminal, the [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) interface is not exposed on the object.</span></span>

<span data-ttu-id="66f94-116">En el ejemplo de código [seleccionar una dirección](select-an-address.md) se muestra el proceso básico para adquirir un puntero de objeto de dirección.</span><span class="sxs-lookup"><span data-stu-id="66f94-116">The [Select an Address](select-an-address.md) code example shows the basic process for acquiring an address object pointer.</span></span>

<span data-ttu-id="66f94-117">Vea [interfaces del objeto Address](address-object-interfaces.md) para obtener una lista de todas las interfaces asociadas al objeto Address.</span><span class="sxs-lookup"><span data-stu-id="66f94-117">See [Address Object Interfaces](address-object-interfaces.md) for a list of all interfaces associated with the Address object.</span></span>

 

 
