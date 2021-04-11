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
# <a name="creating-a-wmi-method"></a>Crear un método WMI

Para crear un método WMI, defina los parámetros de entrada y salida para el método. Los parámetros de entrada y salida se representan mediante [**\_ \_ parámetros**](--parameters.md)de clase del sistema WMI especiales. Para obtener más información, vea [llamar a un método](calling-a-method.md) y [escribir un proveedor de métodos](writing-a-method-provider.md).

En este tema se describen las siguientes secciones:

-   [Crear un método de clase WMI en MOF](#creating-a-wmi-class-method-in-mof)
-   [Crear un método de clase WMI en C++](#creating-a-wmi-class-method-in-c)
-   [Temas relacionados](#related-topics)

## <a name="creating-a-wmi-class-method-in-mof"></a>Crear un método de clase WMI en MOF

En WMI, los métodos de proveedor suelen ser acciones diferentes relacionadas con el objeto que la clase representa. En lugar de cambiar el valor de una propiedad para ejecutar una acción, se debe crear un método. Por ejemplo, puede habilitar o deshabilitar un centro de información de red (NIC) representado por [**Win32 \_ adaptador**](/windows/desktop/CIMWin32Prov/win32-networkadapter) de red mediante los métodos [**enable**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter) y [**Disable**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter) . Aunque estas acciones se pueden representar como una propiedad de lectura y escritura, el diseño recomendado es crear un método. Como alternativa, si desea que un estado o valor esté visible para la clase, el enfoque recomendado es crear una propiedad de lectura/escritura en lugar de un método. En el adaptador de **Win32 \_**, la propiedad **NetEnabled** hace que el estado del adaptador sea visible pero los métodos **enable** o **Disable** ejecutan los cambios entre Estados.

Las declaraciones de clase pueden incluir la declaración de uno o más métodos. Puede optar por heredar los métodos de una clase primaria o implementar el suyo propio. Si decide implementar sus propios métodos, debe declarar el método y marcar el método con etiquetas de calificador específicas.

En el procedimiento siguiente se describe cómo declarar un método en una clase que no se hereda de una clase base.

**Para declarar un método**

1.  Defina el nombre del método entre las llaves de una declaración de clase, seguidos de los calificadores.

    En el ejemplo de código siguiente se describe la sintaxis de un método.

    ``` syntax
    [Dynamic, Provider ("ProviderName")]
    class ClassName
    {
        [Implemented] <ReturnType> <MethodName>
            ([ParameterDirection, IDQualifier] 
            <ParameterType> <ParameterName>);
    };
    ```

2.  Cuando termine, inserte el código de Managed Object Format (MOF) en el repositorio WMI con una llamada al compilador MOF.

    Para obtener más información, vea [compilar archivos MOF](compiling-mof-files.md).

La lista siguiente define los elementos de la declaración del método.

<dl> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>[**Presta**](/windows/desktop/api/Provider/nl-provider-provider)
</dt> <dd>

Vincula un proveedor específico a la descripción de la clase. El valor del calificador de [**proveedor**](/windows/desktop/api/Provider/nl-provider-provider) es el nombre del proveedor, que indica a WMI dónde reside el código que admite el método. Un proveedor también debe marcar con el calificador **dinámico** cualquier clase que tenga instancias dinámicas. Por el contrario, no utilice el calificador **dinámico** para marcar una clase que contenga una instancia estática con métodos **implementados** .

</dd> <dt>

<span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Ha**
</dt> <dd>

Declara que va a implementar un método, en lugar de heredar la implementación del método de la clase primaria. De forma predeterminada, WMI propaga la implementación de la clase primaria a una clase derivada a menos que la clase derivada proporcione una implementación de. Al omitir el calificador **implementado** , se indica que el método no tiene ninguna implementación en esa clase. Si vuelve a declarar un método sin el calificador **implementado** , WMI sigue suponiendo que no va a implementar ese método e invoca la implementación del método de clase primaria cuando se llama. Como tal, la Redeclaración de un método en una clase derivada sin adjuntar el calificador **implementado** solo es útil cuando se agrega o quita un calificador en el método o desde él.

</dd> <dt>

<span id="ReturnType"></span><span id="returntype"></span><span id="RETURNTYPE"></span>ReturnType
</dt> <dd>

Describe el valor que devuelve el método. El valor devuelto para un método debe ser un objeto booleano, numérico, **Char**, **String**, [DateTime](datetime.md)o Schema. También puede declarar el tipo de valor devuelto como [void](void.md), lo que indica que el método no devuelve nada. Sin embargo, no se puede declarar una matriz como un tipo de valor devuelto.

</dd> <dt>

<span id="MethodName"></span><span id="methodname"></span><span id="METHODNAME"></span>MethodName
</dt> <dd>

Define el nombre del método. Cada método debe tener un nombre único. WMI no permite que existan dos métodos con el mismo nombre y firmas diferentes en una clase o en una jerarquía de clases. Como tal, tampoco se puede sobrecargar un método.

</dd> <dt>

<span id="ParameterDirection"></span><span id="parameterdirection"></span><span id="PARAMETERDIRECTION"></span>ParameterDirection
</dt> <dd>

Contiene calificadores que describen si un parámetro es un parámetro de entrada, un parámetro de salida o ambos. No use el mismo nombre de parámetro más de una vez como parámetro de entrada o más de una vez como parámetro de salida. Si el mismo nombre de parámetro aparece con los calificadores [**in**](standard-qualifiers.md) y **out** , la funcionalidad es conceptualmente igual que el uso de los calificadores **in** y **out** en un solo parámetro. Sin embargo, al usar declaraciones independientes, los parámetros de entrada y salida deben ser exactamente iguales en todos los demás aspectos, incluido el número y el tipo de calificadores de [**identificador**](standard-wmi-qualifiers.md) , y el calificador debe ser el mismo y declarado explícitamente para ambos. Se recomienda encarecidamente usar los calificadores **in** y **out** dentro de una única declaración de parámetro.

</dd> <dt>

<span id="IDQualifier"></span><span id="idqualifier"></span><span id="IDQUALIFIER"></span>**IDQualifier**
</dt> <dd>

Contiene el calificador de [**identificador**](standard-wmi-qualifiers.md) que identifica de forma única la posición de cada parámetro dentro de la secuencia de parámetros en el método. De forma predeterminada, el compilador MOF marca automáticamente los parámetros con un calificador de **identificador** . El compilador marca el primer parámetro con un valor de 0 (cero), el segundo parámetro con un valor de 1 (uno), etc. Si es necesario, puede indicar explícitamente la secuencia de ID. en el código MOF.

</dd> <dt>

<span id="ParameterType"></span><span id="parametertype"></span><span id="PARAMETERTYPE"></span>ParameterType
</dt> <dd>

Describe qué tipo de datos puede aceptar el método. Puede definir un tipo de parámetro como cualquier valor de datos MOF, como una matriz, un objeto de esquema o una referencia. Al utilizar una matriz como parámetro, utilice la matriz como sin enlazar o con un tamaño explícito.

</dd> <dt>

<span id="ParameterName"></span><span id="parametername"></span><span id="PARAMETERNAME"></span>ParameterName
</dt> <dd>

Contiene el nombre del parámetro. También puede optar por definir el valor predeterminado del parámetro en este punto. Los parámetros que carecen de valores iniciales permanecen sin asignar.

</dd> </dl>

En el ejemplo de código siguiente se describen los calificadores y listas de parámetros.

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

En el ejemplo de código siguiente se describe cómo usar una matriz en un parámetro MOF.

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

En el ejemplo de código siguiente se describe el uso de un objeto de esquema como un parámetro y un valor devuelto.

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

En el ejemplo de código siguiente se describe cómo incluir dos referencias: una a una instancia de la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) y la otra a una instancia de un tipo de objeto desconocido.

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

## <a name="creating-a-wmi-class-method-in-c"></a>Crear un método de clase WMI en C++

En el procedimiento siguiente se describe cómo crear un método de clase WMI mediante programación.

**Para crear un método de clase WMI mediante programación**

1.  Cree la clase a la que pertenecerá el método.

    En primer lugar, debe tener una clase en la que colocar el método antes de crear el método.

2.  Recupere dos clases secundarias de la clase de sistema [**\_ \_ Parameters**](--parameters.md) mediante [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

    Use la primera clase secundaria para describir los parámetros in-y el segundo para describir los parámetros out. Si es necesario, puede realizar una recuperación única seguida de una llamada al método [**IWbemClassObject:: Clone**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-clone) .

3.  Escriba los parámetros in-en la primera clase y los parámetros out en la segunda clase, usando una o más llamadas a [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    Al describir los parámetros de un método, observe las siguientes reglas y restricciones:

    -   Trate los \[ parámetros in, out \] como entradas independientes, uno en el objeto que contiene los parámetros in-y uno en el objeto que contiene los parámetros out.
    -   Aparte de los \[ calificadores in, out \] , los calificadores restantes deben ser exactamente iguales.
    -   Especifique los calificadores de [**identificador**](standard-wmi-qualifiers.md) , empezando por 0 (cero), uno para cada parámetro.

        El orden de los parámetros de entrada o salida lo establece el valor del calificador de [**ID**](standard-wmi-qualifiers.md) . en cada parámetro. Todos los argumentos de entrada deben preceder a cualquier argumento de salida. Si se cambia el orden de los parámetros de entrada y salida del método al actualizar un proveedor de métodos existente, pueden producirse errores en las aplicaciones que llaman al método. Agregue nuevos parámetros de entrada al final de los parámetros existentes en lugar de insertarlos en la secuencia que ya está establecida.

        Asegúrese de no dejar huecos en la secuencia del calificador de [**identificador**](standard-wmi-qualifiers.md) .

    -   Coloque el valor devuelto en la clase out-Parameters como una propiedad denominada **ReturnValue**.

        Esto identifica la propiedad como el valor devuelto del método. El tipo CIM de esta propiedad es el tipo de valor devuelto del método. Si el método tiene un tipo de valor devuelto de void, no hay ninguna propiedad **ReturnValue** en absoluto. Además, la propiedad **ReturnValue** no puede tener un calificador de [**identificador**](standard-wmi-qualifiers.md) como los argumentos del método. La asignación de un calificador de **identificador** a la propiedad **ReturnValue** produce un error de WMI.

    -   Exprese los valores de parámetro predeterminados para la propiedad en la clase.

4.  Coloque ambos objetos de [**\_ \_ parámetros**](--parameters.md) en la clase primaria con una llamada a [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).

    Una única llamada a [**PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod) puede colocar ambos objetos de [**\_ \_ parámetros**](--parameters.md) en la clase.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una clase](creating-a-class.md)
</dt> </dl>

 

 
