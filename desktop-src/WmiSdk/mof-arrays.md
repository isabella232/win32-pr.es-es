---
description: Una matriz es una lista indizada de valores de datos que son del mismo tipo de datos, a los que se puede hacer referencia. Además de las matrices numéricas y de cadena, MOF admite matrices de objetos incrustados y referencias.
ms.assetid: f63c222f-499d-4776-8901-65cb8b142d2b
ms.tgt_platform: multiple
title: Matrices MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0443f2ef3b3fe8fca398e281de71b0927a4f06f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275788"
---
# <a name="mof-arrays"></a><span data-ttu-id="68319-104">Matrices MOF</span><span class="sxs-lookup"><span data-stu-id="68319-104">MOF Arrays</span></span>

<span data-ttu-id="68319-105">Una matriz es una lista indizada de valores de datos que son del mismo tipo de datos, a los que se puede hacer referencia.</span><span class="sxs-lookup"><span data-stu-id="68319-105">An array is an indexed list of data values that are of the same data type, which you can reference.</span></span> <span data-ttu-id="68319-106">Además de las matrices numéricas y de cadena, MOF admite matrices de objetos incrustados y referencias.</span><span class="sxs-lookup"><span data-stu-id="68319-106">In addition to string and numeric arrays, MOF supports arrays of embedded objects and references.</span></span>

<span data-ttu-id="68319-107">Las siguientes reglas definen una matriz de MOF:</span><span class="sxs-lookup"><span data-stu-id="68319-107">The following rules define a MOF array:</span></span>

-   <span data-ttu-id="68319-108">Los corchetes usados después del identificador de propiedad especifican una matriz en una definición de clase.</span><span class="sxs-lookup"><span data-stu-id="68319-108">Brackets used after the property identifier specify an array in a class definition.</span></span>

    ``` syntax
    Class ArrayDataSample1
    {
        string strArray1[];
    };
    ```

-   <span data-ttu-id="68319-109">Todas las matrices deben ser unidimensionales.</span><span class="sxs-lookup"><span data-stu-id="68319-109">All arrays must be one-dimensional.</span></span>
-   <span data-ttu-id="68319-110">Las matrices pueden estar sin enlazar o tener un tamaño explícito.</span><span class="sxs-lookup"><span data-stu-id="68319-110">Arrays can be unbounded or have an explicit size.</span></span>

    ``` syntax
    Class MyClass
    {
        sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk DiskArray1[]);
        sint32 MyMethod2 ([in, id(0)] Win32_LogicalDisk DiskArray2[32]);
    };
    ```

    <span data-ttu-id="68319-111">WMI implementa matrices enlazadas y sin enlazar como estructuras **SAFEARRAY** , lo que permite que WMI varíe las dimensiones de la matriz en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="68319-111">WMI implements bounded and unbounded arrays as **SAFEARRAY** structures, which allows WMI to vary array dimensions at run time.</span></span> <span data-ttu-id="68319-112">Al declarar una matriz con un tamaño explícito, WMI almacena el tamaño como calificador y trata el tamaño como el tamaño máximo sugerido.</span><span class="sxs-lookup"><span data-stu-id="68319-112">When you declare an array with an explicit size, WMI stores the size as a qualifier, and treats the size as the suggested maximum size.</span></span> <span data-ttu-id="68319-113">Sin embargo, WMI puede expandir el tamaño si es necesario.</span><span class="sxs-lookup"><span data-stu-id="68319-113">However, WMI can expand the size if necessary.</span></span> <span data-ttu-id="68319-114">Cambiar el tamaño explícito no tiene ningún efecto en los datos reales.</span><span class="sxs-lookup"><span data-stu-id="68319-114">Changing the explicit size has no effect on the actual data.</span></span>

-   <span data-ttu-id="68319-115">Las matrices se inicializan especificando valores del tipo adecuado en una lista separada por comas.</span><span class="sxs-lookup"><span data-stu-id="68319-115">Arrays are initialized by specifying values of the appropriate type in a comma-separated list.</span></span>

    ``` syntax
    Class ArrayDataSample2
    {
        [key] string s;
        string strArray2[] = {"hello", "there"};
        sint32 dwArray[] = {1,2,3};
    };
    ```

-   <span data-ttu-id="68319-116">Una matriz de referencias se declara como una matriz de cadenas de ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="68319-116">An array of references is declared as an array of object path strings.</span></span>

    <span data-ttu-id="68319-117">Al declarar una cadena de ruta de acceso de objeto, no coloque espacios en blanco entre los elementos de la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="68319-117">When declaring an object path string, do not place white space between the elements of the object path.</span></span> <span data-ttu-id="68319-118">En el ejemplo siguiente se describe cómo declarar una referencia de ruta de acceso de objeto.</span><span class="sxs-lookup"><span data-stu-id="68319-118">The following example describes how to declare an object path reference.</span></span>

    ``` syntax
    Class ClassWithRefArray
        { 
        [key] string s; 
        object ref refArray[]; 
        };

    instance of ClassWithRefArray
        {
        s = 23;
        refArray = {"Disk.Name=\"C:\"", "Disk.Name=\"E:\""};
        };
    ```

-   <span data-ttu-id="68319-119">Puede usar una matriz como parámetro para un método, pero no como un valor devuelto para un parámetro de entrada o de entrada-salida.</span><span class="sxs-lookup"><span data-stu-id="68319-119">You can use an array as a parameter for a method, but not as a return value for an input or input-output parameter.</span></span>
-   <span data-ttu-id="68319-120">Todos los elementos de una matriz se crean como valores del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="68319-120">All elements in an array are created as values of the same type.</span></span>

    <span data-ttu-id="68319-121">Si los elementos de una matriz son del tipo de **objeto** , puede colocar cualquier tipo de objeto en la matriz.</span><span class="sxs-lookup"><span data-stu-id="68319-121">If the elements of an array are of the **object** type, then you can place any kind of object in the array.</span></span> <span data-ttu-id="68319-122">Por otro lado, si declara un tipo específico de objeto, WMI solo permite objetos de esa clase o subclase en la matriz.</span><span class="sxs-lookup"><span data-stu-id="68319-122">On the other hand, if you declare a specific type of object, then WMI allows only objects of that class or subclass in the array.</span></span> <span data-ttu-id="68319-123">En los ejemplos siguientes se muestran declaraciones de matriz que incluyen el uso del tipo de **objeto** .</span><span class="sxs-lookup"><span data-stu-id="68319-123">The following examples show array declarations that includes using the **object** type.</span></span>

    ``` syntax
    Class EmbedClass
    {
        [key] sint32 PropOfClass;
    };

    Class ArrayDataClass
    {
        [key] string s;
        string strArray1[];
        string strArray2[] = {"hello", "there"};
        sint32 dwArray[] = {1,2,3};
        EmbedClass objArray[];
    };

    instance of ArrayDataClass
    { 
        s = "keyStuff";
        strArray1 = { "1.2.3.4", "1.2.3.5", "1.2.3.7"};
        strArray2 = 
            {
                "SELECT * FROM RegistryKeyChangeEvent",
                "SELECT * FROM RegistryValueChangeEvent",
                "SELECT * FROM RegistryTreeChangeEvent"
            };
        dwArray  = { 1,2,3,5,6 };
        objArray = {
                       instance of EmbedClass{PropOfClass=3;},
                       instance of EmbedClass{PropOfClass=4;}
                   };
    };
    ```

 

 



