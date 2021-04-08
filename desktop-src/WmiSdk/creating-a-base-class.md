---
description: La manera recomendada de crear una nueva clase base de WMI para un proveedor WMI es en un archivo Managed Object Format (MOF).
ms.assetid: d46060aa-77c3-4f51-b4a7-2c3612f2bc5c
ms.tgt_platform: multiple
title: Crear una clase base de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebdcbe6995a7782d854a4d0950db841f23a30b45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002831"
---
# <a name="creating-a-wmi-base-class"></a><span data-ttu-id="b1810-103">Crear una clase base de WMI</span><span class="sxs-lookup"><span data-stu-id="b1810-103">Creating a WMI Base Class</span></span>

<span data-ttu-id="b1810-104">La manera recomendada de crear una nueva clase base de WMI para un proveedor WMI es en un archivo Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="b1810-104">The recommended way to create a new WMI base class for a WMI provider is in a Managed Object Format (MOF) file.</span></span> <span data-ttu-id="b1810-105">También puede crear una clase base mediante la [API com para WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="b1810-105">You can also create a base class using the [COM API for WMI](com-api-for-wmi.md).</span></span> <span data-ttu-id="b1810-106">Aunque se puede crear una clase base o derivada en un script, sin que un proveedor proporcione datos a la clase y sus subclases, la clase no es útil.</span><span class="sxs-lookup"><span data-stu-id="b1810-106">While you can create a base or derived class in script, without a provider supplying data to the class and its subclasses, the class is not useful.</span></span>

<span data-ttu-id="b1810-107">En este tema se describen las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="b1810-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="b1810-108">Crear una clase base mediante MOF</span><span class="sxs-lookup"><span data-stu-id="b1810-108">Creating a Base Class Using MOF</span></span>](#creating-a-base-class-using-mof)
-   [<span data-ttu-id="b1810-109">Crear una clase base con C++</span><span class="sxs-lookup"><span data-stu-id="b1810-109">Creating a Base Class with C++</span></span>](#creating-a-base-class-with-c)
-   [<span data-ttu-id="b1810-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b1810-110">Related topics</span></span>](#related-topics)

## <a name="creating-a-base-class-using-mof"></a><span data-ttu-id="b1810-111">Crear una clase base mediante MOF</span><span class="sxs-lookup"><span data-stu-id="b1810-111">Creating a Base Class Using MOF</span></span>

<span data-ttu-id="b1810-112">Las clases WMI suelen basarse en la herencia.</span><span class="sxs-lookup"><span data-stu-id="b1810-112">WMI classes usually rely on inheritance.</span></span> <span data-ttu-id="b1810-113">Antes de crear una clase base, consulte las clases de Modelo de información común (CIM) disponibles en el equipo de la tarea de administración distribuida ([DMTF](https://www.dmtf.org/)).</span><span class="sxs-lookup"><span data-stu-id="b1810-113">Before creating a base class, check the Common Information Model (CIM) classes available from the Distributed Management Task Force ([DMTF](https://www.dmtf.org/)).</span></span>

<span data-ttu-id="b1810-114">Si muchas clases derivadas van a utilizar las mismas propiedades, coloque estas propiedades y métodos en la clase base.</span><span class="sxs-lookup"><span data-stu-id="b1810-114">If many derived classes will use the same properties, put these properties and methods in your base class.</span></span> <span data-ttu-id="b1810-115">El número máximo de propiedades que puede definir en una clase WMI es 1024.</span><span class="sxs-lookup"><span data-stu-id="b1810-115">The maximum number of properties you can define in a WMI class is 1024.</span></span>

<span data-ttu-id="b1810-116">Al crear una clase base, observe la siguiente lista de instrucciones para los nombres de clase:</span><span class="sxs-lookup"><span data-stu-id="b1810-116">When creating a base class, observe the following list of guidelines for class names:</span></span>

-   <span data-ttu-id="b1810-117">Use mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b1810-117">Use both uppercase and lowercase letters.</span></span>
-   <span data-ttu-id="b1810-118">Comience un nombre de clase con una letra.</span><span class="sxs-lookup"><span data-stu-id="b1810-118">Begin a class name with a letter.</span></span>
-   <span data-ttu-id="b1810-119">No utilice un carácter de subrayado inicial o final.</span><span class="sxs-lookup"><span data-stu-id="b1810-119">Do not use either a leading or trailing underscore.</span></span>
-   <span data-ttu-id="b1810-120">Defina todos los caracteres restantes como letras, dígitos o caracteres de subrayado.</span><span class="sxs-lookup"><span data-stu-id="b1810-120">Define all remaining characters as letters, digits, or underscores.</span></span>
-   <span data-ttu-id="b1810-121">Use una Convención de nomenclatura coherente.</span><span class="sxs-lookup"><span data-stu-id="b1810-121">Use a consistent naming convention.</span></span>

    <span data-ttu-id="b1810-122">Aunque no es necesario, una buena Convención de nomenclatura para una clase son dos componentes Unidos por un carácter de subrayado.</span><span class="sxs-lookup"><span data-stu-id="b1810-122">While not necessary, a good naming convention for a class is two components joined by an underscore.</span></span> <span data-ttu-id="b1810-123">Cuando sea posible, un nombre de proveedor debe componer la primera mitad del nombre y un nombre de clase descriptivo debe ser la segunda parte.</span><span class="sxs-lookup"><span data-stu-id="b1810-123">When possible, a vendor name should make up the first half of the name, and a descriptive class name should be the second part.</span></span>

> [!Note]  
> <span data-ttu-id="b1810-124">Las clases no se pueden cambiar durante la ejecución de proveedores.</span><span class="sxs-lookup"><span data-stu-id="b1810-124">Classes cannot be changed during execution of providers.</span></span> <span data-ttu-id="b1810-125">Debe detener la actividad, cambiar la clase y, a continuación, reiniciar el servicio de administración de Windows.</span><span class="sxs-lookup"><span data-stu-id="b1810-125">You must stop the activity, change the class, and then restart the Windows Management service.</span></span> <span data-ttu-id="b1810-126">Actualmente no es posible detectar un cambio de clase.</span><span class="sxs-lookup"><span data-stu-id="b1810-126">Detecting a class change is currently not possible.</span></span>

 

<span data-ttu-id="b1810-127">En MOF, cree una clase base asignándole un nombre con la palabra clave **Class** , pero no para indicar una clase primaria.</span><span class="sxs-lookup"><span data-stu-id="b1810-127">In MOF, create a base class by naming it with the **class** keyword, but not indicating a parent class.</span></span>

<span data-ttu-id="b1810-128">**Para crear una clase base mediante código MOF**</span><span class="sxs-lookup"><span data-stu-id="b1810-128">**To create a base class using MOF code**</span></span>

1.  <span data-ttu-id="b1810-129">Use la palabra clave **Class** con el nombre de la nueva clase, seguido de un par de llaves y un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="b1810-129">Use the **class** keyword with the name of the new class, followed by a pair of curly braces and a semicolon.</span></span> <span data-ttu-id="b1810-130">Agregue las propiedades y los métodos de la clase entre las llaves.</span><span class="sxs-lookup"><span data-stu-id="b1810-130">Add properties and methods for the class between the curly braces.</span></span> <span data-ttu-id="b1810-131">Se proporciona el siguiente ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="b1810-131">The following code example is provided.</span></span>

    <span data-ttu-id="b1810-132">En el ejemplo de código siguiente se muestra cómo debe definirse una clase base.</span><span class="sxs-lookup"><span data-stu-id="b1810-132">The following code example shows how a base class should be defined.</span></span>

    ``` syntax
    class MyClass_BaseDisk
    {
    };
    ```

    <span data-ttu-id="b1810-133">En el ejemplo de código siguiente se muestra una definición incorrecta de una clase base.</span><span class="sxs-lookup"><span data-stu-id="b1810-133">The following code example shows an incorrect definition of a base class.</span></span>

    ``` syntax
    class MyClass_BaseDisk : CIM_LogicalDisk
    {
    };
    ```

2.  <span data-ttu-id="b1810-134">Agregue los [*calificadores*](gloss-q.md) de clase antes de la palabra clave Class para modificar la forma en que se utiliza la clase.</span><span class="sxs-lookup"><span data-stu-id="b1810-134">Add any class [*qualifiers*](gloss-q.md) before the class keyword to modify the way the class is used.</span></span> <span data-ttu-id="b1810-135">Coloque los calificadores entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="b1810-135">Place the qualifiers between square brackets.</span></span> <span data-ttu-id="b1810-136">Para obtener más información acerca de los calificadores para modificar clases, vea [calificadores de WMI](wmi-qualifiers.md).</span><span class="sxs-lookup"><span data-stu-id="b1810-136">For more information about qualifiers for modifying classes, see [WMI Qualifiers](wmi-qualifiers.md).</span></span> <span data-ttu-id="b1810-137">Utilice el calificador **abstracto** para indicar que no se puede crear una instancia de esta clase directamente.</span><span class="sxs-lookup"><span data-stu-id="b1810-137">Use the **Abstract** qualifier to indicate that you cannot create an instance of this class directly.</span></span> <span data-ttu-id="b1810-138">Las clases abstractas se usan a menudo para definir las propiedades o los métodos que usarán varias clases derivadas.</span><span class="sxs-lookup"><span data-stu-id="b1810-138">Abstract classes are often used to define properties or methods that will be used by several derived classes.</span></span> <span data-ttu-id="b1810-139">Para obtener más información, vea [crear una clase derivada](creating-a-derived-class.md).</span><span class="sxs-lookup"><span data-stu-id="b1810-139">For more information, see [Creating a Derived Class](creating-a-derived-class.md).</span></span>

    <span data-ttu-id="b1810-140">En el ejemplo de código siguiente se define la clase como abstracta y se define el proveedor que proporcionará los datos.</span><span class="sxs-lookup"><span data-stu-id="b1810-140">The following code example defines the class as abstract and defines the provider that will supply the data.</span></span> <span data-ttu-id="b1810-141">El [*tipo*](gloss-f.md) de calificador **ToSubClass** indica que las clases derivadas heredan la información del calificador de **proveedor** .</span><span class="sxs-lookup"><span data-stu-id="b1810-141">The **ToSubClass** qualifier [*flavor*](gloss-f.md) indicates that the information in the **Provider** qualifier is inherited by derived classes.</span></span>

    ``` syntax
    [Abstract, Provider("MyProvider") : ToSubClass]
    class MyClass_BaseDisk
    {
    };
    ```

3.  <span data-ttu-id="b1810-142">Agregue las propiedades y los métodos de la clase entre corchetes antes del nombre de la propiedad o del método.</span><span class="sxs-lookup"><span data-stu-id="b1810-142">Add the properties and methods for the class inside square brackets before the property or method name.</span></span> <span data-ttu-id="b1810-143">Para obtener más información, vea [Agregar una propiedad](adding-a-property.md) y [crear un método](creating-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b1810-143">For more information, see [Adding a Property](adding-a-property.md) and [Creating a Method](creating-a-method.md).</span></span> <span data-ttu-id="b1810-144">Puede modificar estas propiedades y métodos mediante calificadores MOF.</span><span class="sxs-lookup"><span data-stu-id="b1810-144">You can modify these properties and methods using MOF qualifiers.</span></span> <span data-ttu-id="b1810-145">Para obtener más información, consulte [Agregar un calificador](adding-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="b1810-145">For more information, see [Adding a Qualifier](adding-a-qualifier.md).</span></span>

    <span data-ttu-id="b1810-146">En el ejemplo de código siguiente se muestra cómo modificar propiedades y métodos con calificadores MOF.</span><span class="sxs-lookup"><span data-stu-id="b1810-146">The following code example shows how to modify properties and methods with MOF qualifiers.</span></span>

    ``` syntax
    [read : ToSubClass, key : ToSubClass ] string DeviceID;
      [read : ToSubClass] uint32 State;
      [read : ToSubclass, write : ToSubClass] uint64 LimitUsers;
    ```

4.  <span data-ttu-id="b1810-147">Guarde el archivo MOF con la extensión. mof.</span><span class="sxs-lookup"><span data-stu-id="b1810-147">Save the MOF file with an extension of .mof.</span></span>
5.  <span data-ttu-id="b1810-148">Registre la clase con WMI ejecutando [**Mofcomp.exe**](mofcomp.md) en el archivo.</span><span class="sxs-lookup"><span data-stu-id="b1810-148">Register the class with WMI by running [**Mofcomp.exe**](mofcomp.md) on the file.</span></span>

    <span data-ttu-id="b1810-149">**mofcomp.exe** *newmof. mof*</span><span class="sxs-lookup"><span data-stu-id="b1810-149">**mofcomp.exe** *newmof.mof*</span></span>

    <span data-ttu-id="b1810-150">Si no usa el modificador **-N** o el espacio de nombres pragma de comando de preprocesador \# [](pragma-namespace.md) para especificar un espacio de nombres, las clases MOF compiladas se almacenarán en el \\ espacio de nombres predeterminado raíz en el repositorio.</span><span class="sxs-lookup"><span data-stu-id="b1810-150">If you do not use the **-N** switch or the preprocessor command \#[**pragma namespace**](pragma-namespace.md) to specify a namespace, the compiled MOF classes will be stored in the root\\default namespace in the repository.</span></span> <span data-ttu-id="b1810-151">Para obtener más información, consulte [**MOFCOMP**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="b1810-151">For more information, see [**mofcomp**](mofcomp.md).</span></span>

<span data-ttu-id="b1810-152">En el ejemplo de código siguiente se combinan los ejemplos de código MOF descritos en el procedimiento anterior y se muestra cómo crear una clase base en el \\ espacio de nombres root cimv2 mediante MOF.</span><span class="sxs-lookup"><span data-stu-id="b1810-152">The following code example combines the MOF code examples discussed in the previous procedure and shows how to create a base class in the root\\cimv2 namespace using MOF.</span></span>

``` syntax
#pragma namespace("\\\\.\\Root\\cimv2")

[Abstract, Provider("MyProvider") : ToSubClass]
class MyClass_BaseDisk
{
  [read : ToSubClass, key : ToSubClass ] string DeviceID;
  [read : ToSubClass] uint32 State;
  [read : ToSubClass, write : ToSubClass] uint64 LimitUsers;
};
```

<span data-ttu-id="b1810-153">Para obtener más información, vea [crear una clase derivada](creating-a-derived-class.md) para obtener un ejemplo de una clase dinámica derivada de esta clase base.</span><span class="sxs-lookup"><span data-stu-id="b1810-153">For more information, see [Creating a Derived Class](creating-a-derived-class.md) for an example of a dynamic class derived from this base class.</span></span>

## <a name="creating-a-base-class-with-c"></a><span data-ttu-id="b1810-154">Crear una clase base con C++</span><span class="sxs-lookup"><span data-stu-id="b1810-154">Creating a Base Class with C++</span></span>

<span data-ttu-id="b1810-155">La creación de una clase base mediante la API de WMI es principalmente una serie de comandos Put que definen la clase y registran la clase en WMI.</span><span class="sxs-lookup"><span data-stu-id="b1810-155">Creating a base class using the WMI API is mainly a series of Put commands that define the class and register the class with WMI.</span></span> <span data-ttu-id="b1810-156">El propósito principal de esta API es permitir que las aplicaciones cliente creen clases base.</span><span class="sxs-lookup"><span data-stu-id="b1810-156">The main purpose of this API is to enable client applications to create base classes.</span></span> <span data-ttu-id="b1810-157">Sin embargo, también puede tener un proveedor que use esta API para crear una clase base.</span><span class="sxs-lookup"><span data-stu-id="b1810-157">However, you can also have a provider use this API to create a base class.</span></span> <span data-ttu-id="b1810-158">Por ejemplo, si cree que el código MOF del proveedor no se instalará correctamente, puede indicar a su proveedor que cree automáticamente las clases correctas en el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="b1810-158">For example, if you believe that the MOF code for your provider will not be installed properly, you can instruct your provider to automatically create the correct classes in the WMI repository.</span></span> <span data-ttu-id="b1810-159">Para obtener más información sobre los proveedores, consulte [escribir un proveedor de clases](writing-a-class-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b1810-159">For more information about providers, see [Writing a Class Provider](writing-a-class-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="b1810-160">Las clases no se pueden cambiar durante la ejecución de proveedores.</span><span class="sxs-lookup"><span data-stu-id="b1810-160">Classes cannot be changed during execution of providers.</span></span> <span data-ttu-id="b1810-161">Debe detener la actividad, cambiar la clase y, a continuación, reiniciar el servicio de administración de Windows.</span><span class="sxs-lookup"><span data-stu-id="b1810-161">You must stop the activity, change the class, and then restart the Windows Management service.</span></span> <span data-ttu-id="b1810-162">Actualmente no es posible detectar un cambio de clase.</span><span class="sxs-lookup"><span data-stu-id="b1810-162">Detecting a class change is currently not possible.</span></span>

 

<span data-ttu-id="b1810-163">El código requiere que la siguiente referencia se compile correctamente.</span><span class="sxs-lookup"><span data-stu-id="b1810-163">The code requires the following reference to compile correctly.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="b1810-164">Puede crear una nueva clase base mediante programación con la [API com para WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="b1810-164">You can create a new base class programmatically using the [COM API for WMI](com-api-for-wmi.md).</span></span>

<span data-ttu-id="b1810-165">**Para crear una nueva clase base con la API de WMI**</span><span class="sxs-lookup"><span data-stu-id="b1810-165">**To create a new base class with the WMI API**</span></span>

1.  <span data-ttu-id="b1810-166">Recupere una definición de la nueva clase llamando al método [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) con el parámetro *strObjectPath* establecido en un valor **null** .</span><span class="sxs-lookup"><span data-stu-id="b1810-166">Retrieve a definition for the new class by calling the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) method with the *strObjectPath* parameter set to a **null** value.</span></span>

    <span data-ttu-id="b1810-167">En el ejemplo de código siguiente se muestra cómo recuperar una definición para una nueva clase.</span><span class="sxs-lookup"><span data-stu-id="b1810-167">The following code example shows how to retrieve a definition for a new class.</span></span>

    ```C++
    IWbemServices* pSvc = 0;
    IWbemContext* pCtx = 0;
    IWbemClassObject* pNewClass = 0;
    IWbemCallResult* pResult = 0;
    HRESULT hRes = pSvc->GetObject(0, 0, pCtx, &pNewClass, &pResult);
    ```

    

2.  <span data-ttu-id="b1810-168">Establezca un nombre para la clase estableciendo la propiedad System de **\_ \_ clase** con una llamada al método [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .</span><span class="sxs-lookup"><span data-stu-id="b1810-168">Establish a name for the class by setting the **\_\_CLASS** system property with a call to the [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) method.</span></span>

    <span data-ttu-id="b1810-169">En el ejemplo de código siguiente se muestra cómo asignar un nombre a la clase estableciendo la propiedad del sistema de **\_ \_ clase** .</span><span class="sxs-lookup"><span data-stu-id="b1810-169">The following code example shows how to name the class by setting the **\_\_CLASS** system property.</span></span>

    ```C++
    VARIANT v;
    VariantInit(&v);
    V_VT(&v) = VT_BSTR;

    V_BSTR(&v) = SysAllocString(L"Example");
    BSTR Class = SysAllocString(L"__CLASS");
    pNewClass->Put(Class, 0, &v, 0);
    SysFreeString(Class);
    VariantClear(&v);
    ```

    

3.  <span data-ttu-id="b1810-170">Cree la propiedad o propiedades de clave llamando a [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="b1810-170">Create the key property or properties by calling [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="b1810-171">En el ejemplo de código siguiente se describe cómo crear la propiedad de [**Índice**](swbemrefreshableitem-index.md) , que se etiqueta como una propiedad clave en el paso 4.</span><span class="sxs-lookup"><span data-stu-id="b1810-171">The following code example describes how to create the [**Index**](swbemrefreshableitem-index.md) property, which is labeled as a key property in Step 4.</span></span>

    ```C++
      BSTR KeyProp = SysAllocString(L"Index");
      pNewClass->Put(KeyProp, 0, NULL, CIM_STRING);
    ```

    

4.  <span data-ttu-id="b1810-172">Adjunte el calificador estándar de [**clave**](standard-qualifiers.md) a la propiedad de clave llamando primero al método [**IWbemClassObject:: GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) y, a continuación, al método [**IWbemQualifierSet::P UT**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) .</span><span class="sxs-lookup"><span data-stu-id="b1810-172">Attach the [**Key**](standard-qualifiers.md) standard qualifier to the key property by first calling the [**IWbemClassObject::GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) method and then the [**IWbemQualifierSet::Put**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) method.</span></span>

    <span data-ttu-id="b1810-173">En el ejemplo de código siguiente se muestra cómo adjuntar el calificador estándar de [**clave**](standard-qualifiers.md) a la propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="b1810-173">The following code example shows how to attach the [**Key**](standard-qualifiers.md) standard qualifier to the key property.</span></span>

    ```C++
      IWbemQualifierSet *pQual = 0;
      pNewClass->GetPropertyQualifierSet(KeyProp, &pQual);
      SysFreeString(KeyProp);

      V_VT(&v) = VT_BOOL;
      V_BOOL(&v) = VARIANT_TRUE;
      BSTR Key = SysAllocString(L"Key");

      pQual->Put(Key, &v, 0);   // Flavors not required for Key 
      SysFreeString(Key);

      // No longer need the qualifier set for "Index"
      pQual->Release();   
      VariantClear(&v);
    ```

    

5.  <span data-ttu-id="b1810-174">Cree otras propiedades de la clase con [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="b1810-174">Create other properties of the class with [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="b1810-175">En el ejemplo de código siguiente se describe cómo crear propiedades adicionales.</span><span class="sxs-lookup"><span data-stu-id="b1810-175">The following code example describes how to create additional properties.</span></span>

    ```C++
      V_VT(&v) = VT_BSTR;
      V_BSTR(&v) = SysAllocString(L"<default>");
      BSTR OtherProp = SysAllocString(L"OtherInfo");
      pNewClass->Put(OtherProp, 0, &v, CIM_STRING);
      SysFreeString(OtherProp);
      VariantClear(&v);

      OtherProp = SysAllocString(L"IntVal");
      pNewClass->Put(OtherProp, 0, NULL, CIM_SINT32); // NULL is default
      SysFreeString(OtherProp);
    ```

    

6.  <span data-ttu-id="b1810-176">Registre la nueva clase llamando a [**IWbemServices::P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span><span class="sxs-lookup"><span data-stu-id="b1810-176">Register the new class by calling [**IWbemServices::PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span></span>

    <span data-ttu-id="b1810-177">Dado que no puede definir claves e índices después de registrar una nueva clase, asegúrese de que ha definido todas las propiedades antes de llamar a [**PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span><span class="sxs-lookup"><span data-stu-id="b1810-177">Because you cannot define keys and indices after you register a new class, ensure that you have defined all of your properties before calling [**PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span></span>

    <span data-ttu-id="b1810-178">En el ejemplo de código siguiente se describe cómo registrar una nueva clase.</span><span class="sxs-lookup"><span data-stu-id="b1810-178">The following code example describes how to register a new class.</span></span>

    ```C++
      hRes = pSvc->PutClass(pNewClass, 0, pCtx, &pResult);
      pNewClass->Release();
    ```

    

<span data-ttu-id="b1810-179">En el ejemplo de código siguiente se combinan los ejemplos de código descritos en el procedimiento anterior y se muestra cómo crear una clase base mediante la API de WMI.</span><span class="sxs-lookup"><span data-stu-id="b1810-179">The following code example combines the code examples discussed in the previous procedure and shows how to create a base class using the WMI API.</span></span>


```C++
void CreateClass(IWbemServices *pSvc)
{
  IWbemClassObject *pNewClass = 0;
  IWbemContext *pCtx = 0;
  IWbemCallResult *pResult = 0;

  // Get a class definition. 
  // ============================
  HRESULT hRes = pSvc->GetObject(0, 0, pCtx, &pNewClass, &pResult);
  VARIANT v;
  VariantInit(&v);

  // Create the class name.
  // ============================
  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"Example");
  BSTR Class = SysAllocString(L"__CLASS");
  pNewClass->Put(Class, 0, &v, 0);
  SysFreeString(Class);
  VariantClear(&v);

  // Create the key property. 
  // ============================
  BSTR KeyProp = SysAllocString(L"Index");
  pNewClass->Put(KeyProp, 0, NULL, CIM_STRING);

  // Attach Key qualifier to mark the "Index" property as the key.
  // ============================
  IWbemQualifierSet *pQual = 0;
  pNewClass->GetPropertyQualifierSet(KeyProp, &pQual);
  SysFreeString(KeyProp);

  V_VT(&v) = VT_BOOL;
  V_BOOL(&v) = VARIANT_TRUE;
  BSTR Key = SysAllocString(L"Key");

  pQual->Put(Key, &v, 0);   // Flavors not required for Key 
  SysFreeString(Key);

  // No longer need the qualifier set for "Index"
  pQual->Release();     
  VariantClear(&v);

  // Create other properties.
  // ============================
  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"<default>");
  BSTR OtherProp = SysAllocString(L"OtherInfo");
  pNewClass->Put(OtherProp, 0, &v, CIM_STRING);
  SysFreeString(OtherProp);
  VariantClear(&v);

  OtherProp = SysAllocString(L"IntVal");
  pNewClass->Put(OtherProp, 0, NULL, CIM_SINT32); // NULL is default
  SysFreeString(OtherProp);
  
  // Register the class with WMI
  // ============================
  hRes = pSvc->PutClass(pNewClass, 0, pCtx, &pResult);
  pNewClass->Release();
}
```



## <a name="related-topics"></a><span data-ttu-id="b1810-180">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b1810-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1810-181">Crear una clase</span><span class="sxs-lookup"><span data-stu-id="b1810-181">Creating a Class</span></span>](creating-a-class.md)
</dt> </dl>

 

 



