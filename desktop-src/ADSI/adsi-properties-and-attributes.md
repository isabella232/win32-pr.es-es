---
title: Propiedades y atributos ADSI
description: Los atributos a veces se denominan propiedades. Esto puede causar confusión. En esta documentación se usan las siguientes definiciones para propiedades y atributos.
ms.assetid: 8e391d36-5a8d-4960-805a-0caf281cab80
ms.tgt_platform: multiple
keywords:
- Propiedades ADSI y atributos ADSI
- ADSI ADSI, uso, acceso y manipulación de datos, propiedades y atributos
- ADSI de propiedades
- atributos ADSI
- propiedades ADSI, definidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c7b1dca9882f53b7fa746121ed431ace7f9af7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656199"
---
# <a name="adsi-properties-and-attributes"></a><span data-ttu-id="8ef26-110">Propiedades y atributos ADSI</span><span class="sxs-lookup"><span data-stu-id="8ef26-110">ADSI Properties and Attributes</span></span>

<span data-ttu-id="8ef26-111">Los atributos a veces se denominan propiedades.</span><span class="sxs-lookup"><span data-stu-id="8ef26-111">Attributes are sometimes referred to as properties.</span></span> <span data-ttu-id="8ef26-112">Esto puede causar confusión.</span><span class="sxs-lookup"><span data-stu-id="8ef26-112">This can cause confusion.</span></span> <span data-ttu-id="8ef26-113">En esta documentación se usan las siguientes definiciones para propiedades y atributos.</span><span class="sxs-lookup"><span data-stu-id="8ef26-113">This documentation uses the following definitions for properties and attributes.</span></span>

<span data-ttu-id="8ef26-114">Las propiedades son valores con nombre asociados a un objeto de programación.</span><span class="sxs-lookup"><span data-stu-id="8ef26-114">Properties are named values associated with a programming object.</span></span> <span data-ttu-id="8ef26-115">Por ejemplo, la interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) expone propiedades como [**Class**](iads-property-methods.md) y **Name**.</span><span class="sxs-lookup"><span data-stu-id="8ef26-115">For example, the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface exposes properties such as [**Class**](iads-property-methods.md) and **Name**.</span></span>

<span data-ttu-id="8ef26-116">Los atributos son los datos asociados a los objetos de un servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="8ef26-116">Attributes are the data associated with objects in a directory service.</span></span> <span data-ttu-id="8ef26-117">Por ejemplo, un objeto de usuario tendrá un atributo denominado **CN** que contiene una cadena que es el nombre distintivo común o relativo del objeto.</span><span class="sxs-lookup"><span data-stu-id="8ef26-117">For example, a user object will have an attribute called **cn** which contains a string that is the common or relative distinguished name of the object.</span></span> <span data-ttu-id="8ef26-118">Se puede obtener acceso a los atributos a través de métodos de interfaz ADSI como [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) y [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put).</span><span class="sxs-lookup"><span data-stu-id="8ef26-118">Attributes are accessible through ADSI interface methods such as [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put).</span></span>

<span data-ttu-id="8ef26-119">Para obtener más información acerca de las propiedades y los atributos ADSI, consulte:</span><span class="sxs-lookup"><span data-stu-id="8ef26-119">For more information about ADSI properties and attributes, see:</span></span>

-   [<span data-ttu-id="8ef26-120">La caché de atributos ADSI</span><span class="sxs-lookup"><span data-stu-id="8ef26-120">The ADSI Attribute Cache</span></span>](the-adsi-attribute-cache.md)
-   [<span data-ttu-id="8ef26-121">Atributos de valor único frente a varios valores</span><span class="sxs-lookup"><span data-stu-id="8ef26-121">Single vs. Multiple Value Attributes</span></span>](single-vs--multiple-value-attributes.md)
-   [<span data-ttu-id="8ef26-122">Active Directory atributos operativos</span><span class="sxs-lookup"><span data-stu-id="8ef26-122">Active Directory Operational Attributes</span></span>](active-directory-operational-attributes.md)

 

 




