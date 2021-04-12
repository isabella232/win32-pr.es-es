---
description: Un tipo de calificador es una marca que describe más información sobre un calificador.
ms.assetid: a7d9d1c0-9386-4c90-9788-993b35ed12db
ms.tgt_platform: multiple
title: Describir un calificador con un tipo de calificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525cfc2c590ec8916e2e9538b3e8224e97b3b5dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276261"
---
# <a name="describing-a-qualifier-with-a-qualifier-flavor"></a><span data-ttu-id="ba1f4-103">Describir un calificador con un tipo de calificador</span><span class="sxs-lookup"><span data-stu-id="ba1f4-103">Describing a Qualifier with a Qualifier Flavor</span></span>

<span data-ttu-id="ba1f4-104">Un [*tipo de calificador*](gloss-q.md) es una marca que describe más información sobre un calificador.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-104">A [*qualifier flavor*](gloss-q.md) is a flag that describes more information about a qualifier.</span></span> <span data-ttu-id="ba1f4-105">Por ejemplo, el tipo de calificador restringido indica que WMI no debe propagar el calificador asociado a ninguna clase o instancia derivada.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-105">For example, the Restricted qualifier flavor states that WMI should not propagate the associated qualifier to any derived classes or instances.</span></span> <span data-ttu-id="ba1f4-106">Puede establecer sabores mediante código MOF o mediante programación.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-106">You can set flavors using either MOF code or programmatically.</span></span> <span data-ttu-id="ba1f4-107">Aunque puede describir una variedad de efectos con sabores, los principales propósitos de las marcas de sabor consisten en definir cómo WMI propaga los calificadores a través de la herencia.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-107">While you can describe a variety of effects with flavors, the main purposes of flavor flags is to define how WMI propagates qualifiers through inheritance.</span></span>

<span data-ttu-id="ba1f4-108">WMI define varios tipos de calificador que se pueden adjuntar a cualquier calificador, independientemente del origen del calificador.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-108">WMI defines several qualifier flavors that you can attach to any qualifier, regardless of the origin of the qualifier.</span></span> <span data-ttu-id="ba1f4-109">Sin embargo, algunas versiones no son adecuadas para todos los tipos de calificador.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-109">However, some flavors are not appropriate for all qualifier types.</span></span> <span data-ttu-id="ba1f4-110">Por ejemplo, el tipo **ToSubClass** solo es adecuado para los calificadores definidos para una clase.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-110">The **ToSubClass** flavor, for example, is appropriate only for qualifiers defined for a class.</span></span> <span data-ttu-id="ba1f4-111">No se puede adjuntar **ToSubClass** a un calificador usado para describir una instancia.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-111">You cannot attach **ToSubClass** to a qualifier used to describe an instance.</span></span>

<span data-ttu-id="ba1f4-112">Puede usar tipos para describir diferentes efectos para los calificadores.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-112">You can use flavors to describe a variety of different effects for qualifiers.</span></span> <span data-ttu-id="ba1f4-113">Por ejemplo, Flavor puede indicar si se puede localizar un calificador.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-113">For example, flavor can indicate if a qualifier can be localized.</span></span> <span data-ttu-id="ba1f4-114">Sin embargo, uno de los principales propósitos de un tipo de calificador es describir si una clase primaria puede pasar calificadores a una subclase o instancia de clase.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-114">However, one of the main purposes of a qualifier flavor is to describe whether a parent class can pass qualifiers to a subclass or class instance.</span></span> <span data-ttu-id="ba1f4-115">También puede usar tipos para determinar si una propiedad de clase pasa un calificador a una propiedad de instancia.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-115">You can also use flavors to determine if a class property passes a qualifier on to an instance property.</span></span> <span data-ttu-id="ba1f4-116">Por último, use sabores para indicar si una subclase puede reemplazar el valor original de un calificador heredado.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-116">Finally, use flavors to state whether a subclass can override the original value of an inherited qualifier.</span></span> <span data-ttu-id="ba1f4-117">Sin embargo, los calificadores que se declaran para una clase o instancia no se propagan a las propiedades de esa clase o instancia.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-117">However, qualifiers that you declare for a class or instance do not propagate to the properties of that class or instance.</span></span> <span data-ttu-id="ba1f4-118">Además, los tipos que establecen permisos de invalidación solo son válidos si también se establecen los tipos **ToInstance** o **ToSubClass** .</span><span class="sxs-lookup"><span data-stu-id="ba1f4-118">Further, flavors that establish override permissions are valid only if you also set the **ToInstance** or **ToSubClass** flavors.</span></span>

