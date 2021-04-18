---
description: Puede crear una instancia de en C++ a través de la interfaz IWbemServices.
ms.assetid: ee54c1ef-bc91-4771-8c11-9ee3aacd8112
ms.tgt_platform: multiple
title: Crear y declarar una instancia con C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd316975c68625383a9d2a2d1fe2fc389d30494a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706932"
---
# <a name="creating-and-declaring-an-instance-using-c"></a><span data-ttu-id="1a74f-103">Crear y declarar una instancia con C++</span><span class="sxs-lookup"><span data-stu-id="1a74f-103">Creating and Declaring an Instance Using C++</span></span>

<span data-ttu-id="1a74f-104">Puede crear una instancia de en C++ a través de la interfaz [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="1a74f-104">You can create an instance in C++ through the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span>

<span data-ttu-id="1a74f-105">Los ejemplos de código de este tema requieren la siguiente \# instrucción include para compilar correctamente.</span><span class="sxs-lookup"><span data-stu-id="1a74f-105">The code examples in this topic require the following \#include statement to compile correctly.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="1a74f-106">En el procedimiento siguiente se describe cómo crear una instancia de una clase existente.</span><span class="sxs-lookup"><span data-stu-id="1a74f-106">The following procedure describes how to create an instance of an existing class.</span></span>

<span data-ttu-id="1a74f-107">**Para crear una instancia de una clase existente**</span><span class="sxs-lookup"><span data-stu-id="1a74f-107">**To create an instance of an existing class**</span></span>

1.  <span data-ttu-id="1a74f-108">Recupere la definición de la clase existente mediante una llamada a los métodos [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .</span><span class="sxs-lookup"><span data-stu-id="1a74f-108">Retrieve the definition of the existing class by calling the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) methods.</span></span>

    <span data-ttu-id="1a74f-109">En el ejemplo de código siguiente se muestra cómo usar los métodos [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) y [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) para obtener un puntero a la interfaz [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) que proporciona acceso a la definición de clase.</span><span class="sxs-lookup"><span data-stu-id="1a74f-109">The following code example shows how to use the [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) and [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) methods to get a pointer to the [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) interface that provides access to the class definition.</span></span>

    ```C++
    // The pSv variable is of type IWbemServices *

    IWbemClassObject *pNewInstance = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
                  &pExampleClass, &pResult);
    SysFreeString(PathToClass);
    ```

    

2.  <span data-ttu-id="1a74f-110">Cree la nueva instancia de llamando al método [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) .</span><span class="sxs-lookup"><span data-stu-id="1a74f-110">Create the new instance by calling the [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) method.</span></span>

    <span data-ttu-id="1a74f-111">En el ejemplo de código siguiente se muestra cómo crear una nueva instancia de y, a continuación, liberar la clase.</span><span class="sxs-lookup"><span data-stu-id="1a74f-111">The following code example shows how to create a new instance and then release the class.</span></span>

    ```C++
    pExampleClass->SpawnInstance(0, &pNewInstance);
    pExampleClass->Release();  // Don't need the class any more
    ```

    

3.  <span data-ttu-id="1a74f-112">Establezca los valores de las propiedades que no hereden los valores definidos para la clase llamando al método [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .</span><span class="sxs-lookup"><span data-stu-id="1a74f-112">Set values for any properties that do not inherit the values defined for the class by calling the [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) method.</span></span>

    <span data-ttu-id="1a74f-113">Cada instancia de una clase hereda todas las propiedades que se definen para la clase.</span><span class="sxs-lookup"><span data-stu-id="1a74f-113">Each instance of a class inherits all of the properties that are defined for the class.</span></span> <span data-ttu-id="1a74f-114">Sin embargo, puede especificar diferentes valores de propiedad si lo desea.</span><span class="sxs-lookup"><span data-stu-id="1a74f-114">However, you can specify different property values if you choose.</span></span>

    <span data-ttu-id="1a74f-115">Si la clase existente tiene una propiedad de clave, debe establecer la propiedad en **null** o en un valor único garantizado.</span><span class="sxs-lookup"><span data-stu-id="1a74f-115">If the existing class has a key property, you should set the property either to **NULL** or a guaranteed unique value.</span></span> <span data-ttu-id="1a74f-116">Si establece la clave en **null** y la clave es una cadena, [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) o [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) genera internamente y asigna un GUID a la clave.</span><span class="sxs-lookup"><span data-stu-id="1a74f-116">If you set the key to **NULL** and the key is a string, then [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) or [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) internally generates and assigns a GUID to the key.</span></span> <span data-ttu-id="1a74f-117">De este modo, si se especifica **null** para una propiedad de clave, se permite crear una instancia única que no sobrescribirá ninguna instancia anterior.</span><span class="sxs-lookup"><span data-stu-id="1a74f-117">This way, specifying **NULL** for a key property lets you create a unique instance that will not overwrite any previous instance.</span></span>

    <span data-ttu-id="1a74f-118">En el ejemplo de código siguiente se muestra cómo establecer el valor de la propiedad de [**Índice**](swbemrefreshableitem-index.md) de la clase de instancia de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="1a74f-118">The following code example shows how to set the [**Index**](swbemrefreshableitem-index.md) property value of the example instance class.</span></span>

    ```C++
    VARIANT v;
    VariantInit(&v);

    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"IX100");

    BSTR KeyProp = SysAllocString(L"Index");
    pNewInstance->Put(KeyProp, 0, &v, 0);
    SysFreeString(KeyProp);
    VariantClear(&v);
    ```

    

4.  <span data-ttu-id="1a74f-119">Establezca los valores de los calificadores pertinentes a través de una llamada a [**IWbemClassObject:: GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset).</span><span class="sxs-lookup"><span data-stu-id="1a74f-119">Set the values for any relevant qualifiers through a call to [**IWbemClassObject::GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset).</span></span>

    <span data-ttu-id="1a74f-120">El método [**GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset) devuelve un puntero a una interfaz [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) , que usa para tener acceso a los calificadores de una clase o instancia.</span><span class="sxs-lookup"><span data-stu-id="1a74f-120">The [**GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset) method returns a pointer to an [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) interface, which use to access the qualifiers for a class or instance.</span></span> <span data-ttu-id="1a74f-121">Puede especificar valores diferentes para un calificador definido para la clase si el tipo de calificador de clase es **EnableOverride**.</span><span class="sxs-lookup"><span data-stu-id="1a74f-121">You can specify different values for a qualifier defined for the class if the class qualifier flavor is **EnableOverride**.</span></span> <span data-ttu-id="1a74f-122">No se puede modificar ni eliminar un calificador de clase con el tipo de valor establecido en **DisableOverride**.</span><span class="sxs-lookup"><span data-stu-id="1a74f-122">You cannot modify or delete a class qualifier with the flavor set to **DisableOverride**.</span></span> <span data-ttu-id="1a74f-123">Para obtener más información, vea [tipos de calificador](qualifier-flavors.md).</span><span class="sxs-lookup"><span data-stu-id="1a74f-123">For more information, see [Qualifier Flavors](qualifier-flavors.md).</span></span>

    <span data-ttu-id="1a74f-124">Como opción, también puede definir calificadores adicionales para la clase de instancia.</span><span class="sxs-lookup"><span data-stu-id="1a74f-124">As an option, you can also define additional qualifiers for your instance class.</span></span> <span data-ttu-id="1a74f-125">Puede definir calificadores adicionales para la propiedad de instancia o instancia que no es necesario que aparezcan en la declaración de clase.</span><span class="sxs-lookup"><span data-stu-id="1a74f-125">You can define additional qualifiers for the instance or instance property which do not need to appear in the class declaration.</span></span>

5.  <span data-ttu-id="1a74f-126">Guarde la instancia de llamando al método [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) o [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) .</span><span class="sxs-lookup"><span data-stu-id="1a74f-126">Save the instance by calling the [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) method.</span></span>

    <span data-ttu-id="1a74f-127">WMI guarda la instancia en el espacio de nombres WMI actual.</span><span class="sxs-lookup"><span data-stu-id="1a74f-127">WMI saves the instance in the current WMI namespace.</span></span> <span data-ttu-id="1a74f-128">Como tal, la ruta de acceso completa de la instancia depende del espacio de nombres, que suele ser la raíz \\ predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1a74f-128">As such, the full path of the instance is dependent on the namespace, which is typically root\\default.</span></span> <span data-ttu-id="1a74f-129">En este ejemplo de código, el nombre completo de la ruta de acceso sería \\ \\ . \\ raíz \\ predeterminada: example. index = "IX100".</span><span class="sxs-lookup"><span data-stu-id="1a74f-129">For this code example, the full path name would be \\\\.\\root\\default:Example.Index="IX100".</span></span>

    <span data-ttu-id="1a74f-130">En el ejemplo de código siguiente se muestra cómo guardar una instancia de.</span><span class="sxs-lookup"><span data-stu-id="1a74f-130">The following code example shows how to save an instance.</span></span>

    ```C++
        hRes = pSvc->PutInstance(pNewInstance, 0, pCtx, &pResult);
        pNewInstance->Release();
    ```

    

<span data-ttu-id="1a74f-131">Al guardar la instancia en WMI, se bloquean algunas de las propiedades de la instancia.</span><span class="sxs-lookup"><span data-stu-id="1a74f-131">Saving the instance to WMI locks down several of the properties of the instance.</span></span>

<span data-ttu-id="1a74f-132">En concreto, no puede realizar ninguna de las siguientes operaciones a través de la API de WMI después de que exista una instancia dentro de la infraestructura de WMI:</span><span class="sxs-lookup"><span data-stu-id="1a74f-132">Specifically, you cannot perform any of the following operations through the WMI API after an instance exists within the WMI infrastructure:</span></span>

-   <span data-ttu-id="1a74f-133">Cambie la clase primaria de la clase a la que pertenece la instancia.</span><span class="sxs-lookup"><span data-stu-id="1a74f-133">Change the parent class of the class to which the instance belongs.</span></span>
-   <span data-ttu-id="1a74f-134">Agregar o quitar propiedades.</span><span class="sxs-lookup"><span data-stu-id="1a74f-134">Add or remove properties.</span></span>
-   <span data-ttu-id="1a74f-135">Cambiar los tipos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="1a74f-135">Change property types.</span></span>
-   <span data-ttu-id="1a74f-136">Agregue o quite calificadores [**clave**](standard-qualifiers.md) o **indexados** .</span><span class="sxs-lookup"><span data-stu-id="1a74f-136">Add or remove [**Key**](standard-qualifiers.md) or **Indexed** qualifiers.</span></span>
-   <span data-ttu-id="1a74f-137">Agregue o quite los calificadores [**Singleton**](standard-wmi-qualifiers.md), **dinámico** o [**abstracto**](standard-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="1a74f-137">Add or remove [**Singleton**](standard-wmi-qualifiers.md), **Dynamic**, or [**Abstract**](standard-qualifiers.md) qualifiers.</span></span>

<span data-ttu-id="1a74f-138">En el ejemplo de código siguiente se combinan los ejemplos de código descritos en el procedimiento anterior para mostrar cómo crear una instancia de mediante la API de WMI.</span><span class="sxs-lookup"><span data-stu-id="1a74f-138">The following code example combines the code examples discussed in the previous procedure to show how to create an instance using the WMI API.</span></span>


```C++
void CreateInstance (IWbemServices *pSvc)
{
    IWbemClassObject *pNewInstance = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    // Get the class definition.
    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
                 &pExampleClass, &pResult);
    SysFreeString(PathToClass);

    if (hRes != 0)
       return;

    // Create a new instance.
    pExampleClass->SpawnInstance(0, &pNewInstance);
    pExampleClass->Release();  // Don't need the class any more

    VARIANT v;
    VariantInit(&v);

    // Set the Index property (the key).
    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"IX100");

    BSTR KeyProp = SysAllocString(L"Index");
    pNewInstance->Put(KeyProp, 0, &v, 0);
    SysFreeString(KeyProp);
    VariantClear(&v);

    // Set the IntVal property.
    V_VT(&v) = VT_I4;
    V_I4(&v) = 1001;  
    
    BSTR Prop = SysAllocString(L"IntVal");
    pNewInstance->Put(Prop, 0, &v, 0);
    SysFreeString(Prop);
    VariantClear(&v);    
    
    // Other properties acquire the 'default' value specified
    // in the class definition unless otherwise modified here.

    // Write the instance to WMI. 
    hRes = pSvc->PutInstance(pNewInstance, 0, pCtx, &pResult);
    pNewInstance->Release();
}
```



 

 



