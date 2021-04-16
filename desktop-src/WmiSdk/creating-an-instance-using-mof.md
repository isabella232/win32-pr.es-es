---
description: Puede declarar una instancia básica de una clase en el servicio de administración de Windows mediante Managed Object Format (MOF). También puede invalidar los valores predeterminados para una instancia de. Para obtener más información, vea establecer un valor de propiedad de instancia.
ms.assetid: 12eda062-9614-455d-ae99-7706c685137b
ms.tgt_platform: multiple
title: Crear una instancia mediante MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5078c5fcddaab4e8437a33e8cb3210d515360fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706173"
---
# <a name="creating-an-instance-using-mof"></a><span data-ttu-id="e5e27-105">Crear una instancia mediante MOF</span><span class="sxs-lookup"><span data-stu-id="e5e27-105">Creating an Instance Using MOF</span></span>

<span data-ttu-id="e5e27-106">Puede declarar una instancia básica de una clase en el servicio de administración de Windows mediante Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="e5e27-106">You can declare a basic instance of a class in the Windows Management service using Managed Object Format (MOF).</span></span> <span data-ttu-id="e5e27-107">También puede invalidar los valores predeterminados para una instancia de.</span><span class="sxs-lookup"><span data-stu-id="e5e27-107">You can also override the default values for an instance.</span></span> <span data-ttu-id="e5e27-108">Para obtener más información, vea [establecer un valor de propiedad de instancia](#setting-an-instance-property-value).</span><span class="sxs-lookup"><span data-stu-id="e5e27-108">For more information, see [Setting an Instance Property Value](#setting-an-instance-property-value).</span></span>

<span data-ttu-id="e5e27-109">En el procedimiento siguiente se describe cómo declarar una instancia básica de una clase mediante código MOF.</span><span class="sxs-lookup"><span data-stu-id="e5e27-109">The following procedure describes how to declare a basic instance of a class using MOF code.</span></span>

<span data-ttu-id="e5e27-110">**Para declarar una instancia básica de una clase mediante código MOF**</span><span class="sxs-lookup"><span data-stu-id="e5e27-110">**To declare a basic instance of a class using MOF code**</span></span>

1.  <span data-ttu-id="e5e27-111">Use la **instancia de** Keywords seguida del nombre de clase, llaves y un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="e5e27-111">Use the **Instance of** keywords followed by the class name, curly braces, and a semicolon.</span></span>

    <span data-ttu-id="e5e27-112">En el ejemplo de código siguiente se muestra cómo declarar una instancia de una clase.</span><span class="sxs-lookup"><span data-stu-id="e5e27-112">The following code example shows how to declare an instance of a class.</span></span>

    ```mof
    instance of ClassName
    {
    };
    ```

    

2.  <span data-ttu-id="e5e27-113">Cuando termine, inserte el código MOF en el repositorio WMI mediante el compilador MOF.</span><span class="sxs-lookup"><span data-stu-id="e5e27-113">When finished, insert your MOF code into the WMI repository using the MOF compiler.</span></span>

    <span data-ttu-id="e5e27-114">Para obtener más información, vea [compilar archivos MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="e5e27-114">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="e5e27-115">Una instancia de una clase incluye todas las propiedades de la clase.</span><span class="sxs-lookup"><span data-stu-id="e5e27-115">An instance of a class includes all of the properties of the class.</span></span> <span data-ttu-id="e5e27-116">Si la clase es una clase derivada, las instancias de incluyen las propiedades que pertenecen a todas las clases que se encuentran en una posición superior en la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="e5e27-116">If the class is a derived class, instances include the properties belonging to all of the classes higher in the hierarchy.</span></span> <span data-ttu-id="e5e27-117">Cada clase de la que se crea una instancia tiene una o más propiedades de clave.</span><span class="sxs-lookup"><span data-stu-id="e5e27-117">Each class that an instance is created from has one or more key properties.</span></span> <span data-ttu-id="e5e27-118">No se puede crear una instancia de con más de 256 claves.</span><span class="sxs-lookup"><span data-stu-id="e5e27-118">You cannot create an instance with more than 256 keys.</span></span>

## <a name="setting-an-instance-property-value"></a><span data-ttu-id="e5e27-119">Establecer un valor de propiedad de instancia</span><span class="sxs-lookup"><span data-stu-id="e5e27-119">Setting an Instance Property Value</span></span>

<span data-ttu-id="e5e27-120">Dado que las propiedades de los tipos fuertemente de WMI, no se pueden modificar los tipos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e5e27-120">Because WMI strongly types properties, you cannot modify property types.</span></span> <span data-ttu-id="e5e27-121">Sin embargo, puede establecer valores de propiedad en instancias de.</span><span class="sxs-lookup"><span data-stu-id="e5e27-121">You can, however, set property values in instances.</span></span> <span data-ttu-id="e5e27-122">Cuando una clase asigna un valor predeterminado a una propiedad, WMI asigna el valor predeterminado a cada instancia.</span><span class="sxs-lookup"><span data-stu-id="e5e27-122">When a class assigns a default value to a property, WMI assigns the default value to each instance.</span></span> <span data-ttu-id="e5e27-123">Puede invalidar este valor en la declaración de instancia.</span><span class="sxs-lookup"><span data-stu-id="e5e27-123">You can override this value in your instance declaration.</span></span>

<span data-ttu-id="e5e27-124">En el procedimiento siguiente se describe cómo establecer un valor de propiedad o sobrescribir un valor predeterminado mediante código MOF.</span><span class="sxs-lookup"><span data-stu-id="e5e27-124">The following procedure describes how to set a property value or overwrite a default value using MOF code.</span></span>

<span data-ttu-id="e5e27-125">**Para establecer un valor de propiedad o sobrescribir un valor predeterminado mediante código MOF**</span><span class="sxs-lookup"><span data-stu-id="e5e27-125">**To set a property value or overwrite a default value using MOF code**</span></span>

1.  <span data-ttu-id="e5e27-126">Coloque una instrucción de asignación entre las llaves de la declaración de instancia.</span><span class="sxs-lookup"><span data-stu-id="e5e27-126">Place an assignment statement between the curly braces of the instance declaration.</span></span>

    <span data-ttu-id="e5e27-127">En el ejemplo de código siguiente se muestra cómo establecer un valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e5e27-127">The following code example shows how to set a property value.</span></span>

    ``` syntax
    instance of ClassName
    {
        Prop = "value";
    };
    ```

    <span data-ttu-id="e5e27-128">WMI no requiere que se establezca ninguna propiedad durante la creación de la instancia.</span><span class="sxs-lookup"><span data-stu-id="e5e27-128">WMI does not require that you set any property during instance creation.</span></span> <span data-ttu-id="e5e27-129">La excepción es cualquier propiedad marcada con el calificador de [**clave**](key-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="e5e27-129">The exception is any property marked with the [**Key**](key-qualifier.md) qualifier.</span></span> <span data-ttu-id="e5e27-130">Dado que WMI utiliza propiedades de clave para identificar de forma única las instancias, debe establecer todas las propiedades clave a medida que se encuentren.</span><span class="sxs-lookup"><span data-stu-id="e5e27-130">Because WMI uses key properties to uniquely identify instances, you must set all key properties as you encounter them.</span></span> <span data-ttu-id="e5e27-131">Por el contrario, no debe establecer una propiedad del sistema en una declaración de instancia.</span><span class="sxs-lookup"><span data-stu-id="e5e27-131">In contrast, you must not set a system property in an instance declaration.</span></span> <span data-ttu-id="e5e27-132">En su lugar, WMI asigna los valores adecuados a una propiedad del sistema cuando es necesario.</span><span class="sxs-lookup"><span data-stu-id="e5e27-132">Instead, WMI assigns the appropriate values to a system property when necessary.</span></span>

2.  <span data-ttu-id="e5e27-133">Cuando termine, inserte el código MOF en el repositorio WMI con una llamada al compilador MOF.</span><span class="sxs-lookup"><span data-stu-id="e5e27-133">When finished, insert your MOF code into the WMI repository with a call to the MOF compiler.</span></span>

    <span data-ttu-id="e5e27-134">Para obtener más información, vea [compilar archivos MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="e5e27-134">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="e5e27-135">En los ejemplos de código siguientes se muestra cómo una instancia de especifica los datos para las propiedades definidas por una clase.</span><span class="sxs-lookup"><span data-stu-id="e5e27-135">The following code examples show how an instance specifies data for properties defined by a class.</span></span>

``` syntax
class MyClass 
{
    [key] string   strProp;
    sint32   dwProp1;
    uint32       dwProp2;
};

instance of MyClass 
{
    strProp = "hello";
    dwProp1 = -1;
    dwProp2 = 0xffffffff;
};
```

<span data-ttu-id="e5e27-136">En el ejemplo anterior, la clase define tres propiedades: una cadena de caracteres, un entero con signo de 32 bits y un entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="e5e27-136">In the preceding example, the class defines three properties: a character string, a 32-bit signed integer, and a 32-bit unsigned integer.</span></span> <span data-ttu-id="e5e27-137">La instancia de proporciona valores de datos para cada una de estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e5e27-137">The instance provides data values for each of these properties.</span></span>

 

 



