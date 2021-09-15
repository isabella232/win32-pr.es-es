---
description: Puede crear una instancia en C++ a través de la interfaz IWbemServices.
ms.assetid: ee54c1ef-bc91-4771-8c11-9ee3aacd8112
ms.tgt_platform: multiple
title: Creación y declaración de una instancia mediante C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd316975c68625383a9d2a2d1fe2fc389d30494a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465779"
---
# <a name="creating-and-declaring-an-instance-using-c"></a>Creación y declaración de una instancia mediante C++

Puede crear una instancia en C++ a través de la [**interfaz IWbemServices.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)

Los ejemplos de código de este tema requieren que la \# siguiente instrucción include se compile correctamente.


```C++
#include <wbemidl.h>
```



En el procedimiento siguiente se describe cómo crear una instancia de una clase existente.

**Para crear una instancia de una clase existente**

1.  Recupere la definición de la clase existente llamando a los [**métodos IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices::GetObjectAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)

    En el ejemplo de código siguiente se muestra cómo usar los métodos [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) y [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) para obtener un puntero a la [**interfaz IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) que proporciona acceso a la definición de clase.

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

    

2.  Cree la nueva instancia llamando al [**método IWbemClassObject::SpawnInstance.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance)

    En el ejemplo de código siguiente se muestra cómo crear una nueva instancia y, a continuación, liberar la clase .

    ```C++
    pExampleClass->SpawnInstance(0, &pNewInstance);
    pExampleClass->Release();  // Don't need the class any more
    ```

    

3.  Establezca valores para cualquier propiedad que no herede los valores definidos para la clase llamando al método [**IWbemClassObject::P ut.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)

    Cada instancia de una clase hereda todas las propiedades definidas para la clase. Sin embargo, puede especificar valores de propiedad diferentes si lo desea.

    Si la clase existente tiene una propiedad de clave, debe establecer la propiedad en **NULL** o en un valor único garantizado. Si establece la clave en **NULL** y la clave es una cadena, [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) o [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) genera internamente y asigna un GUID a la clave. De este modo, especificar **NULL para** una propiedad de clave permite crear una instancia única que no sobrescribirá ninguna instancia anterior.

    En el ejemplo de código siguiente se muestra cómo establecer el [**valor de la propiedad Index**](swbemrefreshableitem-index.md) de la clase de instancia de ejemplo.

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

    

4.  Establezca los valores de los calificadores pertinentes mediante una llamada a [**IWbemClassObject::GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset).

    El [**método GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset) devuelve un puntero a una interfaz [**IWbemQualifierSet,**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) que usa para tener acceso a los calificadores de una clase o instancia. Puede especificar valores diferentes para un calificador definido para la clase si el tipo de calificador de clase **es EnableOverride**. No se puede modificar ni eliminar un calificador de clase con el tipo establecido en **DisableOverride**. Para obtener más información, vea [Qualifier Flavors](qualifier-flavors.md).

    Como opción, también puede definir calificadores adicionales para la clase de instancia. Puede definir calificadores adicionales para la propiedad de instancia o instancia que no es necesario que aparezcan en la declaración de clase.

5.  Guarde la instancia llamando al método [**IWbemServices::P utInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) [**o IWbemServices::P utInstanceAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)

    WMI guarda la instancia en el espacio de nombres WMI actual. Por lo tanto, la ruta de acceso completa de la instancia depende del espacio de nombres , que normalmente es el valor \\ predeterminado raíz. En este ejemplo de código, el nombre completo de la ruta de acceso sería \\ \\ . \\ root \\ default:Example.Index="IX100".

    En el ejemplo de código siguiente se muestra cómo guardar una instancia de .

    ```C++
        hRes = pSvc->PutInstance(pNewInstance, 0, pCtx, &pResult);
        pNewInstance->Release();
    ```

    

Al guardar la instancia en WMI, se bloquean varias de las propiedades de la instancia.

En concreto, no puede realizar ninguna de las siguientes operaciones a través de la API de WMI después de que exista una instancia dentro de la infraestructura WMI:

-   Cambie la clase primaria de la clase a la que pertenece la instancia.
-   Agregar o quitar propiedades.
-   Cambie los tipos de propiedad.
-   Agregue o quite [**calificadores**](standard-qualifiers.md) key **o indexed.**
-   Agregue o quite [**calificadores Singleton,**](standard-wmi-qualifiers.md) **Dynamic** [**o Abstract.**](standard-qualifiers.md)

En el ejemplo de código siguiente se combinan los ejemplos de código que se han descrito en el procedimiento anterior para mostrar cómo crear una instancia mediante la API wmi.


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



 

 



