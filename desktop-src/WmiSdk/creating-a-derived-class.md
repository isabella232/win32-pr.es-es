---
description: La creación de una clase derivada en WMI es muy similar a la creación de una clase base. Al igual que con una clase base, primero debe definir la clase derivada y, después, registrar la clase derivada con WMI.
ms.assetid: 8dd483b8-8bc2-4a5c-b981-6c2ffaccdb95
ms.tgt_platform: multiple
title: Crear una clase derivada de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b65079d206cb7a0a490622018f6d2e2df98867d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715842"
---
# <a name="creating-a-wmi-derived-class"></a><span data-ttu-id="e2e5d-104">Crear una clase derivada de WMI</span><span class="sxs-lookup"><span data-stu-id="e2e5d-104">Creating a WMI Derived Class</span></span>

<span data-ttu-id="e2e5d-105">La creación de una clase derivada en WMI es muy similar a la creación de una clase base.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-105">Creating a derived class in WMI is very similar to creating a base class.</span></span> <span data-ttu-id="e2e5d-106">Al igual que con una clase base, primero debe definir la clase derivada y, después, registrar la clase derivada con WMI.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-106">As with a base class, you must first define the derived class and then register the derived class with WMI.</span></span> <span data-ttu-id="e2e5d-107">La principal diferencia es que primero debe localizar la clase primaria de la que desea derivar.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-107">The main difference is that you must first locate the parent class from which you wish to derive.</span></span> <span data-ttu-id="e2e5d-108">Para obtener más información, consulte [escribir un proveedor de clases](writing-a-class-provider.md) y [escribir un proveedor de instancias](writing-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e2e5d-108">For more information, see [Writing a Class Provider](writing-a-class-provider.md) and [Writing an Instance Provider](writing-an-instance-provider.md).</span></span>

<span data-ttu-id="e2e5d-109">La manera recomendada de crear clases para un proveedor es en archivos de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="e2e5d-109">The recommended way to create classes for a provider is in Managed Object Format (MOF) files.</span></span> <span data-ttu-id="e2e5d-110">Varias clases derivadas que se relacionan entre sí deben agruparse en un archivo MOF, junto con las clases base de las que derivan propiedades o métodos.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-110">Several derived classes that are related to each other should be grouped into a MOF file, along with any base classes from which they derive properties or methods.</span></span> <span data-ttu-id="e2e5d-111">Si coloca cada clase en un archivo MOF independiente, cada archivo se debe compilar antes de que el proveedor pueda funcionar correctamente.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-111">If you place each class in a separate MOF file then each file must be compiled before the provider can work properly.</span></span>

<span data-ttu-id="e2e5d-112">Después de crear la clase, debe eliminar todas las instancias de la clase antes de poder realizar cualquiera de las siguientes actividades en la clase derivada:</span><span class="sxs-lookup"><span data-stu-id="e2e5d-112">After you create your class, you must delete all instances of your class before you can perform any of the following activities on your derived class:</span></span>

