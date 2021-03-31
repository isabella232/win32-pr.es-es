---
title: Objetos incrustados (COM)
description: Objetos incrustados
ms.assetid: 1f863fd4-fead-4dd3-b855-8820e015b52a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da9938b17130209fec024f94ee99061ad690693
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149799"
---
# <a name="embedded-objects-com"></a><span data-ttu-id="8a007-103">Objetos incrustados (COM)</span><span class="sxs-lookup"><span data-stu-id="8a007-103">Embedded Objects (COM)</span></span>

<span data-ttu-id="8a007-104">Un objeto incrustado está almacenado físicamente en el documento compuesto, junto con toda la información necesaria para administrar el objeto.</span><span class="sxs-lookup"><span data-stu-id="8a007-104">An embedded object is physically stored in the compound document, along with all the information needed to manage the object.</span></span> <span data-ttu-id="8a007-105">En otras palabras, el objeto incrustado es realmente una parte del documento compuesto en el que reside.</span><span class="sxs-lookup"><span data-stu-id="8a007-105">In other words, the embedded object is actually a part of the compound document in which it resides.</span></span> <span data-ttu-id="8a007-106">Esta disposición tiene un par de desventajas.</span><span class="sxs-lookup"><span data-stu-id="8a007-106">This arrangement has a couple of disadvantages.</span></span> <span data-ttu-id="8a007-107">En primer lugar, un documento compuesto que contiene objetos incrustados será mayor que uno que contenga los mismos objetos que los vínculos.</span><span class="sxs-lookup"><span data-stu-id="8a007-107">First, a compound document containing embedded objects will be larger than one containing the same objects as links.</span></span> <span data-ttu-id="8a007-108">En segundo lugar, los cambios realizados en el origen de un objeto incrustado no se replicarán automáticamente en la copia incrustada, y los cambios en la copia incrustada no se reflejarán en el origen, como si se tratase de un vínculo.</span><span class="sxs-lookup"><span data-stu-id="8a007-108">Second, changes made to the source of an embedded object will not be automatically replicated in the embedded copy, and changes in the embedded copy will not be reflected in the source, as they are with a link.</span></span>

<span data-ttu-id="8a007-109">Aun así, para determinados fines, la incrustación ofrece varias ventajas con respecto a los vínculos.</span><span class="sxs-lookup"><span data-stu-id="8a007-109">Still, for certain purposes, embedding offers several advantages over links.</span></span> <span data-ttu-id="8a007-110">En primer lugar, los usuarios pueden transferir documentos compuestos con objetos incrustados a otros equipos u otras ubicaciones del mismo equipo sin interrumpir un vínculo.</span><span class="sxs-lookup"><span data-stu-id="8a007-110">First, users can transfer compound documents with embedded objects to other computers, or other locations on the same computer, without breaking a link.</span></span> <span data-ttu-id="8a007-111">En segundo lugar, los usuarios pueden modificar los objetos incrustados sin cambiar el contenido de la original.</span><span class="sxs-lookup"><span data-stu-id="8a007-111">Second, users can edit embedded objects without changing the content of the original.</span></span> <span data-ttu-id="8a007-112">A veces, esta separación es precisamente lo que se necesita.</span><span class="sxs-lookup"><span data-stu-id="8a007-112">Sometimes, this separation is precisely what is required.</span></span> <span data-ttu-id="8a007-113">En tercer lugar, los objetos incrustados se pueden activar en contexto, lo que significa que el usuario puede editar o manipular de otro modo el objeto sin tener que trabajar en una ventana independiente de la del contenedor del objeto.</span><span class="sxs-lookup"><span data-stu-id="8a007-113">Third, embedded objects can be activated in place, meaning that the user can edit or otherwise manipulate the object without having to work in a separate window from that of the object's container.</span></span> <span data-ttu-id="8a007-114">En su lugar, cuando se activa el objeto, la interfaz de usuario de la aplicación contenedora cambia para exponer las herramientas necesarias para administrar o modificar el objeto.</span><span class="sxs-lookup"><span data-stu-id="8a007-114">Instead, when the object is activated, the container application's user interface changes to expose those tools that are necessary to manage or modify the object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a007-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8a007-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a007-116">Crear objetos vinculados e incrustados a partir de datos existentes</span><span class="sxs-lookup"><span data-stu-id="8a007-116">Creating Linked and Embedded Objects from Existing Data</span></span>](creating-linked-and-embedded-objects-from-existing-data.md)
</dt> </dl>

 

 




