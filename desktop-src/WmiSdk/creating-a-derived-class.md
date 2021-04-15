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
# <a name="creating-a-wmi-derived-class"></a>Crear una clase derivada de WMI

La creación de una clase derivada en WMI es muy similar a la creación de una clase base. Al igual que con una clase base, primero debe definir la clase derivada y, después, registrar la clase derivada con WMI. La principal diferencia es que primero debe localizar la clase primaria de la que desea derivar. Para obtener más información, consulte [escribir un proveedor de clases](writing-a-class-provider.md) y [escribir un proveedor de instancias](writing-an-instance-provider.md).

La manera recomendada de crear clases para un proveedor es en archivos de Managed Object Format (MOF). Varias clases derivadas que se relacionan entre sí deben agruparse en un archivo MOF, junto con las clases base de las que derivan propiedades o métodos. Si coloca cada clase en un archivo MOF independiente, cada archivo se debe compilar antes de que el proveedor pueda funcionar correctamente.

Después de crear la clase, debe eliminar todas las instancias de la clase antes de poder realizar cualquiera de las siguientes actividades en la clase derivada:

-   Cambie la clase primaria de la clase derivada.
-   Agregar o quitar propiedades.
-   Cambiar los tipos de propiedad.
-   Agregue o quite calificadores [**clave**](key-qualifier.md) o **indexados** .
-   Agregue o quite los calificadores [**Singleton**](standard-wmi-qualifiers.md), **dinámico** o [**abstracto**](standard-qualifiers.md) .

> [!Note]  
> Para agregar, quitar o modificar una propiedad o un calificador, llame a [**IWbemServices::P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass) o [**SWbemObject \_ . put**](swbemobject-put-.md) y establezca el parámetro de marca en "Force Mode". El calificador [**abstract**](standard-qualifiers.md) solo se puede usar si la clase primaria es abstracta.

 

Cuando declare la clase derivada, observe las siguientes reglas y restricciones:

-   La clase primaria de la clase derivada debe existir ya.

    La declaración de la clase primaria puede aparecer en el mismo archivo MOF que la clase derivada o en un archivo diferente. Si se desconoce la clase primaria, el compilador genera un error en tiempo de ejecución.

-   Una clase derivada solo puede tener una clase primaria.

    WMI no admite la herencia múltiple. Sin embargo, una clase primaria puede tener muchas clases derivadas.

-   Puede definir índices para las clases derivadas, pero WMI no utiliza estos índices.

    Por consiguiente, si se especifica un índice en una clase derivada, no se mejora el rendimiento de las consultas de las instancias de la clase derivada. Puede mejorar el rendimiento de una consulta en una clase derivada especificando las propiedades indizadas de la clase primaria de la clase derivada.

-   Las definiciones de clases derivadas pueden ser más complejas y pueden incluir características como alias, calificadores y sabores de calificador.

    Para obtener más información, vea [crear un alias](creating-an-alias.md) y [Agregar un calificador](adding-a-qualifier.md).

-   Si desea cambiar un calificador, cambiar el valor predeterminado de una propiedad de clase base, o escribir de forma más segura una propiedad de referencia o de objeto incrustado de una clase base, debe declarar de nuevo toda la clase base.
-   El número máximo de propiedades que puede definir en una clase WMI es 1024.

> [!Note]  
> Las clases no se pueden cambiar durante la ejecución de proveedores. Debe detener la actividad, cambiar la clase y, a continuación, reiniciar el servicio de administración de Windows. Actualmente no es posible detectar un cambio de clase.

 

Como con la clase base, el uso más común de esta técnica será de las aplicaciones cliente. Sin embargo, un proveedor también puede crear una clase derivada. Para obtener más información, vea [crear una clase base](creating-a-base-class.md) y [escribir un proveedor de clases](writing-a-class-provider.md).

El ejemplo de código de este tema requiere la siguiente \# instrucción include para compilar correctamente.


```C++
#include <wbemidl.h>
```



En el procedimiento siguiente se describe cómo crear una clase derivada mediante C++.

**Para crear una clase derivada con C++**

1.  Busque la clase base con una llamada a [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).

    En el ejemplo de código siguiente se muestra cómo buscar la clase base de ejemplo.

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

    

2.  Cree un objeto derivado de la clase base con una llamada a [**IWbemClassObject:: SpawnDerivedClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawnderivedclass).

    En el ejemplo de código siguiente se muestra cómo crear un objeto de clase derivada.

    ```C++
    pExampleClass->SpawnDerivedClass(0, &pNewDerivedClass);
    pExampleClass->Release();  // Don't need the parent class any more
    ```

    

3.  Establezca un nombre para la clase estableciendo la propiedad System de **\_ \_ clase** con una llamada al método [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .

    En el ejemplo de código siguiente se muestra cómo asignar un nombre a la clase derivada.

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

    

4.  Cree propiedades adicionales con [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    En el ejemplo de código siguiente se muestra cómo crear propiedades adicionales.

    ```C++
    BSTR OtherProp = SysAllocString(L"OtherInfo2");
    pNewDerivedClass->Put(OtherProp, 0, NULL, CIM_STRING); 
    SysFreeString(OtherProp);
    ```

    

5.  Guarde la nueva clase llamando a [**IWbemServices::P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).

    En el ejemplo de código siguiente se muestra cómo guardar la nueva clase derivada.

    ```C++
    hRes = pSvc->PutClass(pNewDerivedClass, 0, pCtx, &pResult);
    pNewDerivedClass->Release();
    ```

    

En el ejemplo de código siguiente se combinan los ejemplos de código descritos en el procedimiento anterior para describir cómo crear una clase derivada mediante la API de WMI.


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



En el procedimiento siguiente se describe cómo definir una clase derivada mediante código MOF.

**Para definir una clase derivada mediante código MOF**

1.  Defina la clase derivada con la palabra clave **Class** , seguida del nombre de la clase derivada y el nombre de la clase primaria separados por dos puntos.

    En el ejemplo de código siguiente se describe una implementación de una clase derivada.

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

2.  Cuando haya finalizado, compile el código MOF con el compilador MOF.

    Para obtener más información, vea [compilar archivos MOF](compiling-mof-files.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una clase](creating-a-class.md)
</dt> </dl>

 

 



