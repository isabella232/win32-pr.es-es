---
description: Una clase de asociación es un tipo especial de clase que define una relación entre otras dos clases.
ms.assetid: 21fd6e39-5dd3-41b8-a2f5-0135a6637ce8
ms.tgt_platform: multiple
title: Declarar una clase de asociación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083ce578ca912290fd026f225799793f89685aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083138"
---
# <a name="declaring-an-association-class"></a><span data-ttu-id="ed82c-103">Declarar una clase de asociación</span><span class="sxs-lookup"><span data-stu-id="ed82c-103">Declaring an Association Class</span></span>

<span data-ttu-id="ed82c-104">Una clase de asociación es un tipo especial de clase que define una relación entre otras dos clases.</span><span class="sxs-lookup"><span data-stu-id="ed82c-104">An association class is a special type of class that defines a relationship between two other classes.</span></span>

<span data-ttu-id="ed82c-105">En el procedimiento siguiente se describe cómo crear una clase de asociación mediante código MOF.</span><span class="sxs-lookup"><span data-stu-id="ed82c-105">The following procedure describes how to create an association class using MOF code.</span></span>

<span data-ttu-id="ed82c-106">**Para crear una clase de asociación mediante código MOF**</span><span class="sxs-lookup"><span data-stu-id="ed82c-106">**To create an association class using MOF code**</span></span>

1.  <span data-ttu-id="ed82c-107">Asigne el calificador de **Asociación** a la clase.</span><span class="sxs-lookup"><span data-stu-id="ed82c-107">Assign the **Association** qualifier to your class.</span></span>

    <span data-ttu-id="ed82c-108">Aunque es posible crear una clase con referencias a objetos o clases, el uso del calificador de **Asociación** no solo hace evidente que la clase es una clase de asociación, pero, como procedimiento recomendado, garantiza que la clase funcionará completamente como una clase de asociación.</span><span class="sxs-lookup"><span data-stu-id="ed82c-108">Although it is possible to create a class with references to objects or classes, using the **Association** qualifier not only makes it clear that your class is an association class, but, as a best practice, ensures that your class fully functions as an association class.</span></span>

2.  <span data-ttu-id="ed82c-109">Cree dos referencias en la clase que describen las dos instancias de objeto que desea asociar con el tipo de **referencia** .</span><span class="sxs-lookup"><span data-stu-id="ed82c-109">Create two references within the class describing the two object instances you wish to associate together using the **ref** type.</span></span>

    <span data-ttu-id="ed82c-110">Las referencias enlazan los dos objetos de la asociación mediante el contenedor de rutas de acceso a los objetos.</span><span class="sxs-lookup"><span data-stu-id="ed82c-110">The references bind the two objects in the association by containing paths to the objects.</span></span> <span data-ttu-id="ed82c-111">Aunque no es necesario, utilice también las propiedades de referencia como propiedades clave.</span><span class="sxs-lookup"><span data-stu-id="ed82c-111">Although not required, use the reference properties as key properties as well.</span></span>

    <span data-ttu-id="ed82c-112">Aunque puede crear referencias completas o relativas al espacio de nombres, WMI solo tiene compatibilidad limitada para las referencias entre espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="ed82c-112">Although you can create fully qualified or namespace-relative references, WMI has only limited support for cross-namespace references.</span></span> <span data-ttu-id="ed82c-113">En concreto, solo los objetos definidos estáticamente pueden hacer referencia entre sí a través de los límites del espacio de nombres; los objetos admitidos dinámicamente no pueden hacer referencia entre sí.</span><span class="sxs-lookup"><span data-stu-id="ed82c-113">Specifically, only statically defined objects can reference each other across namespace boundaries; dynamically supported objects cannot reference each other.</span></span>

    <span data-ttu-id="ed82c-114">Si es necesario, use los calificadores **HasClassRef** y **Classref** junto con el tipo **ref del objeto** para hacer referencia a una clase.</span><span class="sxs-lookup"><span data-stu-id="ed82c-114">If necessary, use the **HasClassRef** and **Classref** qualifiers in conjunction with the **object ref** type to reference a class.</span></span>

    <span data-ttu-id="ed82c-115">WMI admite tener un punto **de referencia de referencia a** una instancia de y la otra referencia de **objeto** apunta a una clase.</span><span class="sxs-lookup"><span data-stu-id="ed82c-115">WMI supports having one **ref** reference point to an instance, and the other **object** reference point to a class.</span></span> <span data-ttu-id="ed82c-116">En este caso, la clase de asociación describiría una asociación que enlaza instancias a clases.</span><span class="sxs-lookup"><span data-stu-id="ed82c-116">In this case, your association class would describe an association that binds instances to classes.</span></span>

    <span data-ttu-id="ed82c-117">En el ejemplo de código siguiente se describe la sintaxis para usar **HasClassRef** y **Classref** con un tipo de **objeto** .</span><span class="sxs-lookup"><span data-stu-id="ed82c-117">The following code example describes the syntax for using **HasClassRef** and **Classref** with an **object** type.</span></span>

    ``` syntax
    [HasClassRefs, Association]
    class SomeAssocClass
    {
         [key, classref{ "MyEndpoint", "OtherContainer" }]
         object ref ep1;
         [key] object ref ep2;
    }; 
    ```

    <span data-ttu-id="ed82c-118">En el ejemplo anterior, la referencia de **EP1** puede apuntar a las definiciones de clase **para la clase** OtherContainer o la clase  .</span><span class="sxs-lookup"><span data-stu-id="ed82c-118">In the previous example, the **ep1** reference can point to the class definitions for either the **MyEndpoint** class or the **OtherContainer** class.</span></span> <span data-ttu-id="ed82c-119">Tenga en cuenta que, aunque debe escribir la clase de referencia de un tipo débil, no se puede escribir el calificador **Classref** en sí. al hacerlo, se reduciría seriamente la eficacia del motor de consultas de WMI.</span><span class="sxs-lookup"><span data-stu-id="ed82c-119">Note that while you must weakly type the reference class, you cannot weakly type the **Classref** qualifier itself; doing so would severely reduce the efficiency of the WMI query engine.</span></span> <span data-ttu-id="ed82c-120">La escritura débil es crear una referencia que puede contener cualquier tipo de datos mediante la palabra clave de **objeto** y el tipo de datos **ref** .</span><span class="sxs-lookup"><span data-stu-id="ed82c-120">Weak typing is creating a reference that can contain any data type by using the **object** keyword and **ref** data type.</span></span> <span data-ttu-id="ed82c-121">Para usar correctamente **HasClassRef**, debe establecer los tipos de calificador pertinentes para propagarse a todas las instancias y subclases.</span><span class="sxs-lookup"><span data-stu-id="ed82c-121">To successfully use **HasClassRef**, you must set the relevant qualifier flavors to propagate to all instances and subclasses.</span></span>

