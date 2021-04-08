---
description: Al igual que muchas otras técnicas de Managed Object Format (MOF), la aplicación de un calificador al código es un proceso relativamente sencillo.
ms.assetid: aaa5c921-bdcd-40e6-ab4b-9441a1957e5b
ms.tgt_platform: multiple
title: Aplicar un calificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 042a3cdbf7236dc838735ce0cbf18a6315dd02e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819395"
---
# <a name="applying-a-qualifier"></a><span data-ttu-id="3cb36-103">Aplicar un calificador</span><span class="sxs-lookup"><span data-stu-id="3cb36-103">Applying a Qualifier</span></span>

<span data-ttu-id="3cb36-104">Al igual que muchas otras técnicas de Managed Object Format (MOF), la aplicación de un calificador al código es un proceso relativamente sencillo.</span><span class="sxs-lookup"><span data-stu-id="3cb36-104">Like many other techniques in Managed Object Format (MOF), applying a qualifier to your code is a relatively simple process.</span></span>

<span data-ttu-id="3cb36-105">Los únicos desafíos reales son las siguientes restricciones en las convenciones de nomenclatura que aplica WMI:</span><span class="sxs-lookup"><span data-stu-id="3cb36-105">The only real challenges are the following restrictions in naming conventions that WMI enforces:</span></span>

-   <span data-ttu-id="3cb36-106">Un calificador puede describir una clase, una instancia, una propiedad, un método o un parámetro de método.</span><span class="sxs-lookup"><span data-stu-id="3cb36-106">A qualifier can describe a class, instance, property, method, or method parameter.</span></span>
-   <span data-ttu-id="3cb36-107">Los nombres de calificador no pueden tener un carácter de subrayado inicial ni final.</span><span class="sxs-lookup"><span data-stu-id="3cb36-107">Qualifier names cannot have either leading or trailing underscores.</span></span>
-   <span data-ttu-id="3cb36-108">Un nombre de calificador no puede comenzar con un dígito.</span><span class="sxs-lookup"><span data-stu-id="3cb36-108">A qualifier name cannot begin with a digit.</span></span>
-   <span data-ttu-id="3cb36-109">Un nombre de calificador no puede contener caracteres especiales como & \* @!</span><span class="sxs-lookup"><span data-stu-id="3cb36-109">A qualifier name cannot contain special characters such as & \* @ !</span></span><span data-ttu-id="3cb36-110"> ~ \\ /.</span><span class="sxs-lookup"><span data-stu-id="3cb36-110"> ~ \\ /.</span></span>
-   <span data-ttu-id="3cb36-111">Todos los nombres de calificador distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3cb36-111">All qualifier names are case-insensitive.</span></span>
-   <span data-ttu-id="3cb36-112">No se pueden volver a definir los calificadores WMI estándar ni los calificadores descritos en la especificación CIM de DMTF.</span><span class="sxs-lookup"><span data-stu-id="3cb36-112">You cannot redefine the standard WMI qualifiers or any qualifiers described in the DMTF CIM specification.</span></span>
-   <span data-ttu-id="3cb36-113">Los tipos de calificador no se declaran explícitamente.</span><span class="sxs-lookup"><span data-stu-id="3cb36-113">Qualifier types are not explicitly declared.</span></span>

    <span data-ttu-id="3cb36-114">Si no declara un tipo de calificador, WMI supone que el tipo es booleano con un valor de **true**.</span><span class="sxs-lookup"><span data-stu-id="3cb36-114">If you do not declare a qualifier type, WMI assumes the type as Boolean with a value of **TRUE**.</span></span> <span data-ttu-id="3cb36-115">De lo contrario, WMI escribe los calificadores basados en los valores de calificador que se declaran.</span><span class="sxs-lookup"><span data-stu-id="3cb36-115">Otherwise, WMI types qualifiers based on the qualifier values you declare.</span></span>

-   <span data-ttu-id="3cb36-116">Al crear sus propios calificadores, debe anteponer el nombre del esquema al nombre del calificador.</span><span class="sxs-lookup"><span data-stu-id="3cb36-116">When creating your own qualifiers, you should prefix your schema name to your qualifier name.</span></span>

    <span data-ttu-id="3cb36-117">El objetivo de esta regla es evitar la confusión con los nuevos calificadores.</span><span class="sxs-lookup"><span data-stu-id="3cb36-117">The purpose of this rule is to avoid confusion with new qualifiers.</span></span>

