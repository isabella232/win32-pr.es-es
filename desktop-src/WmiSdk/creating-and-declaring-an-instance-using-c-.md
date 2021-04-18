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
# <a name="creating-and-declaring-an-instance-using-c"></a>Crear y declarar una instancia con C++

Puede crear una instancia de en C++ a través de la interfaz [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .

Los ejemplos de código de este tema requieren la siguiente \# instrucción include para compilar correctamente.


```C++
#include <wbemidl.h>
```



En el procedimiento siguiente se describe cómo crear una instancia de una clase existente.

**Para crear una instancia de una clase existente**

1.  Recupere la definición de la clase existente mediante una llamada a los métodos [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .

    En el ejemplo de código siguiente se muestra cómo usar los métodos [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) y [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) para obtener un puntero a la interfaz [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) que proporciona acceso a la definición de clase.

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

    

2.  Cree la nueva instancia de llamando al método [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) .

    En el ejemplo de código siguiente se muestra cómo crear una nueva instancia de y, a continuación, liberar la clase.

    ```C++
    pExampleClass->SpawnInstance(0, &pNewInstance);
    pExampleClass->Release();  // Don't need the class any more
    ```

    

3.  Establezca los valores de las propiedades que no hereden los valores definidos para la clase llamando al método [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .

    Cada instancia de una clase hereda todas las propiedades que se definen para la clase. Sin embargo, puede especificar diferentes valores de propiedad si lo desea.

    Si la clase existente tiene una propiedad de clave, debe establecer la propiedad en **null** o en un valor único garantizado. Si establece la clave en **null** y la clave es una cadena, [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) o [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) genera internamente y asigna un GUID a la clave. De este modo, si se especifica **null** para una propiedad de clave, se permite crear una instancia única que no sobrescribirá ninguna instancia anterior.

    En el ejemplo de código siguiente se muestra cómo establecer el valor de la propiedad de [**Índice**](swbemrefreshableitem-index.md) de la clase de instancia de ejemplo.

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

    

4.  Establezca los valores de los calificadores pertinentes a través de una llamada a [**IWbemClassObject:: GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset).

    El método [**GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset) devuelve un puntero a una interfaz [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) , que usa para tener acceso a los calificadores de una clase o instancia. Puede especificar valores diferentes para un calificador definido para la clase si el tipo de calificador de clase es **EnableOverride**. No se puede modificar ni eliminar un calificador de clase con el tipo de valor establecido en **DisableOverride**. Para obtener más información, vea [tipos de calificador](qualifier-flavors.md).

    Como opción, también puede definir calificadores adicionales para la clase de instancia. Puede definir calificadores adicionales para la propiedad de instancia o instancia que no es necesario que aparezcan en la declaración de clase.

5.  Guarde la instancia de llamando al método [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) o [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) .

    WMI guarda la instancia en el espacio de nombres WMI actual. Como tal, la ruta de acceso completa de la instancia depende del espacio de nombres, que suele ser la raíz \\ predeterminada. En este ejemplo de código, el nombre completo de la ruta de acceso sería \\ \\ . \\ raíz \\ predeterminada: example. index = "IX100".

    En el ejemplo de código siguiente se muestra cómo guardar una instancia de.

    ```C++
        hRes = pSvc->PutInstance(pNewInstance, 0, pCtx, &pResult);
        pNewInstance->Release();
    ```

    

Al guardar la instancia en WMI, se bloquean algunas de las propiedades de la instancia.

En concreto, no puede realizar ninguna de las siguientes operaciones a través de la API de WMI después de que exista una instancia dentro de la infraestructura de WMI:

-   Cambie la clase primaria de la clase a la que pertenece la instancia.
-   Agregar o quitar propiedades.
-   Cambiar los tipos de propiedad.
-   Agregue o quite calificadores [**clave**](standard-qualifiers.md) o **indexados** .
-   Agregue o quite los calificadores [**Singleton**](standard-wmi-qualifiers.md), **dinámico** o [**abstracto**](standard-qualifiers.md) .

En el ejemplo de código siguiente se combinan los ejemplos de código descritos en el procedimiento anterior para mostrar cómo crear una instancia de mediante la API de WMI.


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



 

 



