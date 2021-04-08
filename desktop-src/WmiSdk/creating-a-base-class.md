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
# <a name="creating-a-wmi-base-class"></a>Crear una clase base de WMI

La manera recomendada de crear una nueva clase base de WMI para un proveedor WMI es en un archivo Managed Object Format (MOF). También puede crear una clase base mediante la [API com para WMI](com-api-for-wmi.md). Aunque se puede crear una clase base o derivada en un script, sin que un proveedor proporcione datos a la clase y sus subclases, la clase no es útil.

En este tema se describen las siguientes secciones:

-   [Crear una clase base mediante MOF](#creating-a-base-class-using-mof)
-   [Crear una clase base con C++](#creating-a-base-class-with-c)
-   [Temas relacionados](#related-topics)

## <a name="creating-a-base-class-using-mof"></a>Crear una clase base mediante MOF

Las clases WMI suelen basarse en la herencia. Antes de crear una clase base, consulte las clases de Modelo de información común (CIM) disponibles en el equipo de la tarea de administración distribuida ([DMTF](https://www.dmtf.org/)).

Si muchas clases derivadas van a utilizar las mismas propiedades, coloque estas propiedades y métodos en la clase base. El número máximo de propiedades que puede definir en una clase WMI es 1024.

Al crear una clase base, observe la siguiente lista de instrucciones para los nombres de clase:

-   Use mayúsculas y minúsculas.
-   Comience un nombre de clase con una letra.
-   No utilice un carácter de subrayado inicial o final.
-   Defina todos los caracteres restantes como letras, dígitos o caracteres de subrayado.
-   Use una Convención de nomenclatura coherente.

    Aunque no es necesario, una buena Convención de nomenclatura para una clase son dos componentes Unidos por un carácter de subrayado. Cuando sea posible, un nombre de proveedor debe componer la primera mitad del nombre y un nombre de clase descriptivo debe ser la segunda parte.

> [!Note]  
> Las clases no se pueden cambiar durante la ejecución de proveedores. Debe detener la actividad, cambiar la clase y, a continuación, reiniciar el servicio de administración de Windows. Actualmente no es posible detectar un cambio de clase.

 

En MOF, cree una clase base asignándole un nombre con la palabra clave **Class** , pero no para indicar una clase primaria.

**Para crear una clase base mediante código MOF**

1.  Use la palabra clave **Class** con el nombre de la nueva clase, seguido de un par de llaves y un punto y coma. Agregue las propiedades y los métodos de la clase entre las llaves. Se proporciona el siguiente ejemplo de código.

    En el ejemplo de código siguiente se muestra cómo debe definirse una clase base.

    ``` syntax
    class MyClass_BaseDisk
    {
    };
    ```

    En el ejemplo de código siguiente se muestra una definición incorrecta de una clase base.

    ``` syntax
    class MyClass_BaseDisk : CIM_LogicalDisk
    {
    };
    ```

2.  Agregue los [*calificadores*](gloss-q.md) de clase antes de la palabra clave Class para modificar la forma en que se utiliza la clase. Coloque los calificadores entre corchetes. Para obtener más información acerca de los calificadores para modificar clases, vea [calificadores de WMI](wmi-qualifiers.md). Utilice el calificador **abstracto** para indicar que no se puede crear una instancia de esta clase directamente. Las clases abstractas se usan a menudo para definir las propiedades o los métodos que usarán varias clases derivadas. Para obtener más información, vea [crear una clase derivada](creating-a-derived-class.md).

    En el ejemplo de código siguiente se define la clase como abstracta y se define el proveedor que proporcionará los datos. El [*tipo*](gloss-f.md) de calificador **ToSubClass** indica que las clases derivadas heredan la información del calificador de **proveedor** .

    ``` syntax
    [Abstract, Provider("MyProvider") : ToSubClass]
    class MyClass_BaseDisk
    {
    };
    ```

3.  Agregue las propiedades y los métodos de la clase entre corchetes antes del nombre de la propiedad o del método. Para obtener más información, vea [Agregar una propiedad](adding-a-property.md) y [crear un método](creating-a-method.md). Puede modificar estas propiedades y métodos mediante calificadores MOF. Para obtener más información, consulte [Agregar un calificador](adding-a-qualifier.md).

    En el ejemplo de código siguiente se muestra cómo modificar propiedades y métodos con calificadores MOF.

    ``` syntax
    [read : ToSubClass, key : ToSubClass ] string DeviceID;
      [read : ToSubClass] uint32 State;
      [read : ToSubclass, write : ToSubClass] uint64 LimitUsers;
    ```

4.  Guarde el archivo MOF con la extensión. mof.
5.  Registre la clase con WMI ejecutando [**Mofcomp.exe**](mofcomp.md) en el archivo.

    **mofcomp.exe** *newmof. mof*

    Si no usa el modificador **-N** o el espacio de nombres pragma de comando de preprocesador \# [](pragma-namespace.md) para especificar un espacio de nombres, las clases MOF compiladas se almacenarán en el \\ espacio de nombres predeterminado raíz en el repositorio. Para obtener más información, consulte [**MOFCOMP**](mofcomp.md).

En el ejemplo de código siguiente se combinan los ejemplos de código MOF descritos en el procedimiento anterior y se muestra cómo crear una clase base en el \\ espacio de nombres root cimv2 mediante MOF.

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

Para obtener más información, vea [crear una clase derivada](creating-a-derived-class.md) para obtener un ejemplo de una clase dinámica derivada de esta clase base.

## <a name="creating-a-base-class-with-c"></a>Crear una clase base con C++

La creación de una clase base mediante la API de WMI es principalmente una serie de comandos Put que definen la clase y registran la clase en WMI. El propósito principal de esta API es permitir que las aplicaciones cliente creen clases base. Sin embargo, también puede tener un proveedor que use esta API para crear una clase base. Por ejemplo, si cree que el código MOF del proveedor no se instalará correctamente, puede indicar a su proveedor que cree automáticamente las clases correctas en el repositorio WMI. Para obtener más información sobre los proveedores, consulte [escribir un proveedor de clases](writing-a-class-provider.md).

> [!Note]  
> Las clases no se pueden cambiar durante la ejecución de proveedores. Debe detener la actividad, cambiar la clase y, a continuación, reiniciar el servicio de administración de Windows. Actualmente no es posible detectar un cambio de clase.

 

El código requiere que la siguiente referencia se compile correctamente.


```C++
#include <wbemidl.h>
```



Puede crear una nueva clase base mediante programación con la [API com para WMI](com-api-for-wmi.md).

**Para crear una nueva clase base con la API de WMI**

1.  Recupere una definición de la nueva clase llamando al método [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) con el parámetro *strObjectPath* establecido en un valor **null** .

    En el ejemplo de código siguiente se muestra cómo recuperar una definición para una nueva clase.

    ```C++
    IWbemServices* pSvc = 0;
    IWbemContext* pCtx = 0;
    IWbemClassObject* pNewClass = 0;
    IWbemCallResult* pResult = 0;
    HRESULT hRes = pSvc->GetObject(0, 0, pCtx, &pNewClass, &pResult);
    ```

    

2.  Establezca un nombre para la clase estableciendo la propiedad System de **\_ \_ clase** con una llamada al método [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .

    En el ejemplo de código siguiente se muestra cómo asignar un nombre a la clase estableciendo la propiedad del sistema de **\_ \_ clase** .

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

    

3.  Cree la propiedad o propiedades de clave llamando a [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    En el ejemplo de código siguiente se describe cómo crear la propiedad de [**Índice**](swbemrefreshableitem-index.md) , que se etiqueta como una propiedad clave en el paso 4.

    ```C++
      BSTR KeyProp = SysAllocString(L"Index");
      pNewClass->Put(KeyProp, 0, NULL, CIM_STRING);
    ```

    

4.  Adjunte el calificador estándar de [**clave**](standard-qualifiers.md) a la propiedad de clave llamando primero al método [**IWbemClassObject:: GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) y, a continuación, al método [**IWbemQualifierSet::P UT**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) .

    En el ejemplo de código siguiente se muestra cómo adjuntar el calificador estándar de [**clave**](standard-qualifiers.md) a la propiedad de clave.

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

    

5.  Cree otras propiedades de la clase con [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    En el ejemplo de código siguiente se describe cómo crear propiedades adicionales.

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

    

6.  Registre la nueva clase llamando a [**IWbemServices::P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).

    Dado que no puede definir claves e índices después de registrar una nueva clase, asegúrese de que ha definido todas las propiedades antes de llamar a [**PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).

    En el ejemplo de código siguiente se describe cómo registrar una nueva clase.

    ```C++
      hRes = pSvc->PutClass(pNewClass, 0, pCtx, &pResult);
      pNewClass->Release();
    ```

    

En el ejemplo de código siguiente se combinan los ejemplos de código descritos en el procedimiento anterior y se muestra cómo crear una clase base mediante la API de WMI.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una clase](creating-a-class.md)
</dt> </dl>

 

 