-   <span data-ttu-id="e2e5d-113">Cambie la clase primaria de la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-113">Change the parent class of your derived class.</span></span>
-   <span data-ttu-id="e2e5d-114">Agregar o quitar propiedades.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-114">Add or remove properties.</span></span>
-   <span data-ttu-id="e2e5d-115">Cambiar los tipos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-115">Change property types.</span></span>
-   <span data-ttu-id="e2e5d-116">Agregue o quite calificadores [**clave**](key-qualifier.md) o **indexados** .</span><span class="sxs-lookup"><span data-stu-id="e2e5d-116">Add or remove [**Key**](key-qualifier.md) or **Indexed** qualifiers.</span></span>
-   <span data-ttu-id="e2e5d-117">Agregue o quite los calificadores [**Singleton**](standard-wmi-qualifiers.md), **dinámico** o [**abstracto**](standard-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="e2e5d-117">Add or remove [**Singleton**](standard-wmi-qualifiers.md), **Dynamic**, or [**Abstract**](standard-qualifiers.md) qualifiers.</span></span>

> [!Note]  
> <span data-ttu-id="e2e5d-118">Para agregar, quitar o modificar una propiedad o un calificador, llame a [**IWbemServices::P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass) o [**SWbemObject \_ . put**](swbemobject-put-.md) y establezca el parámetro de marca en "Force Mode".</span><span class="sxs-lookup"><span data-stu-id="e2e5d-118">To add, remove, or modify a property or qualifier, call [**IWbemServices::PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass) or [**SWbemObject.Put\_**](swbemobject-put-.md) and set the flag parameter to "force mode".</span></span> <span data-ttu-id="e2e5d-119">El calificador [**abstract**](standard-qualifiers.md) solo se puede usar si la clase primaria es abstracta.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-119">The [**Abstract**](standard-qualifiers.md) qualifier can be used only if the parent class is abstract.</span></span>

 

<span data-ttu-id="e2e5d-120">Cuando declare la clase derivada, observe las siguientes reglas y restricciones:</span><span class="sxs-lookup"><span data-stu-id="e2e5d-120">When you declare your derived class, observe the following rules and restrictions:</span></span>

-   <span data-ttu-id="e2e5d-121">La clase primaria de la clase derivada debe existir ya.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-121">The parent class of the derived class must already exist.</span></span>

    <span data-ttu-id="e2e5d-122">La declaración de la clase primaria puede aparecer en el mismo archivo MOF que la clase derivada o en un archivo diferente.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-122">The declaration of the parent class can appear in the same MOF file as the derived class or in a different file.</span></span> <span data-ttu-id="e2e5d-123">Si se desconoce la clase primaria, el compilador genera un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-123">If the parent class is unknown, the compiler generates a run-time error.</span></span>

-   <span data-ttu-id="e2e5d-124">Una clase derivada solo puede tener una clase primaria.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-124">A derived class can have only a single parent class.</span></span>

    <span data-ttu-id="e2e5d-125">WMI no admite la herencia múltiple.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-125">WMI does not support multiple inheritance.</span></span> <span data-ttu-id="e2e5d-126">Sin embargo, una clase primaria puede tener muchas clases derivadas.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-126">However, a parent class can have many derived classes.</span></span>

-   <span data-ttu-id="e2e5d-127">Puede definir índices para las clases derivadas, pero WMI no utiliza estos índices.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-127">You can define indices for derived classes, but WMI does not use these indices.</span></span>

    <span data-ttu-id="e2e5d-128">Por consiguiente, si se especifica un índice en una clase derivada, no se mejora el rendimiento de las consultas de las instancias de la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-128">Therefore, specifying an index on a derived class does not improve the performance of queries for instances of the derived class.</span></span> <span data-ttu-id="e2e5d-129">Puede mejorar el rendimiento de una consulta en una clase derivada especificando las propiedades indizadas de la clase primaria de la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-129">You can improve the performance of a query on a derived class by specifying indexed properties for the parent class of the derived class.</span></span>

-   <span data-ttu-id="e2e5d-130">Las definiciones de clases derivadas pueden ser más complejas y pueden incluir características como alias, calificadores y sabores de calificador.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-130">Derived class definitions can be more complex, and can include such features as aliases, qualifiers, and qualifier flavors.</span></span>

    <span data-ttu-id="e2e5d-131">Para obtener más información, vea [crear un alias](creating-an-alias.md) y [Agregar un calificador](adding-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="e2e5d-131">For more information, see [Creating an Alias](creating-an-alias.md) and [Adding a Qualifier](adding-a-qualifier.md).</span></span>

-   <span data-ttu-id="e2e5d-132">Si desea cambiar un calificador, cambiar el valor predeterminado de una propiedad de clase base, o escribir de forma más segura una propiedad de referencia o de objeto incrustado de una clase base, debe declarar de nuevo toda la clase base.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-132">If you wish to change a qualifier, change the default value of a base class property, or more strongly type a reference or embedded object property of a base class, you must declare the entire base class again.</span></span>
-   <span data-ttu-id="e2e5d-133">El número máximo de propiedades que puede definir en una clase WMI es 1024.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-133">The maximum number of properties you can define in a WMI class is 1024.</span></span>

> [!Note]  
> <span data-ttu-id="e2e5d-134">Las clases no se pueden cambiar durante la ejecución de proveedores.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-134">Classes cannot be changed during execution of providers.</span></span> <span data-ttu-id="e2e5d-135">Debe detener la actividad, cambiar la clase y, a continuación, reiniciar el servicio de administración de Windows.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-135">You must stop the activity, change the class, and then restart the Windows Management service.</span></span> <span data-ttu-id="e2e5d-136">Actualmente no es posible detectar un cambio de clase.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-136">Detecting a class change is currently not possible.</span></span>

 

<span data-ttu-id="e2e5d-137">Como con la clase base, el uso más común de esta técnica será de las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-137">As with the base class, the most common use of this technique will be by client applications.</span></span> <span data-ttu-id="e2e5d-138">Sin embargo, un proveedor también puede crear una clase derivada.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-138">However, a provider can also create a derived class.</span></span> <span data-ttu-id="e2e5d-139">Para obtener más información, vea [crear una clase base](creating-a-base-class.md) y [escribir un proveedor de clases](writing-a-class-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e2e5d-139">For more information, see [Creating a Base Class](creating-a-base-class.md) and [Writing a Class Provider](writing-a-class-provider.md).</span></span>

<span data-ttu-id="e2e5d-140">El ejemplo de código de este tema requiere la siguiente \# instrucción include para compilar correctamente.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-140">The code example in this topic requires the following \#include statement to compile correctly.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="e2e5d-141">En el procedimiento siguiente se describe cómo crear una clase derivada mediante C++.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-141">The following procedure describes how to create a derived class using C++.</span></span>

<span data-ttu-id="e2e5d-142">**Para crear una clase derivada con C++**</span><span class="sxs-lookup"><span data-stu-id="e2e5d-142">**To create a derived class using C++**</span></span>

1.  <span data-ttu-id="e2e5d-143">Busque la clase base con una llamada a [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="e2e5d-143">Locate the base class with a call to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>

    <span data-ttu-id="e2e5d-144">En el ejemplo de código siguiente se muestra cómo buscar la clase base de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-144">The following code example shows how to locate the Example base class.</span></span>

    ```C++
    // The pSv variable is of type IWbemServices *

    IWbemClassObject *pNewDerivedClass = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, &pExampleClass, &pResult);
    SysFreeString(PathToClass);
    ```

    

2.  <span data-ttu-id="e2e5d-145">Cree un objeto derivado de la clase base con una llamada a [**IWbemClassObject:: SpawnDerivedClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawnderivedclass).</span><span class="sxs-lookup"><span data-stu-id="e2e5d-145">Create a derived object from the base class with a call to [**IWbemClassObject::SpawnDerivedClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawnderivedclass).</span></span>

    <span data-ttu-id="e2e5d-146">En el ejemplo de código siguiente se muestra cómo crear un objeto de clase derivada.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-146">The following code example shows how to create a derived class object.</span></span>

    ```C++
    pExampleClass->SpawnDerivedClass(0, &pNewDerivedClass);
    pExampleClass->Release();  // Don't need the parent class any more
    ```

    

3.  <span data-ttu-id="e2e5d-147">Establezca un nombre para la clase estableciendo la propiedad System de **\_ \_ clase** con una llamada al método [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .</span><span class="sxs-lookup"><span data-stu-id="e2e5d-147">Establish a name for the class by setting the **\_\_CLASS** system property with a call to the [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) method.</span></span>

    <span data-ttu-id="e2e5d-148">En el ejemplo de código siguiente se muestra cómo asignar un nombre a la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-148">The following code example shows how to assign a name to the derived class.</span></span>

    ```C++
    VARIANT v;
    VariantInit(&v);

    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"Example2");
    BSTR Class = SysAllocString(L"__CLASS");
    pNewDerivedClass->Put(Class, 0, &v, 0);
    SysFreeString(Class);
    VariantClear(&v);
    ```

    

4.  <span data-ttu-id="e2e5d-149">Cree propiedades adicionales con [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="e2e5d-149">Create additional properties with [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="e2e5d-150">En el ejemplo de código siguiente se muestra cómo crear propiedades adicionales.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-150">The following code example shows how to create additional properties.</span></span>

    ```C++
    BSTR OtherProp = SysAllocString(L"OtherInfo2");
    pNewDerivedClass->Put(OtherProp, 0, NULL, CIM_STRING); 
    SysFreeString(OtherProp);
    ```

    

5.  <span data-ttu-id="e2e5d-151">Guarde la nueva clase llamando a [**IWbemServices::P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span><span class="sxs-lookup"><span data-stu-id="e2e5d-151">Save the new class by calling [**IWbemServices::PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span></span>

    <span data-ttu-id="e2e5d-152">En el ejemplo de código siguiente se muestra cómo guardar la nueva clase derivada.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-152">The following code example shows how to save the new derived class.</span></span>

    ```C++
    hRes = pSvc->PutClass(pNewDerivedClass, 0, pCtx, &pResult);
    pNewDerivedClass->Release();
    ```

    

<span data-ttu-id="e2e5d-153">En el ejemplo de código siguiente se combinan los ejemplos de código descritos en el procedimiento anterior para describir cómo crear una clase derivada mediante la API de WMI.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-153">The following code example combines the code examples discussed in the previous procedure to describe how to create a derived class using the WMI API.</span></span>


```C++
void CreateDerivedClass(IWbemServices *pSvc)
{
  IWbemClassObject *pNewDerivedClass = 0;
  IWbemClassObject *pExampleClass = 0;
  IWbemContext *pCtx = 0;
  IWbemCallResult *pResult = 0;

  BSTR PathToClass = SysAllocString(L"Example");
  HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
    &pExampleClass, &pResult);
  SysFreeString(PathToClass);

  if (hRes != 0)
    return;

  pExampleClass->SpawnDerivedClass(0, &pNewDerivedClass);
  pExampleClass->Release();  // The parent class is no longer needed

  VARIANT v;
  VariantInit(&v);

  // Create the class name.
  // =====================

  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"Example2");
  BSTR Class = SysAllocString(L"__CLASS");
  pNewDerivedClass->Put(Class, 0, &v, 0);
  SysFreeString(Class);
  VariantClear(&v);

  // Create another property.
  // =======================
  BSTR OtherProp = SysAllocString(L"OtherInfo2");
  // No default value
  pNewDerivedClass->Put(OtherProp, 0, NULL, CIM_STRING); 
  SysFreeString(OtherProp);
  
  // Register the class with WMI. 
  // ============================
  hRes = pSvc->PutClass(pNewDerivedClass, 0, pCtx, &pResult);
  pNewDerivedClass->Release();
}
```



<span data-ttu-id="e2e5d-154">En el procedimiento siguiente se describe cómo definir una clase derivada mediante código MOF.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-154">The following procedure describes how to define a derived class using MOF code.</span></span>

<span data-ttu-id="e2e5d-155">**Para definir una clase derivada mediante código MOF**</span><span class="sxs-lookup"><span data-stu-id="e2e5d-155">**To define a derived class using MOF code**</span></span>

1.  <span data-ttu-id="e2e5d-156">Defina la clase derivada con la palabra clave **Class** , seguida del nombre de la clase derivada y el nombre de la clase primaria separados por dos puntos.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-156">Define your derived class with the **Class** keyword, followed by the name of your derived class, and the name of the parent class separated by a colon.</span></span>

    <span data-ttu-id="e2e5d-157">En el ejemplo de código siguiente se describe una implementación de una clase derivada.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-157">The following code example describes an implementation of a derived class.</span></span>

    ``` syntax
    class MyClass 
    {
        [key] string   strProp;
        sint32   dwProp1;
        uint32       dwProp2;
    };

    class MyDerivedClass : MyClass
    {
        string   strDerivedProp;
        sint32   dwDerivedProp;
    };
    ```

2.  <span data-ttu-id="e2e5d-158">Cuando haya finalizado, compile el código MOF con el compilador MOF.</span><span class="sxs-lookup"><span data-stu-id="e2e5d-158">When complete, compile your MOF code with the MOF compiler.</span></span>

    <span data-ttu-id="e2e5d-159">Para obtener más información, vea [compilar archivos MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="e2e5d-159">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2e5d-160">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e2e5d-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2e5d-161">Crear una clase</span><span class="sxs-lookup"><span data-stu-id="e2e5d-161">Creating a Class</span></span>](creating-a-class.md)
</dt> </dl>

 

 