-   <span data-ttu-id="3cb36-118">Puede crear matrices homogéneas de calificadores.</span><span class="sxs-lookup"><span data-stu-id="3cb36-118">You can create homogeneous arrays of qualifiers.</span></span>

    <span data-ttu-id="3cb36-119">En el ejemplo de código siguiente se muestra cómo se especifican las matrices de calificador con llaves que rodean los valores.</span><span class="sxs-lookup"><span data-stu-id="3cb36-119">The following code example shows how qualifier arrays are specified with curly braces that surround the values.</span></span>

    ``` syntax
    [StringArray{"hello", "there"}, SingleElementArray{3}]
    ```

-   <span data-ttu-id="3cb36-120">WMI no admite los tipos de automatización que no se enumeran en la referencia, como VT \_ null.</span><span class="sxs-lookup"><span data-stu-id="3cb36-120">WMI does not support automation types not listed in the reference, such as VT\_NULL.</span></span> <span data-ttu-id="3cb36-121">Para obtener más información, vea [tipos de datos MOF](mof-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="3cb36-121">For more information, see [MOF Data Types](mof-data-types.md).</span></span>

<span data-ttu-id="3cb36-122">El siguiente procedimiento le ayudará a usar C++ para agregar un calificador a una propiedad.</span><span class="sxs-lookup"><span data-stu-id="3cb36-122">The following procedure helps you to use C++ to add a qualifier to a property.</span></span>

<span data-ttu-id="3cb36-123">**Para aplicar un calificador mediante C++**</span><span class="sxs-lookup"><span data-stu-id="3cb36-123">**To apply a qualifier using C++**</span></span>

-   <span data-ttu-id="3cb36-124">Aplique el calificador con una llamada al método [**IWbemQualifierSet::P UT**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) .</span><span class="sxs-lookup"><span data-stu-id="3cb36-124">Apply the qualifier with a call to the [**IWbemQualifierSet::Put**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) method.</span></span>

    <span data-ttu-id="3cb36-125">Puede usar otros métodos de [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) para recuperar o eliminar calificadores existentes.</span><span class="sxs-lookup"><span data-stu-id="3cb36-125">You can use other methods of [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) to retrieve or delete existing qualifiers.</span></span>

<span data-ttu-id="3cb36-126">El siguiente procedimiento le ayuda a aplicar un calificador en archivos MOF.</span><span class="sxs-lookup"><span data-stu-id="3cb36-126">The following procedure helps you to apply a qualifier in MOF files.</span></span>

<span data-ttu-id="3cb36-127">**Para describir una palabra clave o un identificador con un calificador mediante MOF**</span><span class="sxs-lookup"><span data-stu-id="3cb36-127">**To describe a keyword or identifier with a qualifier using MOF**</span></span>

-   <span data-ttu-id="3cb36-128">Coloque un calificador entre corchetes antes de la palabra clave o el identificador descrito por el calificador.</span><span class="sxs-lookup"><span data-stu-id="3cb36-128">Place a qualifier in brackets before the keyword or identifier described by the qualifier.</span></span>

    <span data-ttu-id="3cb36-129">En el ejemplo de código siguiente se muestra cómo se usan los calificadores.</span><span class="sxs-lookup"><span data-stu-id="3cb36-129">The following code example shows how qualifiers are used.</span></span>

    ``` syntax
    [qualifiers...]
    class StdDisk
    {
      [qualifiers...]  uint32 dwNumCylinders;
      [qualifiers...]  uint32 dwNumHeads;
      [qualifiers...]  sint32 Method1();
      sint32 Method2([qualifiers...] Parameter1);
    };
    ```

    <span data-ttu-id="3cb36-130">En el siguiente ejemplo se describe la colocación adecuada de los calificadores.</span><span class="sxs-lookup"><span data-stu-id="3cb36-130">The following example describes the proper placement of qualifiers.</span></span>

    ``` syntax
    [Abstract]
    class MyClass
    {
        [Amendment, InstanceOf]  uint32 dwNumber;
        sint32 MyMethod ([in] sint32 Param);
    };
    ```

 

 



