---
description: Cómo implementar IUnknown
ms.assetid: 4e363ccb-9725-4be6-bb31-283bf1d658f5
title: Cómo implementar IUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27c12e25d56adab1841a375ac6c1ce0857a73b5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536526"
---
# <a name="how-to-implement-iunknown"></a><span data-ttu-id="dfb1b-103">Cómo implementar IUnknown</span><span class="sxs-lookup"><span data-stu-id="dfb1b-103">How to Implement IUnknown</span></span>

<span data-ttu-id="dfb1b-104">Microsoft DirectShow se basa en el modelo de objetos componentes (COM).</span><span class="sxs-lookup"><span data-stu-id="dfb1b-104">Microsoft DirectShow is based on the Component Object Model (COM).</span></span> <span data-ttu-id="dfb1b-105">Si escribe su propio filtro, debe implementarlo como un objeto COM.</span><span class="sxs-lookup"><span data-stu-id="dfb1b-105">If you write your own filter, you must implement it as a COM object.</span></span> <span data-ttu-id="dfb1b-106">Las clases base de DirectShow proporcionan un marco desde el que realizar esta tarea.</span><span class="sxs-lookup"><span data-stu-id="dfb1b-106">The DirectShow base classes provide a framework from which to do this.</span></span> <span data-ttu-id="dfb1b-107">No es necesario usar las clases base, pero puede simplificar el proceso de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="dfb1b-107">Using the base classes is not required, but it can simplify the development process.</span></span> <span data-ttu-id="dfb1b-108">En este artículo se describen algunos de los detalles internos de los objetos COM y su implementación en las clases base de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="dfb1b-108">This article describes some of the internal details of COM objects and their implementation in the DirectShow base classes.</span></span>

<span data-ttu-id="dfb1b-109">En este artículo se supone que sabe cómo programar aplicaciones cliente COM (es decir, que comprende los métodos en **IUnknown**), pero no supone ninguna experiencia previa en el desarrollo de objetos com.</span><span class="sxs-lookup"><span data-stu-id="dfb1b-109">This article assumes that you know how to program COM client applications—in other words, that you understand the methods in **IUnknown**—but does not assume any prior experience developing COM objects.</span></span> <span data-ttu-id="dfb1b-110">DirectShow controla muchos de los detalles del desarrollo de un objeto COM.</span><span class="sxs-lookup"><span data-stu-id="dfb1b-110">DirectShow handles many of the details of developing a COM object.</span></span> <span data-ttu-id="dfb1b-111">Si tiene experiencia en el desarrollo de objetos COM, debe leer la sección [uso de CUnknown](using-cunknown.md), que describe la clase base [**CUnknown**](cunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="dfb1b-111">If you have experience developing COM objects, you should read the section [Using CUnknown](using-cunknown.md), which describes the [**CUnknown**](cunknown.md) base class.</span></span>

<span data-ttu-id="dfb1b-112">COM es una especificación, no una implementación de.</span><span class="sxs-lookup"><span data-stu-id="dfb1b-112">COM is a specification, not an implementation.</span></span> <span data-ttu-id="dfb1b-113">Define las reglas que debe seguir un componente; poner esas reglas en vigor se deja al desarrollador.</span><span class="sxs-lookup"><span data-stu-id="dfb1b-113">It defines the rules that a component must follow; putting those rules into effect is left to the developer.</span></span> <span data-ttu-id="dfb1b-114">En DirectShow, todos los objetos se derivan de un conjunto de clases base de C++.</span><span class="sxs-lookup"><span data-stu-id="dfb1b-114">In DirectShow, all objects derive from a set of C++ base classes.</span></span> <span data-ttu-id="dfb1b-115">Los métodos y constructores de la clase base realizan la mayor parte del trabajo "contabilidad" COM, por ejemplo, mantener un recuento de referencias coherente.</span><span class="sxs-lookup"><span data-stu-id="dfb1b-115">The base class constructors and methods do most of the COM "bookkeeping" work, such as keeping a consistent reference count.</span></span> <span data-ttu-id="dfb1b-116">Al derivar el filtro de una clase base, se hereda la funcionalidad de la clase.</span><span class="sxs-lookup"><span data-stu-id="dfb1b-116">By deriving your filter from a base class, you inherit the functionality of the class.</span></span> <span data-ttu-id="dfb1b-117">Para utilizar eficazmente las clases base, se necesita una descripción general de cómo implementan la especificación COM.</span><span class="sxs-lookup"><span data-stu-id="dfb1b-117">To use base classes effectively, you need a general understanding of how they implement the COM specification.</span></span>

<span data-ttu-id="dfb1b-118">Este artículo contiene los siguientes temas.</span><span class="sxs-lookup"><span data-stu-id="dfb1b-118">This article contains the following topics.</span></span>

-   [<span data-ttu-id="dfb1b-119">Cómo funciona IUnknown</span><span class="sxs-lookup"><span data-stu-id="dfb1b-119">How IUnknown Works</span></span>](how-iunknown-works.md)
-   [<span data-ttu-id="dfb1b-120">Usar CUnknown</span><span class="sxs-lookup"><span data-stu-id="dfb1b-120">Using CUnknown</span></span>](using-cunknown.md)

## <a name="related-topics"></a><span data-ttu-id="dfb1b-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dfb1b-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfb1b-122">DirectShow y COM</span><span class="sxs-lookup"><span data-stu-id="dfb1b-122">DirectShow and COM</span></span>](directshow-and-com.md)
</dt> </dl>

 

 



