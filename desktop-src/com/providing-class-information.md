---
title: Proporcionar información de clase
description: Proporcionar información de clase
ms.assetid: 808d9a39-4511-4aba-a23f-3c929970503b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc4505a12d4a7f50a605cbd04cae33805db2b19b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148802"
---
# <a name="providing-class-information"></a><span data-ttu-id="29734-103">Proporcionar información de clase</span><span class="sxs-lookup"><span data-stu-id="29734-103">Providing Class Information</span></span>

<span data-ttu-id="29734-104">A menudo resulta útil que un cliente de un objeto examine la información de tipo del objeto.</span><span class="sxs-lookup"><span data-stu-id="29734-104">It is often useful for a client of an object to examine the object's type information.</span></span> <span data-ttu-id="29734-105">Dado el CLSID del objeto, un cliente puede localizar la biblioteca de tipos del objeto mediante las entradas del registro y, a continuación, puede examinar la biblioteca de tipos para la entrada de coclase en la biblioteca que coincide con el CLSID.</span><span class="sxs-lookup"><span data-stu-id="29734-105">Given the object's CLSID, a client can locate the object's type library using registry entries and then can scan the type library for the coclass entry in the library matching the CLSID.</span></span>

<span data-ttu-id="29734-106">Sin embargo, no todos los objetos tienen un CLSID, aunque todavía necesitan proporcionar información de tipo.</span><span class="sxs-lookup"><span data-stu-id="29734-106">However, not all objects have a CLSID, although they still need to provide type information.</span></span> <span data-ttu-id="29734-107">Además, es conveniente que un cliente tenga una manera de solicitar simplemente un objeto para su información de tipo en lugar de pasar por todos los tediosas tareas para extraer la misma información de las entradas del registro.</span><span class="sxs-lookup"><span data-stu-id="29734-107">In addition, it is convenient for a client to have a way to simply ask an object for its type information instead of going through all the tedium to extract the same information from registry entries.</span></span> <span data-ttu-id="29734-108">Esta capacidad es importante cuando se trabaja con interfaces de salida en objetos conectables.</span><span class="sxs-lookup"><span data-stu-id="29734-108">This capability is important when dealing with outgoing interfaces on connectable objects.</span></span> <span data-ttu-id="29734-109">(Consulte [uso de IProvideClassInfo](using-iprovideclassinfo.md) para obtener más información sobre cómo los objetos conectables proporcionan esta capacidad).</span><span class="sxs-lookup"><span data-stu-id="29734-109">(See [Using IProvideClassInfo](using-iprovideclassinfo.md) for more information on how connectable objects provide this capability.)</span></span>

<span data-ttu-id="29734-110">En estos casos, un cliente puede consultar el objeto para [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) o [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2).</span><span class="sxs-lookup"><span data-stu-id="29734-110">In these cases, a client can query the object for [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) or [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2).</span></span> <span data-ttu-id="29734-111">Si existen estas interfaces, el cliente llama al método [**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) para obtener la información de tipo de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="29734-111">If these interfaces exist, the client calls the [**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) method to get the type information for the interface.</span></span>

<span data-ttu-id="29734-112">Mediante la implementación de [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) o [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2), un objeto especifica que puede proporcionar información de tipo para toda la clase; es decir, lo que describiría en su sección coclass de su biblioteca de tipos, si tiene uno.</span><span class="sxs-lookup"><span data-stu-id="29734-112">By implementing [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) or [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2), an object specifies that it can provide type information for its entire class; that is, what it would describe in its coclass section of its type library, if it has one.</span></span> <span data-ttu-id="29734-113">[**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) devuelve un puntero **ITypeInfo** que corresponde a la información de coclase del objeto.</span><span class="sxs-lookup"><span data-stu-id="29734-113">[**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) returns an **ITypeInfo** pointer corresponding to the object's coclass information.</span></span> <span data-ttu-id="29734-114">A través de este puntero **ITypeInfo** , el cliente puede examinar todas las definiciones de interfaz de entrada y de salida del objeto.</span><span class="sxs-lookup"><span data-stu-id="29734-114">Through this **ITypeInfo** pointer, the client can examine all the object's incoming and outgoing interface definitions.</span></span>

<span data-ttu-id="29734-115">El objeto también puede proporcionar [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2).</span><span class="sxs-lookup"><span data-stu-id="29734-115">The object can also provide [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2).</span></span> <span data-ttu-id="29734-116">La interfaz **IProvideClassInfo2** es una extensión simple para [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) que facilita y agiliza la recuperación de los identificadores de interfaz de salida de un objeto para su conjunto de eventos predeterminado.</span><span class="sxs-lookup"><span data-stu-id="29734-116">The **IProvideClassInfo2** interface is a simple extension to [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) that makes it quick and easy to retrieve an object's outgoing interface identifiers for its default event set.</span></span> <span data-ttu-id="29734-117">**IProvideClassInfo2** se deriva de **IProvideClassInfo**.</span><span class="sxs-lookup"><span data-stu-id="29734-117">**IProvideClassInfo2** is derived from **IProvideClassInfo**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="29734-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="29734-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29734-119">Clientes y servidores COM</span><span class="sxs-lookup"><span data-stu-id="29734-119">COM Clients and Servers</span></span>](com-clients-and-servers.md)
</dt> </dl>

 

 




