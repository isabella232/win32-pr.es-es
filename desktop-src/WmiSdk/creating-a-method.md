---
description: Para crear un método WMI, defina los parámetros de entrada y salida para el método.
ms.assetid: 71cbecde-33c4-4bf1-9793-bef6d823dcac
ms.tgt_platform: multiple
title: Crear un método WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2489a5dd4e97ed6c8d26eeb292c45fa66901cbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278771"
---
# <a name="creating-a-wmi-method"></a><span data-ttu-id="f167f-103">Crear un método WMI</span><span class="sxs-lookup"><span data-stu-id="f167f-103">Creating a WMI Method</span></span>

<span data-ttu-id="f167f-104">Para crear un método WMI, defina los parámetros de entrada y salida para el método.</span><span class="sxs-lookup"><span data-stu-id="f167f-104">To create a WMI method, define the input and output parameters for the method.</span></span> <span data-ttu-id="f167f-105">Los parámetros de entrada y salida se representan mediante [**\_ \_ parámetros**](--parameters.md)de clase del sistema WMI especiales.</span><span class="sxs-lookup"><span data-stu-id="f167f-105">The input and output parameters are represented by a special WMI system class [**\_\_PARAMETERS**](--parameters.md).</span></span> <span data-ttu-id="f167f-106">Para obtener más información, vea [llamar a un método](calling-a-method.md) y [escribir un proveedor de métodos](writing-a-method-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f167f-106">For more information, see [Calling a Method](calling-a-method.md) and [Writing a Method Provider](writing-a-method-provider.md).</span></span>

<span data-ttu-id="f167f-107">En este tema se describen las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="f167f-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="f167f-108">Crear un método de clase WMI en MOF</span><span class="sxs-lookup"><span data-stu-id="f167f-108">Creating a WMI Class Method in MOF</span></span>](#creating-a-wmi-class-method-in-mof)
-   [<span data-ttu-id="f167f-109">Crear un método de clase WMI en C++</span><span class="sxs-lookup"><span data-stu-id="f167f-109">Creating a WMI Class Method in C++</span></span>](#creating-a-wmi-class-method-in-c)
-   [<span data-ttu-id="f167f-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f167f-110">Related topics</span></span>](#related-topics)

## <a name="creating-a-wmi-class-method-in-mof"></a><span data-ttu-id="f167f-111">Crear un método de clase WMI en MOF</span><span class="sxs-lookup"><span data-stu-id="f167f-111">Creating a WMI Class Method in MOF</span></span>

<span data-ttu-id="f167f-112">En WMI, los métodos de proveedor suelen ser acciones diferentes relacionadas con el objeto que la clase representa.</span><span class="sxs-lookup"><span data-stu-id="f167f-112">In WMI, provider methods are generally distinct actions related to the object that the class represents.</span></span> <span data-ttu-id="f167f-113">En lugar de cambiar el valor de una propiedad para ejecutar una acción, se debe crear un método.</span><span class="sxs-lookup"><span data-stu-id="f167f-113">Rather than change the value of a property to execute an action, a method should be created.</span></span> <span data-ttu-id="f167f-114">Por ejemplo, puede habilitar o deshabilitar un centro de información de red (NIC) representado por [**Win32 \_ adaptador**](/windows/desktop/CIMWin32Prov/win32-networkadapter) de red mediante los métodos [**enable**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter) y [**Disable**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter) .</span><span class="sxs-lookup"><span data-stu-id="f167f-114">For example, you can enable or disable a network information center (NIC) that is represented by [**Win32\_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) by using the [**Enable**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter) and [**Disable**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter) methods.</span></span> <span data-ttu-id="f167f-115">Aunque estas acciones se pueden representar como una propiedad de lectura y escritura, el diseño recomendado es crear un método.</span><span class="sxs-lookup"><span data-stu-id="f167f-115">While these actions can be represented as a read/write property, the recommended design is to create a method.</span></span> <span data-ttu-id="f167f-116">Como alternativa, si desea que un estado o valor esté visible para la clase, el enfoque recomendado es crear una propiedad de lectura/escritura en lugar de un método.</span><span class="sxs-lookup"><span data-stu-id="f167f-116">Alternatively, if you want to make a state or value visible for the class, then the recommended approach is to create a read/write property rather than a method.</span></span> <span data-ttu-id="f167f-117">En el adaptador de **Win32 \_**, la propiedad **NetEnabled** hace que el estado del adaptador sea visible pero los métodos **enable** o **Disable** ejecutan los cambios entre Estados.</span><span class="sxs-lookup"><span data-stu-id="f167f-117">In **Win32\_NetworkAdapter**, the **NetEnabled** property makes the state of the adapter visible but changes between states are executed by the **Enable** or **Disable** methods.</span></span>

<span data-ttu-id="f167f-118">Las declaraciones de clase pueden incluir la declaración de uno o más métodos.</span><span class="sxs-lookup"><span data-stu-id="f167f-118">Class declarations can include the declaration of one or more methods.</span></span> <span data-ttu-id="f167f-119">Puede optar por heredar los métodos de una clase primaria o implementar el suyo propio.</span><span class="sxs-lookup"><span data-stu-id="f167f-119">You can either choose to inherit the methods of a parent class, or implement your own.</span></span> <span data-ttu-id="f167f-120">Si decide implementar sus propios métodos, debe declarar el método y marcar el método con etiquetas de calificador específicas.</span><span class="sxs-lookup"><span data-stu-id="f167f-120">If you choose to implement your own methods, you must declare the method and mark the method with specific qualifier tags.</span></span>

<span data-ttu-id="f167f-121">En el procedimiento siguiente se describe cómo declarar un método en una clase que no se hereda de una clase base.</span><span class="sxs-lookup"><span data-stu-id="f167f-121">The following procedure describes how to declare a method in a class that does not inherit from a base class.</span></span>

<span data-ttu-id="f167f-122">**Para declarar un método**</span><span class="sxs-lookup"><span data-stu-id="f167f-122">**To declare a method**</span></span>

1.  <span data-ttu-id="f167f-123">Defina el nombre del método entre las llaves de una declaración de clase, seguidos de los calificadores.</span><span class="sxs-lookup"><span data-stu-id="f167f-123">Define the name of your method between the curly braces of a class declaration, followed by any qualifiers.</span></span>

    <span data-ttu-id="f167f-124">En el ejemplo de código siguiente se describe la sintaxis de un método.</span><span class="sxs-lookup"><span data-stu-id="f167f-124">The following code example describes the syntax for a method.</span></span>

    ``` syntax
    [Dynamic, Provider ("ProviderName")]
    class ClassName
    {
        [Implemented] <ReturnType> <MethodName>
            ([ParameterDirection, IDQualifier] 
            <ParameterType> <ParameterName>);
    };
    ```

2.  <span data-ttu-id="f167f-125">Cuando termine, inserte el código de Managed Object Format (MOF) en el repositorio WMI con una llamada al compilador MOF.</span><span class="sxs-lookup"><span data-stu-id="f167f-125">When finished, insert your Managed Object Format (MOF) code into the WMI repository with a call to the MOF compiler.</span></span>

    <span data-ttu-id="f167f-126">Para obtener más información, vea [compilar archivos MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="f167f-126">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="f167f-127">La lista siguiente define los elementos de la declaración del método.</span><span class="sxs-lookup"><span data-stu-id="f167f-127">The following list defines the elements of the method declaration.</span></span>

<dl> <dt>

<span data-ttu-id="f167f-128"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>[**Presta**](/windows/desktop/api/Provider/nl-provider-provider)</span><span class="sxs-lookup"><span data-stu-id="f167f-128"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>[**Provider**](/windows/desktop/api/Provider/nl-provider-provider)</span></span>
</dt> <dd>

<span data-ttu-id="f167f-129">Vincula un proveedor específico a la descripción de la clase.</span><span class="sxs-lookup"><span data-stu-id="f167f-129">Links a specific provider to your class description.</span></span> <span data-ttu-id="f167f-130">El valor del calificador de [**proveedor**](/windows/desktop/api/Provider/nl-provider-provider) es el nombre del proveedor, que indica a WMI dónde reside el código que admite el método.</span><span class="sxs-lookup"><span data-stu-id="f167f-130">The value of the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier is the name of the provider, which tells WMI where the code that supports your method resides.</span></span> <span data-ttu-id="f167f-131">Un proveedor también debe marcar con el calificador **dinámico** cualquier clase que tenga instancias dinámicas.</span><span class="sxs-lookup"><span data-stu-id="f167f-131">A provider should also mark with the **Dynamic** qualifier any class that has dynamic instances.</span></span> <span data-ttu-id="f167f-132">Por el contrario, no utilice el calificador **dinámico** para marcar una clase que contenga una instancia estática con métodos **implementados** .</span><span class="sxs-lookup"><span data-stu-id="f167f-132">In contrast, do not use the **Dynamic** qualifier to mark a class that contains a static instance with **Implemented** methods.</span></span>

</dd> <dt>

<span data-ttu-id="f167f-133"><span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Ha**</span><span class="sxs-lookup"><span data-stu-id="f167f-133"><span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Implemented**</span></span>
</dt> <dd>

<span data-ttu-id="f167f-134">Declara que va a implementar un método, en lugar de heredar la implementación del método de la clase primaria.</span><span class="sxs-lookup"><span data-stu-id="f167f-134">Declares that you will implement a method, rather than inherit the method implementation from the parent class.</span></span> <span data-ttu-id="f167f-135">De forma predeterminada, WMI propaga la implementación de la clase primaria a una clase derivada a menos que la clase derivada proporcione una implementación de.</span><span class="sxs-lookup"><span data-stu-id="f167f-135">By default, WMI propagates the implementation of the parent class to a derived class unless the derived class provides an implementation.</span></span> <span data-ttu-id="f167f-136">Al omitir el calificador **implementado** , se indica que el método no tiene ninguna implementación en esa clase.</span><span class="sxs-lookup"><span data-stu-id="f167f-136">Omitting the **Implemented** qualifier indicates that the method has no implementation in that class.</span></span> <span data-ttu-id="f167f-137">Si vuelve a declarar un método sin el calificador **implementado** , WMI sigue suponiendo que no va a implementar ese método e invoca la implementación del método de clase primaria cuando se llama.</span><span class="sxs-lookup"><span data-stu-id="f167f-137">If you redeclare a method without the **Implemented** qualifier, WMI still assumes that you are not going to implement that method, and invokes the parent class method implementation when called.</span></span> <span data-ttu-id="f167f-138">Como tal, la Redeclaración de un método en una clase derivada sin adjuntar el calificador **implementado** solo es útil cuando se agrega o quita un calificador en el método o desde él.</span><span class="sxs-lookup"><span data-stu-id="f167f-138">As such, redeclaring a method in a derived class without attaching the **Implemented** qualifier is useful only when you add or remove a qualifier to or from the method.</span></span>

</dd> <dt>

<span data-ttu-id="f167f-139"><span id="ReturnType"></span><span id="returntype"></span><span id="RETURNTYPE"></span>ReturnType</span><span class="sxs-lookup"><span data-stu-id="f167f-139"><span id="ReturnType"></span><span id="returntype"></span><span id="RETURNTYPE"></span>ReturnType</span></span>
</dt> <dd>

<span data-ttu-id="f167f-140">Describe el valor que devuelve el método.</span><span class="sxs-lookup"><span data-stu-id="f167f-140">Describes what value the method returns.</span></span> <span data-ttu-id="f167f-141">El valor devuelto para un método debe ser un objeto booleano, numérico, **Char**, **String**, [DateTime](datetime.md)o Schema.</span><span class="sxs-lookup"><span data-stu-id="f167f-141">The return value for a method must be a Boolean, numeric, **CHAR**, **STRING**, [DATETIME](datetime.md), or schema object.</span></span> <span data-ttu-id="f167f-142">También puede declarar el tipo de valor devuelto como [void](void.md), lo que indica que el método no devuelve nada.</span><span class="sxs-lookup"><span data-stu-id="f167f-142">You can also declare the return type as [VOID](void.md), indicating that the method returns nothing.</span></span> <span data-ttu-id="f167f-143">Sin embargo, no se puede declarar una matriz como un tipo de valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="f167f-143">However, you cannot declare an array as a return value type.</span></span>

</dd> <dt>

<span data-ttu-id="f167f-144"><span id="MethodName"></span><span id="methodname"></span><span id="METHODNAME"></span>MethodName</span><span class="sxs-lookup"><span data-stu-id="f167f-144"><span id="MethodName"></span><span id="methodname"></span><span id="METHODNAME"></span>MethodName</span></span>
</dt> <dd>

<span data-ttu-id="f167f-145">Define el nombre del método.</span><span class="sxs-lookup"><span data-stu-id="f167f-145">Defines the name of the method.</span></span> <span data-ttu-id="f167f-146">Cada método debe tener un nombre único.</span><span class="sxs-lookup"><span data-stu-id="f167f-146">Every method must have a unique name.</span></span> <span data-ttu-id="f167f-147">WMI no permite que existan dos métodos con el mismo nombre y firmas diferentes en una clase o en una jerarquía de clases.</span><span class="sxs-lookup"><span data-stu-id="f167f-147">WMI does not allow two methods with the same name and different signatures to exist in one class or within a class hierarchy.</span></span> <span data-ttu-id="f167f-148">Como tal, tampoco se puede sobrecargar un método.</span><span class="sxs-lookup"><span data-stu-id="f167f-148">As such, you also cannot overload a method.</span></span>

</dd> <dt>

<span data-ttu-id="f167f-149"><span id="ParameterDirection"></span><span id="parameterdirection"></span><span id="PARAMETERDIRECTION"></span>ParameterDirection</span><span class="sxs-lookup"><span data-stu-id="f167f-149"><span id="ParameterDirection"></span><span id="parameterdirection"></span><span id="PARAMETERDIRECTION"></span>ParameterDirection</span></span>
</dt> <dd>

<span data-ttu-id="f167f-150">Contiene calificadores que describen si un parámetro es un parámetro de entrada, un parámetro de salida o ambos.</span><span class="sxs-lookup"><span data-stu-id="f167f-150">Contains qualifiers that describe if a parameter is an input parameter, output parameter, or both.</span></span> <span data-ttu-id="f167f-151">No use el mismo nombre de parámetro más de una vez como parámetro de entrada o más de una vez como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="f167f-151">Do not use the same parameter name more than one time as an input parameter or more than one time as an output parameter.</span></span> <span data-ttu-id="f167f-152">Si el mismo nombre de parámetro aparece con los calificadores [**in**](standard-qualifiers.md) y **out** , la funcionalidad es conceptualmente igual que el uso de los calificadores **in** y **out** en un solo parámetro.</span><span class="sxs-lookup"><span data-stu-id="f167f-152">If the same parameter name appears with both the [**In**](standard-qualifiers.md) and an **Out** qualifiers, the functionality is conceptually the same as using the **In**, **Out** qualifiers on a single parameter.</span></span> <span data-ttu-id="f167f-153">Sin embargo, al usar declaraciones independientes, los parámetros de entrada y salida deben ser exactamente iguales en todos los demás aspectos, incluido el número y el tipo de calificadores de [**identificador**](standard-wmi-qualifiers.md) , y el calificador debe ser el mismo y declarado explícitamente para ambos.</span><span class="sxs-lookup"><span data-stu-id="f167f-153">However, when using separate declarations, the input and output parameters must be exactly the same in all other respects, including the number and type of [**ID**](standard-wmi-qualifiers.md) qualifiers, and the qualifier must be the same and explicitly declared for both.</span></span> <span data-ttu-id="f167f-154">Se recomienda encarecidamente usar los calificadores **in** y **out** dentro de una única declaración de parámetro.</span><span class="sxs-lookup"><span data-stu-id="f167f-154">It is strongly recommended to use the **In**, **Out** qualifiers within a single parameter declaration.</span></span>

</dd> <dt>

<span data-ttu-id="f167f-155"><span id="IDQualifier"></span><span id="idqualifier"></span><span id="IDQUALIFIER"></span>**IDQualifier**</span><span class="sxs-lookup"><span data-stu-id="f167f-155"><span id="IDQualifier"></span><span id="idqualifier"></span><span id="IDQUALIFIER"></span>**IDQualifier**</span></span>
</dt> <dd>

<span data-ttu-id="f167f-156">Contiene el calificador de [**identificador**](standard-wmi-qualifiers.md) que identifica de forma única la posición de cada parámetro dentro de la secuencia de parámetros en el método.</span><span class="sxs-lookup"><span data-stu-id="f167f-156">Contains the [**ID**](standard-wmi-qualifiers.md) qualifier that uniquely identifies the position of each parameter within the sequence of parameters in the method.</span></span> <span data-ttu-id="f167f-157">De forma predeterminada, el compilador MOF marca automáticamente los parámetros con un calificador de **identificador** .</span><span class="sxs-lookup"><span data-stu-id="f167f-157">By default, the MOF compiler automatically marks parameters with an **ID** qualifier.</span></span> <span data-ttu-id="f167f-158">El compilador marca el primer parámetro con un valor de 0 (cero), el segundo parámetro con un valor de 1 (uno), etc.</span><span class="sxs-lookup"><span data-stu-id="f167f-158">The compiler marks the first parameter with a value of 0 (zero), the second parameter a value of 1 (one), and so on.</span></span> <span data-ttu-id="f167f-159">Si es necesario, puede indicar explícitamente la secuencia de ID. en el código MOF.</span><span class="sxs-lookup"><span data-stu-id="f167f-159">If necessary, you can explicitly state the ID sequence in your MOF code.</span></span>

</dd> <dt>

<span data-ttu-id="f167f-160"><span id="ParameterType"></span><span id="parametertype"></span><span id="PARAMETERTYPE"></span>ParameterType</span><span class="sxs-lookup"><span data-stu-id="f167f-160"><span id="ParameterType"></span><span id="parametertype"></span><span id="PARAMETERTYPE"></span>ParameterType</span></span>
</dt> <dd>

<span data-ttu-id="f167f-161">Describe qué tipo de datos puede aceptar el método.</span><span class="sxs-lookup"><span data-stu-id="f167f-161">Describes what data type the method can accept.</span></span> <span data-ttu-id="f167f-162">Puede definir un tipo de parámetro como cualquier valor de datos MOF, como una matriz, un objeto de esquema o una referencia.</span><span class="sxs-lookup"><span data-stu-id="f167f-162">You can define a parameter type as any MOF data value, including an array, schema object, or reference.</span></span> <span data-ttu-id="f167f-163">Al utilizar una matriz como parámetro, utilice la matriz como sin enlazar o con un tamaño explícito.</span><span class="sxs-lookup"><span data-stu-id="f167f-163">When using an array as a parameter, use the array as unbound or with an explicit size.</span></span>

</dd> <dt>

<span data-ttu-id="f167f-164"><span id="ParameterName"></span><span id="parametername"></span><span id="PARAMETERNAME"></span>ParameterName</span><span class="sxs-lookup"><span data-stu-id="f167f-164"><span id="ParameterName"></span><span id="parametername"></span><span id="PARAMETERNAME"></span>ParameterName</span></span>
</dt> <dd>

<span data-ttu-id="f167f-165">Contiene el nombre del parámetro.</span><span class="sxs-lookup"><span data-stu-id="f167f-165">Contains the name of the parameter.</span></span> <span data-ttu-id="f167f-166">También puede optar por definir el valor predeterminado del parámetro en este punto.</span><span class="sxs-lookup"><span data-stu-id="f167f-166">You can also choose to define the default value of the parameter at this point.</span></span> <span data-ttu-id="f167f-167">Los parámetros que carecen de valores iniciales permanecen sin asignar.</span><span class="sxs-lookup"><span data-stu-id="f167f-167">Parameters lacking initial values remain unassigned.</span></span>

</dd> </dl>

<span data-ttu-id="f167f-168">En el ejemplo de código siguiente se describen los calificadores y listas de parámetros.</span><span class="sxs-lookup"><span data-stu-id="f167f-168">The following code example describes parameter listing and qualifiers.</span></span>

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] sint32 InParam);
    [Implemented] 
    void MyMethod2 ([in, id(0)] sint32 InParam, 
       [out, id(1)] sint32 OutParam);
    [Implemented] 
    sint32 MyMethod3 ([in, out, id(0)] sint32 InOutParam);
};
```

<span data-ttu-id="f167f-169">En el ejemplo de código siguiente se describe cómo usar una matriz en un parámetro MOF.</span><span class="sxs-lookup"><span data-stu-id="f167f-169">The following code example describes how to use an array in a MOF parameter.</span></span>

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk DiskParam[]);
    [Implemented] 
    sint32 MyMethod2 ([in, id(0)] Win32_LogicalDisk DiskParam[32]);
};
```

<span data-ttu-id="f167f-170">En el ejemplo de código siguiente se describe el uso de un objeto de esquema como un parámetro y un valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="f167f-170">The following code example describes using a schema object as both a parameter and return value.</span></span>

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk 
        DiskParam);
    [Implemented] 
    Win32_LogicalDisk MyMethod2 ([in, id(0)] string DiskVolLabel);
};
```

<span data-ttu-id="f167f-171">En el ejemplo de código siguiente se describe cómo incluir dos referencias: una a una instancia de la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) y la otra a una instancia de un tipo de objeto desconocido.</span><span class="sxs-lookup"><span data-stu-id="f167f-171">The following code example describes how to include two references: one to an instance of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class and the other to an instance of an unknown object type.</span></span>

``` syntax
[Dynamic, Provider("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk ref DiskRef);
    [Implemented] 
    sint32 MyMethod2 ([in, id(0)] object ref AnyObject);
};
```

## <a name="creating-a-wmi-class-method-in-c"></a><span data-ttu-id="f167f-172">Crear un método de clase WMI en C++</span><span class="sxs-lookup"><span data-stu-id="f167f-172">Creating a WMI Class Method in C++</span></span>

<span data-ttu-id="f167f-173">En el procedimiento siguiente se describe cómo crear un método de clase WMI mediante programación.</span><span class="sxs-lookup"><span data-stu-id="f167f-173">The following procedure describes how to create a WMI class method programmatically.</span></span>

<span data-ttu-id="f167f-174">**Para crear un método de clase WMI mediante programación**</span><span class="sxs-lookup"><span data-stu-id="f167f-174">**To create a WMI class method programmatically**</span></span>

1.  <span data-ttu-id="f167f-175">Cree la clase a la que pertenecerá el método.</span><span class="sxs-lookup"><span data-stu-id="f167f-175">Create the class to which the method will belong.</span></span>

    <span data-ttu-id="f167f-176">En primer lugar, debe tener una clase en la que colocar el método antes de crear el método.</span><span class="sxs-lookup"><span data-stu-id="f167f-176">You must first have a class to place the method in before you create the method.</span></span>

2.  <span data-ttu-id="f167f-177">Recupere dos clases secundarias de la clase de sistema [**\_ \_ Parameters**](--parameters.md) mediante [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="f167f-177">Retrieve two child classes of the [**\_\_PARAMETERS**](--parameters.md) system class using either [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

    <span data-ttu-id="f167f-178">Use la primera clase secundaria para describir los parámetros in-y el segundo para describir los parámetros out.</span><span class="sxs-lookup"><span data-stu-id="f167f-178">Use the first child class to describe the in-parameters, and the second to describe the out-parameters.</span></span> <span data-ttu-id="f167f-179">Si es necesario, puede realizar una recuperación única seguida de una llamada al método [**IWbemClassObject:: Clone**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-clone) .</span><span class="sxs-lookup"><span data-stu-id="f167f-179">If necessary, you can perform a single retrieval followed by a call to the [**IWbemClassObject::Clone**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-clone) method.</span></span>

3.  <span data-ttu-id="f167f-180">Escriba los parámetros in-en la primera clase y los parámetros out en la segunda clase, usando una o más llamadas a [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="f167f-180">Write the in-parameters to the first class, and the out-parameters to the second class, using one or more calls to [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="f167f-181">Al describir los parámetros de un método, observe las siguientes reglas y restricciones:</span><span class="sxs-lookup"><span data-stu-id="f167f-181">When describing parameters to a method, observe the following rules and restrictions:</span></span>

    -   <span data-ttu-id="f167f-182">Trate los \[ parámetros in, out \] como entradas independientes, uno en el objeto que contiene los parámetros in-y uno en el objeto que contiene los parámetros out.</span><span class="sxs-lookup"><span data-stu-id="f167f-182">Treat the \[in, out\] parameters as separate entries, one in the object that contains the in-parameters and one in the object that contains the out-parameters.</span></span>
    -   <span data-ttu-id="f167f-183">Aparte de los \[ calificadores in, out \] , los calificadores restantes deben ser exactamente iguales.</span><span class="sxs-lookup"><span data-stu-id="f167f-183">Other than the \[in, out\] qualifiers, the remaining qualifiers must be exactly the same.</span></span>
    -   <span data-ttu-id="f167f-184">Especifique los calificadores de [**identificador**](standard-wmi-qualifiers.md) , empezando por 0 (cero), uno para cada parámetro.</span><span class="sxs-lookup"><span data-stu-id="f167f-184">Specify the [**ID**](standard-wmi-qualifiers.md) qualifiers, starting at 0 (zero), one for each parameter.</span></span>

        <span data-ttu-id="f167f-185">El orden de los parámetros de entrada o salida lo establece el valor del calificador de [**ID**](standard-wmi-qualifiers.md) . en cada parámetro.</span><span class="sxs-lookup"><span data-stu-id="f167f-185">The order of the input or output parameters is established by the value of the [**ID**](standard-wmi-qualifiers.md) qualifier on each parameter.</span></span> <span data-ttu-id="f167f-186">Todos los argumentos de entrada deben preceder a cualquier argumento de salida.</span><span class="sxs-lookup"><span data-stu-id="f167f-186">All input arguments must precede any output arguments.</span></span> <span data-ttu-id="f167f-187">Si se cambia el orden de los parámetros de entrada y salida del método al actualizar un proveedor de métodos existente, pueden producirse errores en las aplicaciones que llaman al método.</span><span class="sxs-lookup"><span data-stu-id="f167f-187">Changing the order of method input and output parameters when updating an existing method provider can cause applications that call the method to fail.</span></span> <span data-ttu-id="f167f-188">Agregue nuevos parámetros de entrada al final de los parámetros existentes en lugar de insertarlos en la secuencia que ya está establecida.</span><span class="sxs-lookup"><span data-stu-id="f167f-188">Add new input parameters at the end of the existing parameters rather than inserting them in the sequence that is already established.</span></span>

        <span data-ttu-id="f167f-189">Asegúrese de no dejar huecos en la secuencia del calificador de [**identificador**](standard-wmi-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="f167f-189">Make sure to leave no gaps in the [**ID**](standard-wmi-qualifiers.md) qualifier sequence.</span></span>

    -   <span data-ttu-id="f167f-190">Coloque el valor devuelto en la clase out-Parameters como una propiedad denominada **ReturnValue**.</span><span class="sxs-lookup"><span data-stu-id="f167f-190">Place the return value in the out-parameters class as a property named **ReturnValue**.</span></span>

        <span data-ttu-id="f167f-191">Esto identifica la propiedad como el valor devuelto del método.</span><span class="sxs-lookup"><span data-stu-id="f167f-191">This identifies the property as the return value of the method.</span></span> <span data-ttu-id="f167f-192">El tipo CIM de esta propiedad es el tipo de valor devuelto del método.</span><span class="sxs-lookup"><span data-stu-id="f167f-192">The CIM type of this property is the return type of the method.</span></span> <span data-ttu-id="f167f-193">Si el método tiene un tipo de valor devuelto de void, no hay ninguna propiedad **ReturnValue** en absoluto.</span><span class="sxs-lookup"><span data-stu-id="f167f-193">If the method has a return type of void, then do not have a **ReturnValue** property at all.</span></span> <span data-ttu-id="f167f-194">Además, la propiedad **ReturnValue** no puede tener un calificador de [**identificador**](standard-wmi-qualifiers.md) como los argumentos del método.</span><span class="sxs-lookup"><span data-stu-id="f167f-194">Also, the **ReturnValue** property cannot have an [**ID**](standard-wmi-qualifiers.md) qualifier like the arguments of the method.</span></span> <span data-ttu-id="f167f-195">La asignación de un calificador de **identificador** a la propiedad **ReturnValue** produce un error de WMI.</span><span class="sxs-lookup"><span data-stu-id="f167f-195">Assigning an **ID** qualifier to the **ReturnValue** property produces a WMI error.</span></span>

    -   <span data-ttu-id="f167f-196">Exprese los valores de parámetro predeterminados para la propiedad en la clase.</span><span class="sxs-lookup"><span data-stu-id="f167f-196">Express any default parameter values for the property in the class.</span></span>

4.  <span data-ttu-id="f167f-197">Coloque ambos objetos de [**\_ \_ parámetros**](--parameters.md) en la clase primaria con una llamada a [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span><span class="sxs-lookup"><span data-stu-id="f167f-197">Place both [**\_\_PARAMETERS**](--parameters.md) objects into the parent class with a call to [**IWbemClassObject::PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span></span>

    <span data-ttu-id="f167f-198">Una única llamada a [**PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod) puede colocar ambos objetos de [**\_ \_ parámetros**](--parameters.md) en la clase.</span><span class="sxs-lookup"><span data-stu-id="f167f-198">A single call to [**PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod) can place both [**\_\_PARAMETERS**](--parameters.md) objects into the class.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f167f-199">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f167f-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f167f-200">Crear una clase</span><span class="sxs-lookup"><span data-stu-id="f167f-200">Creating a Class</span></span>](creating-a-class.md)
</dt> </dl>

 

 
