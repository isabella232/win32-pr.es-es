---
description: Conjuntos de propiedades
ms.assetid: 4b8a917f-7a6c-4433-83f4-b83ef6d26115
title: Conjuntos de propiedades (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcdc65efbc99eeed3a5f94ab33ce5ec982975852
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422868"
---
# <a name="property-sets-directshow"></a><span data-ttu-id="42a2c-103">Conjuntos de propiedades (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="42a2c-103">Property Sets (DirectShow)</span></span>

<span data-ttu-id="42a2c-104">Microsoft DirectShow usa conjuntos de propiedades para admitir los servicios extendidos ofrecidos por el hardware y sus controladores y filtros asociados.</span><span class="sxs-lookup"><span data-stu-id="42a2c-104">Microsoft DirectShow uses property sets to support extended services offered by hardware and its associated drivers and filters.</span></span> <span data-ttu-id="42a2c-105">Los proveedores de hardware y filtro pueden definir nuevas capacidades como propiedades, organizarlas en conjuntos de propiedades y publicar la especificación de estos conjuntos de propiedades.</span><span class="sxs-lookup"><span data-stu-id="42a2c-105">Hardware and filter vendors can define new capabilities as properties, arrange them in property sets, and publish the specification for these property sets.</span></span> <span data-ttu-id="42a2c-106">Como desarrollador de la aplicación, puede usar los métodos de la interfaz [**IKsPropertySet**](ikspropertyset.md) para determinar si un controlador o filtro admite un conjunto determinado de propiedades y recuperar o establecer esas propiedades.</span><span class="sxs-lookup"><span data-stu-id="42a2c-106">As the application developer, you can use the methods of the [**IKsPropertySet**](ikspropertyset.md) interface to determine whether a driver or filter supports a particular set of properties, and retrieve or set those properties.</span></span>

<span data-ttu-id="42a2c-107">Todos los métodos expuestos por **IKsPropertySet** requieren un **GUID** que identifique el conjunto de propiedades (el parámetro *GuidPropSet* ) y un **valor DWORD** que identifique la propiedad dentro del conjunto de propiedades (el parámetro *dwPropID* ).</span><span class="sxs-lookup"><span data-stu-id="42a2c-107">All the methods exposed by **IKsPropertySet** require a **GUID** that identifies the property set (the *guidPropSet* parameter) and a **DWORD** that identifies the property within the property set (the *dwPropID* parameter).</span></span> <span data-ttu-id="42a2c-108">El parámetro *dwPropID* normalmente es un miembro de un tipo de datos enumerados.</span><span class="sxs-lookup"><span data-stu-id="42a2c-108">The *dwPropID* parameter is typically a member of an enumerated data type.</span></span>

<span data-ttu-id="42a2c-109">Las propiedades individuales pueden tener los datos asociados que se especifican en el parámetro *pPropData* en los métodos [**IKsPropertySet:: set**](ikspropertyset-set.md) y [**IKsPropertySet:: get**](ikspropertyset-get.md) .</span><span class="sxs-lookup"><span data-stu-id="42a2c-109">Individual properties can have associated data that you specify in the *pPropData* parameter in the [**IKsPropertySet::Set**](ikspropertyset-set.md) and [**IKsPropertySet::Get**](ikspropertyset-get.md) methods.</span></span> <span data-ttu-id="42a2c-110">En estos métodos, los datos de la propiedad se escriben como un puntero a `void` .</span><span class="sxs-lookup"><span data-stu-id="42a2c-110">In these methods, the property data is typed as a pointer to `void`.</span></span> <span data-ttu-id="42a2c-111">El tipo de datos y el significado de los datos se especifican en la definición del conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="42a2c-111">The data type and the meaning of the data are specified in the definition of the property set.</span></span>

<span data-ttu-id="42a2c-112">En las secciones siguientes se proporciona información sobre los conjuntos de propiedades admitidos en DirectShow:</span><span class="sxs-lookup"><span data-stu-id="42a2c-112">The following sections provide information about the property sets supported in DirectShow:</span></span>

-   [<span data-ttu-id="42a2c-113">**Conjunto de propiedades de protección de copia de DVD**</span><span class="sxs-lookup"><span data-stu-id="42a2c-113">**DVD Copy Protection Property Set**</span></span>](dvd-copy-protection-property-set.md)
-   [<span data-ttu-id="42a2c-114">**Conjunto de propiedades de Karaoke de DVD**</span><span class="sxs-lookup"><span data-stu-id="42a2c-114">**DVD Karaoke Property Set**</span></span>](dvd-karaoke-property-set.md)
-   [<span data-ttu-id="42a2c-115">**Conjunto de propiedades de subimagen de DVD**</span><span class="sxs-lookup"><span data-stu-id="42a2c-115">**DVD Subpicture Property Set**</span></span>](dvd-subpicture-property-set.md)
-   [<span data-ttu-id="42a2c-116">Conjunto de propiedades de transporte de dispositivo externo</span><span class="sxs-lookup"><span data-stu-id="42a2c-116">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
-   [<span data-ttu-id="42a2c-117">Conjunto de propiedades de ejecución de fotogramas</span><span class="sxs-lookup"><span data-stu-id="42a2c-117">Frame Stepping Property Set</span></span>](frame-stepping-property-set.md)
-   [<span data-ttu-id="42a2c-118">Conjunto de propiedades de PIN</span><span class="sxs-lookup"><span data-stu-id="42a2c-118">Pin Property Set</span></span>](pin-property-set.md)
-   [<span data-ttu-id="42a2c-119">**Conjunto de propiedades de cambio de velocidad**</span><span class="sxs-lookup"><span data-stu-id="42a2c-119">**Rate Change Property Set**</span></span>](rate-change-property-set.md)

 

 



