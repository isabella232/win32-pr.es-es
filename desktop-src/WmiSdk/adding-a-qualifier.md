---
description: Un calificador es una cadena de datos que proporciona más información sobre una clase, una instancia, una propiedad, un método o un parámetro.
ms.assetid: 6984b575-b365-49dd-aeab-a763430f434c
ms.tgt_platform: multiple
title: Adición de un calificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5a6f18f2b79bcd25b2b4ca75811157c9091e6eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697892"
---
# <a name="adding-a-qualifier"></a><span data-ttu-id="33aa4-103">Adición de un calificador</span><span class="sxs-lookup"><span data-stu-id="33aa4-103">Adding a Qualifier</span></span>

<span data-ttu-id="33aa4-104">Un calificador es una cadena de datos que proporciona más información sobre una clase, una instancia, una propiedad, un método o un parámetro.</span><span class="sxs-lookup"><span data-stu-id="33aa4-104">A qualifier is a data string that provides more information about a class, instance, property, method, or parameter.</span></span>

<span data-ttu-id="33aa4-105">La definición de clase siguiente es un ejemplo de una clase derivada que tiene calificadores de clase.</span><span class="sxs-lookup"><span data-stu-id="33aa4-105">The following class definition is an example of a derived class that has class qualifiers.</span></span>

``` syntax
[Dynamic, Provider ("ProviderX")] 
class MyDerivedClass : MyClass
{
    [key] string sKey;
    [Implemented] sint32 ValueMethod();
    [Implemented] sint32 MyMethod ([in, Id(0)] sint32 Param);
};
```

<span data-ttu-id="33aa4-106">Los calificadores se pueden dividir en calificadores estándar, calificadores CIM y calificadores únicos, entre los que se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="33aa4-106">Qualifiers can be divided into standard qualifiers, CIM qualifiers, and unique qualifiers include the following:</span></span>

-   <span data-ttu-id="33aa4-107">Calificador estándar</span><span class="sxs-lookup"><span data-stu-id="33aa4-107">Standard qualifier</span></span>

    <span data-ttu-id="33aa4-108">Un calificador estándar es un calificador definido por WMI que se usa habitualmente en código MOF.</span><span class="sxs-lookup"><span data-stu-id="33aa4-108">A standard qualifier is a qualifier defined by WMI and commonly used in MOF code.</span></span> <span data-ttu-id="33aa4-109">Por ejemplo, los calificadores [**dinámicos**](dynamic-qualifier.md) y de [**lectura**](standard-qualifiers.md) son calificadores estándar.</span><span class="sxs-lookup"><span data-stu-id="33aa4-109">For example, the [**Dynamic**](dynamic-qualifier.md) and [**Read**](standard-qualifiers.md) qualifiers are both standard qualifiers.</span></span> <span data-ttu-id="33aa4-110">Para obtener más información, vea [calificadores de WMI](wmi-qualifiers.md).</span><span class="sxs-lookup"><span data-stu-id="33aa4-110">For more information, see [WMI Qualifiers](wmi-qualifiers.md).</span></span>

-   <span data-ttu-id="33aa4-111">Calificador de CIM</span><span class="sxs-lookup"><span data-stu-id="33aa4-111">CIM qualifier</span></span>

    <span data-ttu-id="33aa4-112">Un calificador de CIM es un calificador incluido en la especificación CIM.</span><span class="sxs-lookup"><span data-stu-id="33aa4-112">A CIM qualifier is a qualifier included in the CIM specification.</span></span> <span data-ttu-id="33aa4-113">Aunque use calificadores CIM en código MOF, los calificadores estándar se han diseñado específicamente con WMI en mente.</span><span class="sxs-lookup"><span data-stu-id="33aa4-113">While use CIM qualifiers in MOF code, the standard qualifiers are designed specifically with WMI in mind.</span></span> <span data-ttu-id="33aa4-114">Para obtener más información, consulte la [especificación de CIM](https://www.dmtf.org/spec/cims.html/)de DMTF.</span><span class="sxs-lookup"><span data-stu-id="33aa4-114">For more information, see the DMTF [CIM Specification](https://www.dmtf.org/spec/cims.html/).</span></span>

-   <span data-ttu-id="33aa4-115">Calificador único</span><span class="sxs-lookup"><span data-stu-id="33aa4-115">Unique qualifier</span></span>

    <span data-ttu-id="33aa4-116">Un calificador único es un calificador definido específicamente para una nueva clase por parte de un proveedor de clases.</span><span class="sxs-lookup"><span data-stu-id="33aa4-116">A unique qualifier is a qualifier defined specifically for a new class by a class provider.</span></span> <span data-ttu-id="33aa4-117">Por ejemplo, el calificador de [**unidades**](standard-qualifiers.md) es un calificador no estándar específico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="33aa4-117">For example, the [**Units**](standard-qualifiers.md) qualifier is a nonstandard, provider-specific qualifier.</span></span> <span data-ttu-id="33aa4-118">Puede crear sus propios calificadores para usarlos con su proveedor.</span><span class="sxs-lookup"><span data-stu-id="33aa4-118">You can create your own qualifiers for use with your provider.</span></span> <span data-ttu-id="33aa4-119">Para obtener más información sobre la creación de un proveedor, vea [desarrollar un proveedor WMI](developing-a-wmi-provider.md).</span><span class="sxs-lookup"><span data-stu-id="33aa4-119">For more information about creating a provider, see [Developing a WMI Provider](developing-a-wmi-provider.md).</span></span>

<span data-ttu-id="33aa4-120">Sea cual sea su calificador, el proceso principal que realice es usar el calificador en el código MOF.</span><span class="sxs-lookup"><span data-stu-id="33aa4-120">Whatever your qualifier does, the main process you perform is to use the qualifier in your MOF code.</span></span> <span data-ttu-id="33aa4-121">Para obtener más información, vea [aplicar un calificador](applying-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="33aa4-121">For more information, see [Applying a Qualifier](applying-a-qualifier.md).</span></span> <span data-ttu-id="33aa4-122">Puede describir más detalladamente un calificador con un tipo de calificador.</span><span class="sxs-lookup"><span data-stu-id="33aa4-122">You can further describe a qualifier with a qualifier flavor.</span></span> <span data-ttu-id="33aa4-123">Un tipo de calificador contiene más información sobre cómo un proveedor debe usar un calificador.</span><span class="sxs-lookup"><span data-stu-id="33aa4-123">A qualifier flavor contains more information regarding how a provider should use a qualifier.</span></span> <span data-ttu-id="33aa4-124">Para obtener más información, vea [Descripción de un calificador con un tipo de calificador](describing-a-qualifier-with-a-qualifier-flavor.md).</span><span class="sxs-lookup"><span data-stu-id="33aa4-124">For more information, see [Describing a Qualifier with a Qualifier Flavor](describing-a-qualifier-with-a-qualifier-flavor.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="33aa4-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="33aa4-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33aa4-126">Diseñar clases de Managed Object Format (MOF)</span><span class="sxs-lookup"><span data-stu-id="33aa4-126">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