3.  <span data-ttu-id="ed82c-122">Cree otras propiedades según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="ed82c-122">Create any other properties as necessary.</span></span>

    <span data-ttu-id="ed82c-123">En el ejemplo de código siguiente se muestra que WMI no admite actualmente clases de asociación que tengan menos o más de dos propiedades de referencia.</span><span class="sxs-lookup"><span data-stu-id="ed82c-123">The following code example shows that WMI does not currently support association classes having less or more than two reference properties.</span></span>

    ``` syntax
    [Association : ToInstance] 
    class MyAssocClass
    {
        ClassX ref PathToClassX ;
        ClassY ref PathToClassY ;
    };
    ```

4.  <span data-ttu-id="ed82c-124">Cuando termine, compile el código MOF con el compilador MOF.</span><span class="sxs-lookup"><span data-stu-id="ed82c-124">When finished, compile your MOF code with the MOF compiler.</span></span>

    <span data-ttu-id="ed82c-125">Para obtener más información, vea [compilar archivos MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="ed82c-125">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="ed82c-126">En el ejemplo de código del paso 3 se define la clase de asociación **MyAssocClass** .</span><span class="sxs-lookup"><span data-stu-id="ed82c-126">The code example in Step 3 defines the **MyAssocClass** association class.</span></span> <span data-ttu-id="ed82c-127">La clase **MyAssocClass** define una relación entre **ClassX** y **Classy**.</span><span class="sxs-lookup"><span data-stu-id="ed82c-127">The **MyAssocClass** class defines a relationship between **ClassX** and **ClassY**.</span></span> <span data-ttu-id="ed82c-128">Las propiedades **PathToClassX** y **PathToClassY** contienen rutas de acceso de objeto a las instancias de las clases que se van a asociar.</span><span class="sxs-lookup"><span data-stu-id="ed82c-128">The **PathToClassX** and **PathToClassY** properties contain object paths to the instances of the classes to be associated.</span></span> <span data-ttu-id="ed82c-129">La palabra clave **ToInstance** es una de las diversas marcas de sabor que define WMI para proporcionar información sobre el uso de un calificador.</span><span class="sxs-lookup"><span data-stu-id="ed82c-129">The keyword **ToInstance** is one of several flavor flags that WMI defines to provide information about the use of a qualifier.</span></span> <span data-ttu-id="ed82c-130">La palabra clave **ToInstance** indica que WMI debe propagar el calificador de **Asociación** a todas las instancias de la clase Association.</span><span class="sxs-lookup"><span data-stu-id="ed82c-130">The **ToInstance** keyword indicates that WMI should propagate the **Association** qualifier to all instances of the association class.</span></span> <span data-ttu-id="ed82c-131">Al activar este calificador de instancia, el software cliente puede determinar que una instancia pertenece a una clase de asociación, sin tener que recuperar la definición de clase para buscar el calificador de **Asociación** .</span><span class="sxs-lookup"><span data-stu-id="ed82c-131">By checking this instance qualifier, the client software can determine that an instance belongs to an association class, without having to retrieve the class definition to look for the **Association** qualifier.</span></span> <span data-ttu-id="ed82c-132">Para obtener más información, vea [Descripción de un calificador con un tipo de calificador](describing-a-qualifier-with-a-qualifier-flavor.md) y [referencias](references.md).</span><span class="sxs-lookup"><span data-stu-id="ed82c-132">For more information, see [Describing a Qualifier With a Qualifier Flavor](describing-a-qualifier-with-a-qualifier-flavor.md) and [References](references.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed82c-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ed82c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed82c-134">Diseñar clases de Managed Object Format (MOF)</span><span class="sxs-lookup"><span data-stu-id="ed82c-134">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



