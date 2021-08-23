---
description: Para crear un método WMI, defina los parámetros de entrada y salida para el método .
ms.assetid: 71cbecde-33c4-4bf1-9793-bef6d823dcac
ms.tgt_platform: multiple
title: Crear un método WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 689f69518f440e7c1983a92fbf86877c5c6dd2149ce2b31b8459aa08b9e94c4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612535"
---
# <a name="creating-a-wmi-method"></a>Crear un método WMI

Para crear un método WMI, defina los parámetros de entrada y salida para el método . Los parámetros de entrada y salida se representan mediante una clase de sistema WMI [**\_ \_ especial PARAMETERS**](--parameters.md). Para obtener más información, vea [Llamar a un método y](calling-a-method.md) Escribir un proveedor de [métodos](writing-a-method-provider.md).

En este tema se de abordan las siguientes secciones:

-   [Crear un método de clase WMI en MOF](#creating-a-wmi-class-method-in-mof)
-   [Crear un método de clase WMI en C++](#creating-a-wmi-class-method-in-c)
-   [Temas relacionados](#related-topics)

## <a name="creating-a-wmi-class-method-in-mof"></a>Crear un método de clase WMI en MOF

En WMI, los métodos de proveedor suelen ser acciones distintas relacionadas con el objeto que representa la clase . En lugar de cambiar el valor de una propiedad para ejecutar una acción, se debe crear un método . Por ejemplo, puede habilitar o deshabilitar un centro de información de red (NIC) representado por [**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) mediante los métodos [**Habilitar**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter) [**y**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter) Deshabilitar. Aunque estas acciones se pueden representar como una propiedad de lectura y escritura, el diseño recomendado es crear un método. Como alternativa, si desea que un estado o valor sea visible para la clase, el enfoque recomendado es crear una propiedad de lectura y escritura en lugar de un método. En **Win32 \_ NetworkAdapter**, la propiedad **NetEnabled** hace que el estado del adaptador sea visible, pero los métodos **Enable** o **Disable** ejecutan los cambios entre estados.

Las declaraciones de clase pueden incluir la declaración de uno o varios métodos. Puede optar por heredar los métodos de una clase primaria o implementar los suyos propios. Si decide implementar sus propios métodos, debe declarar el método y marcar el método con etiquetas de calificador específicas.

En el procedimiento siguiente se describe cómo declarar un método en una clase que no hereda de una clase base.

**Para declarar un método**

1.  Defina el nombre del método entre las llaves de una declaración de clase, seguido de cualquier calificador.

    En el ejemplo de código siguiente se describe la sintaxis de un método .

    ``` syntax
    [Dynamic, Provider ("ProviderName")]
    class ClassName
    {
        [Implemented] <ReturnType> <MethodName>
            ([ParameterDirection, IDQualifier] 
            <ParameterType> <ParameterName>);
    };
    ```

2.  Cuando termine, inserte el Managed Object Format (MOF) en el repositorio WMI con una llamada al compilador MOF.

    Para obtener más información, [vea Compilar archivos MOF](compiling-mof-files.md).

En la lista siguiente se definen los elementos de la declaración de método.

<dl> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>[**Proveedor**](/windows/desktop/api/Provider/nl-provider-provider)
</dt> <dd>

Vincula un proveedor específico a la descripción de la clase. El valor del [**calificador Provider**](/windows/desktop/api/Provider/nl-provider-provider) es el nombre del proveedor, que indica a WMI dónde reside el código que admite el método. Un proveedor también debe marcar con el **calificador Dinámico** cualquier clase que tenga instancias dinámicas. Por el contrario, no use el calificador **Dinámico** para marcar una clase que contiene una instancia estática con **métodos implementados.**

</dd> <dt>

<span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Implementado**
</dt> <dd>

Declara que implementará un método, en lugar de heredar la implementación del método de la clase primaria. De forma predeterminada, WMI propaga la implementación de la clase primaria a una clase derivada a menos que la clase derivada proporciona una implementación. Omitir el **calificador Implementado** indica que el método no tiene ninguna implementación en esa clase. Si se reeclara un  método sin el calificador Implementado, WMI sigue presupone que no se va a implementar ese método e invoca la implementación del método de clase primaria cuando se llama a . Por lo tanto, volver a declarar un método en una clase derivada sin asociar el calificador **Implementado** solo es útil cuando se agrega o quita un calificador al método o desde este.

</dd> <dt>

<span id="ReturnType"></span><span id="returntype"></span><span id="RETURNTYPE"></span>ReturnType
</dt> <dd>

Describe el valor que devuelve el método. El valor devuelto para un método debe ser un objeto booleano, numérico, **CHAR,** **STRING,** [DATETIME](datetime.md)o de esquema. También puede declarar el tipo de valor devuelto [como VOID](void.md), lo que indica que el método no devuelve nada. Sin embargo, no se puede declarar una matriz como un tipo de valor devuelto.

</dd> <dt>

<span id="MethodName"></span><span id="methodname"></span><span id="METHODNAME"></span>Nombredemétodo
</dt> <dd>

Define el nombre del método. Cada método debe tener un nombre único. WMI no permite que existan dos métodos con el mismo nombre y firmas diferentes en una clase o dentro de una jerarquía de clases. Por lo tanto, tampoco puede sobrecargar un método .

</dd> <dt>

<span id="ParameterDirection"></span><span id="parameterdirection"></span><span id="PARAMETERDIRECTION"></span>ParameterDirection
</dt> <dd>

Contiene calificadores que describen si un parámetro es un parámetro de entrada, un parámetro de salida o ambos. No use el mismo nombre de parámetro más de una vez como parámetro de entrada o más de una vez como parámetro de salida. Si aparece el mismo nombre de parámetro con los calificadores [**In**](standard-qualifiers.md) y **Out,** la funcionalidad es conceptualmente la misma que usar los calificadores **In** y **Out** en un solo parámetro. Sin embargo, cuando se usan declaraciones independientes, los parámetros de entrada y salida deben [](standard-wmi-qualifiers.md) ser exactamente iguales en todos los demás aspectos, incluido el número y el tipo de calificadores de identificador, y el calificador debe ser el mismo y declararse explícitamente para ambos. Se recomienda encarecidamente usar los calificadores **In**, **Out** dentro de una declaración de parámetro único.

</dd> <dt>

<span id="IDQualifier"></span><span id="idqualifier"></span><span id="IDQUALIFIER"></span>**IDQualifier**
</dt> <dd>

Contiene el [**calificador de**](standard-wmi-qualifiers.md) identificador que identifica de forma única la posición de cada parámetro dentro de la secuencia de parámetros del método . De forma predeterminada, el compilador de MOF marca automáticamente los parámetros con un **calificador de** identificador. El compilador marca el primer parámetro con un valor de 0 (cero), el segundo parámetro un valor de 1 (uno), y así sucesivamente. Si es necesario, puede especificar explícitamente la secuencia de identificador en el código MOF.

</dd> <dt>

<span id="ParameterType"></span><span id="parametertype"></span><span id="PARAMETERTYPE"></span>ParameterType
</dt> <dd>

Describe qué tipo de datos puede aceptar el método. Puede definir un tipo de parámetro como cualquier valor de datos MOF, incluida una matriz, un objeto de esquema o una referencia. Cuando use una matriz como parámetro, use la matriz como sin enlazar o con un tamaño explícito.

</dd> <dt>

<span id="ParameterName"></span><span id="parametername"></span><span id="PARAMETERNAME"></span>ParameterName
</dt> <dd>

Contiene el nombre del parámetro. También puede elegir definir el valor predeterminado del parámetro en este momento. Los parámetros que carecen de valores iniciales permanecen sin signo.

</dd> </dl>

En el ejemplo de código siguiente se describen los calificadores y la lista de parámetros.

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

En el ejemplo de código siguiente se describe el uso de un objeto de esquema como parámetro y valor devuelto.

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

En el ejemplo de código siguiente se describe cómo incluir dos referencias: una a una instancia de la clase [**\_ LogicalDisk win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) y la otra a una instancia de un tipo de objeto desconocido.

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

    Primero debe tener una clase en la que colocar el método antes de crear el método .

2.  Recupere dos clases secundarias de la [**\_ \_ clase del**](--parameters.md) sistema PARAMETERS mediante [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

    Use la primera clase secundaria para describir los parámetros en y la segunda para describir los parámetros out. Si es necesario, puede realizar una única recuperación seguida de una llamada al [**método IWbemClassObject::Clone.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-clone)

3.  Escriba los parámetros in en la primera clase y los parámetros out en la segunda clase, mediante una o varias llamadas a [**IWbemClassObject::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    Al describir parámetros en un método, observe las siguientes reglas y restricciones:

    -   Trate los parámetros de entrada y salida como entradas independientes, uno en el objeto que contiene los parámetros in y otro en el objeto que \[ \] contiene los parámetros out.
    -   Aparte de los calificadores de entrada y \[ \] salida, los calificadores restantes deben ser exactamente iguales.
    -   Especifique los [**calificadores**](standard-wmi-qualifiers.md) de identificador, empezando por 0 (cero), uno para cada parámetro.

        El orden de los parámetros de entrada o salida se establece mediante el valor del [**calificador de identificador**](standard-wmi-qualifiers.md) en cada parámetro. Todos los argumentos de entrada deben preceder a los argumentos de salida. Cambiar el orden de los parámetros de entrada y salida del método al actualizar un proveedor de métodos existente puede provocar un error en las aplicaciones que llaman al método. Agregue nuevos parámetros de entrada al final de los parámetros existentes en lugar de insertarlos en la secuencia que ya está establecida.

        Asegúrese de no dejar espacios en la secuencia del [**calificador de**](standard-wmi-qualifiers.md) identificador.

    -   Coloque el valor devuelto en la clase out-parameters como una propiedad denominada **ReturnValue**.

        Esto identifica la propiedad como el valor devuelto del método . El tipo CIM de esta propiedad es el tipo de valor devuelto del método . Si el método tiene un tipo de valor devuelto void, no tiene una **propiedad ReturnValue** en absoluto. Además, la **propiedad ReturnValue** no puede tener un [**calificador de**](standard-wmi-qualifiers.md) identificador como los argumentos del método . La asignación **de un** calificador de identificador a **la propiedad ReturnValue** genera un error wmi.

    -   Expresar cualquier valor de parámetro predeterminado para la propiedad de la clase .

4.  Coloque ambos [**\_ \_ objetos PARAMETERS**](--parameters.md) en la clase primaria con una llamada a [**IWbemClassObject::P utMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).

    Una sola llamada a [**PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod) puede colocar ambos [**\_ \_ objetos PARAMETERS**](--parameters.md) en la clase .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una clase](creating-a-class.md)
</dt> </dl>

 

 