<span data-ttu-id="ba1f4-119">Un tipo se puede asignar globalmente a un calificador para un archivo MOF completo utilizando la sintaxis siguiente en la que el espacio en blanco actúa como delimitador cuando se especifican varios tipos.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-119">A flavor can be globally assigned to a qualifier for an entire MOF file using the following syntax in which white space acts as the delimiter when multiple flavors are specified.</span></span>

``` syntax
Qualifier QualifierName : flavor1 <flavor2...>;
```

<span data-ttu-id="ba1f4-120">Los tipos globales se aplican a todos los usos subsiguientes del calificador en el archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-120">Global flavors apply to all subsequent uses of the qualifier in the MOF file.</span></span> <span data-ttu-id="ba1f4-121">Las instrucciones de tipo global pueden aparecer en cualquier parte del archivo fuera de un bloque de declaración de objeto.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-121">Global flavor statements may occur anywhere in the file outside of an object declaration block.</span></span> <span data-ttu-id="ba1f4-122">Los tipos redefinidos en el nivel de clase, instancia o propiedad reemplazan las declaraciones de tipo globales para el ámbito de ese objeto.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-122">Flavors redefined at the class, instance, or property level override the global flavor declarations for the scope of that object.</span></span>

<span data-ttu-id="ba1f4-123">No se puede definir un nuevo tipo.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-123">You cannot define a new flavor.</span></span> <span data-ttu-id="ba1f4-124">Aunque puede crear un nuevo calificador, use solo los [tipos de calificador](qualifier-flavors.md) existentes para describir el nuevo calificador.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-124">Although you can create a new qualifier, use only existing [Qualifier Flavors](qualifier-flavors.md) to describe your new qualifier.</span></span>

<span data-ttu-id="ba1f4-125">**Para definir los tipos de calificador en MOF**</span><span class="sxs-lookup"><span data-stu-id="ba1f4-125">**To define qualifier flavors in MOF**</span></span>

-   <span data-ttu-id="ba1f4-126">Declare los tipos que describen un calificador determinado después del nombre del calificador, entre los corchetes del calificador.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-126">Declare the flavors that describe a given qualifier after the qualifier name, between the qualifier brackets.</span></span> <span data-ttu-id="ba1f4-127">Use el espacio en blanco como delimitador entre varias versiones.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-127">Use white space as the delimiter between multiple flavors.</span></span>

    <span data-ttu-id="ba1f4-128">En el ejemplo siguiente se muestra el patrón para adjuntar calificadores predefinidos.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-128">The following example shows the pattern for attaching predefined qualifiers.</span></span>

    ``` syntax
    [qualifier1 : flavor1 flavor2 flavor3, qualifier2 : flavor1]
    ```

<span data-ttu-id="ba1f4-129">Puede agregar tipos de calificador mediante programación solo en C++.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-129">You can add qualifier flavors programmatically only in C++.</span></span> <span data-ttu-id="ba1f4-130">Esta operación no está disponible en la [API de scripting para WMI](scripting-api-for-wmi.md), aunque puede Agregar un nuevo calificador mediante una llamada a [**SWbemQualifierSet. Add**](swbemqualifierset-add.md).</span><span class="sxs-lookup"><span data-stu-id="ba1f4-130">This operation is not available in the [Scripting API for WMI](scripting-api-for-wmi.md), although you can add a new qualifier by calling [**SWbemQualifierSet.Add**](swbemqualifierset-add.md).</span></span>

<span data-ttu-id="ba1f4-131">**Para asignar un tipo mediante C++**</span><span class="sxs-lookup"><span data-stu-id="ba1f4-131">**To assign a flavor using C++**</span></span>

-   <span data-ttu-id="ba1f4-132">Llame al método [**IWbemQualifierSet::P UT**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) con el parámetro *lFlavor* establecido en una de las constantes definidas para el método.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-132">Call the [**IWbemQualifierSet::Put**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) method with the *lFlavor* parameter set to one of the constants defined for the method.</span></span>

 

 



