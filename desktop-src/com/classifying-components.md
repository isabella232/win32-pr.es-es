---
title: Clasificar componentes
description: Clasificar componentes
ms.assetid: 4d805532-96c9-400d-b78a-f8d0d9bdbf83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ea1547c219a44262fdeaf7edb02f65c7a3aac6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903710"
---
# <a name="classifying-components"></a><span data-ttu-id="687c6-103">Clasificar componentes</span><span class="sxs-lookup"><span data-stu-id="687c6-103">Classifying Components</span></span>

<span data-ttu-id="687c6-104">Aunque un cliente puede examinar la lista de CLSID en el registro y seleccionar un componente que se va a usar, la carga de cada componente en el registro y la consulta de las interfaces compatibles son muy lentas.</span><span class="sxs-lookup"><span data-stu-id="687c6-104">While a client is able to browse through the list of CLSIDs in the registry and select a component to use, loading each component in the registry and querying it for its supported interfaces is very time-consuming.</span></span> <span data-ttu-id="687c6-105">Para determinar si un componente admite las interfaces requeridas antes de crear una instancia del componente, se desarrolló un método para clasificar los componentes en categorías.</span><span class="sxs-lookup"><span data-stu-id="687c6-105">To determine whether a component supports the interfaces required before creating an instance of the component, a method to classify components into categories was developed.</span></span>

<span data-ttu-id="687c6-106">Una categoría de componente es un conjunto de interfaces a las que se ha asignado un GUID denominado CATId.</span><span class="sxs-lookup"><span data-stu-id="687c6-106">A component category is a set of interfaces that have been assigned a GUID named CATID.</span></span> <span data-ttu-id="687c6-107">Los componentes que implementan todas las interfaces de una categoría de componente se registran como miembros de esa categoría de componente.</span><span class="sxs-lookup"><span data-stu-id="687c6-107">Components that implement all of the interfaces in a component category register themselves as members of that component category.</span></span> <span data-ttu-id="687c6-108">Los componentes que pertenecen a una determinada categoría de componentes se pueden seleccionar en el registro.</span><span class="sxs-lookup"><span data-stu-id="687c6-108">Components that belong to a certain component category can then be selected from the registry.</span></span> <span data-ttu-id="687c6-109">Al registrarse como miembro de una categoría de componente, el componente garantiza que admita todas las interfaces de miembro de la categoría de componentes.</span><span class="sxs-lookup"><span data-stu-id="687c6-109">By registering itself as a member of a component category, the component is guaranteeing that it supports all of the member interfaces in the component category.</span></span>

<span data-ttu-id="687c6-110">Un componente puede ser un miembro de muchas categorías.</span><span class="sxs-lookup"><span data-stu-id="687c6-110">A component can be a member of many categories.</span></span> <span data-ttu-id="687c6-111">No se limita a admitir interfaces en una categoría de componentes.</span><span class="sxs-lookup"><span data-stu-id="687c6-111">It is not limited to supporting interfaces in a component category.</span></span> <span data-ttu-id="687c6-112">Puede admitir cualquier interfaz, además de las de una categoría de componente.</span><span class="sxs-lookup"><span data-stu-id="687c6-112">It can support any interface, in addition to those in a component category.</span></span>

<span data-ttu-id="687c6-113">A diferencia del registro estándar de componentes, en el que los desarrolladores deben escribir código que registre los objetos manualmente, la categoría de componentes automatiza gran parte de este trabajo.</span><span class="sxs-lookup"><span data-stu-id="687c6-113">In contrast to the standard registration of components, in which developers must write code that manually registers objects, component categories automates much of this work.</span></span> <span data-ttu-id="687c6-114">Los seis métodos de la interfaz [**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) definen categorías de componentes y registran objetos que los implementan o requieren.</span><span class="sxs-lookup"><span data-stu-id="687c6-114">The six methods of the [**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) interface define component categories and register objects that implement or require them.</span></span> <span data-ttu-id="687c6-115">El objeto de [Administrador de categorías de componentes](the-component-categories-manager.md) implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="687c6-115">The [Component Categories Manager](the-component-categories-manager.md) object implements this interface.</span></span> <span data-ttu-id="687c6-116">Vea **ICatRegister** y [**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) para obtener información adicional sobre el uso de categorías de componentes.</span><span class="sxs-lookup"><span data-stu-id="687c6-116">See **ICatRegister** and [**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) for additional information on using component categories.</span></span>

## <a name="related-topics"></a><span data-ttu-id="687c6-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="687c6-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="687c6-118">Registro de aplicaciones COM</span><span class="sxs-lookup"><span data-stu-id="687c6-118">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 




