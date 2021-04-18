---
description: A continuación se enumeran los calificadores estándar específicos de WMI.
ms.assetid: 63bdbafc-51f3-4714-8b7e-9d5a61cef45e
ms.tgt_platform: multiple
title: Calificadores WMI estándar
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Standard
api_type:
- NA
api_location: ''
ms.openlocfilehash: e73b053354d86c4a56698a7a65c17e302425f56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706650"
---
# <a name="standard-wmi-qualifiers"></a>Calificadores WMI estándar

A continuación se enumeran los calificadores estándar específicos de WMI.

<dt>

<span id="Amendment"></span><span id="amendment"></span><span id="AMENDMENT"></span>**Corrección**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: clases

Indica que una clase contiene calificadores corregidos que están localizados. El valor predeterminado es **true**.

La clase asociada se puede traducir. Para tener acceso a la versión traducida, use el identificador de configuración regional para construir un nombre de espacio de nombres.

</dd> <dt>

<span id="Bypass_GetObject"></span><span id="bypass_getobject"></span><span id="BYPASS_GETOBJECT"></span>**Omitir \_ GetObject**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: métodos

Indica que la llamada al método debe pasar directamente a la llamada **ExecMethodAsync** del proveedor en lugar de que el proveedor realice primero una llamada a **GetObject** para validar la ruta de acceso del objeto. El valor predeterminado es **false**. El uso de **bypass \_ GetObject** puede mejorar significativamente el rendimiento.

Antes de usar **bypass \_ GetObject**, asegúrese de que no se realiza ninguna de las siguientes acciones:

-   Derive una clase de la clase.
-   Invalide el método que tiene el calificador **\_ GetObject bypass** .

Si no se siguen estas precauciones, se puede invocar la implementación del método de la clase primaria en lugar de la clase secundaria. Para obtener más información, vea usar el \_ calificador de omisión de GetObject.

</dd> <dt>

<span id="CIM_Key"></span><span id="cim_key"></span><span id="CIM_KEY"></span>**\_Clave CIM**
</dt> <dd>

Tipo de datos: **CIM \_ booleano**

Se aplica a: propiedades

Indica que la propiedad asociada es una propiedad clave en CIM pero no en WMI.

</dd> <dt>

<span id="CIMType"></span><span id="cimtype"></span><span id="CIMTYPE"></span>[**CIMType**](cimtype-qualifier.md)
</dt> <dd>

Tipo de datos: **VT \_ BSTR**

Se aplica a: propiedades, métodos, parámetros

Contiene el texto que describe el tipo de una propiedad.

</dd> <dt>

<span id="ClassContext"></span><span id="classcontext"></span><span id="CLASSCONTEXT"></span>**ClassContext**
</dt> <dd>

Tipo de datos: **VT \_ BSTR**

Se aplica a: clases

Indica que una clase tiene instancias asociadas a más información de forma dinámica y proporcionada por un proveedor.

</dd> <dt>

<span id="Deprecated"></span><span id="deprecated"></span><span id="DEPRECATED"></span>**En desuso**
</dt> <dd>

Tipo de datos: **CIM \_ booleano**

Se aplica a: propiedades, clases

Indica que la propiedad ha sido reemplazada por otra propiedad.

</dd> <dt>

<span id="Display"></span><span id="display"></span><span id="DISPLAY"></span>**Muestra**
</dt> <dd>

Se aplica a: clases, propiedades

**UUID** de la clase asociada.

</dd> <dt>

<span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>[**Dinámica**](dynamic-qualifier.md)
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: clases, propiedades

Indica una clase cuyas instancias se crean dinámicamente. El valor de este calificador debe establecerse en **true**.

</dd> <dt>

<span id="DynProps"></span><span id="dynprops"></span><span id="DYNPROPS"></span>**DynProps**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: clases, instancias

Indica que una instancia contiene los valores proporcionados por los proveedores de propiedades dinámicas. El valor predeterminado es **true**.

Debe especificar este calificador en una instancia de este tipo. Solo se permite el valor **true** .

</dd> <dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>**Resuelto**
</dt> <dd>

Tipo de datos: **CIM \_ booleano**

Se aplica a: instancias

Indica que el valor de esta propiedad no puede cambiar durante la duración de la instancia.

</dd> <dt>

<span id="ID"></span><span id="id"></span>**SESIÓN**
</dt> <dd>

Tipo de datos: **VT \_ I4**

Se aplica a: propiedades, parámetros

Identifica y secuencia de forma única un parámetro de propiedad o de método cuando se generan automáticamente instrucciones de MOF.

Este calificador solo es necesario para los parámetros de método. Al crear parámetros para un método, los diseñadores de clases deben comenzar con el identificador (0) para el primer parámetro y usar cada entero sucesivo para cada parámetro sucesivo. Si los calificadores de **identificador** se omiten involuntariamente, el compilador MOF genera automáticamente calificadores de **identificador** .

</dd> <dt>

<span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Ha**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: métodos

Indica que un método tiene una implementación proporcionada por un proveedor.

</dd> <dt>

<span id="InstanceContext"></span><span id="instancecontext"></span><span id="INSTANCECONTEXT"></span>**InstanceContext**
</dt> <dd>

Tipo de datos: **VT \_ BSTR**

Se aplica a: instancias

Indica que una instancia contiene los valores proporcionados por un proveedor de propiedades dinámicas.

El valor se pasa al proveedor de propiedades como argumento al método [**IWbemPropertyProvider:: GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) .

</dd> <dt>

<span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Configuración regional**
</dt> <dd>

Tipo de datos: **VT \_ BSTR**

Se aplica a: clases o instancias

Especifica el idioma de origen de una clase o instancia. Para obtener más información sobre los valores de configuración regional, consulte [códigos de configuración regional](#locale-codes).

</dd> <dt>

<span id="NamespaceSecuritySDDL"></span><span id="namespacesecuritysddl"></span><span id="NAMESPACESECURITYSDDL"></span>**NamespaceSecuritySDDL**
</dt> <dd>

Tipo de datos: **matriz de cadenas**

Se aplica a: instancias de espacio de nombres

Especifica un descriptor de seguridad para el espacio de nombres en formato [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language) . Para obtener más información, vea [establecer la seguridad del espacio de nombres cuando se crea el espacio de nombres](setting-namespace-security-when-the-namespace-is-created.md). WMI procesa la cadena SDDL para establecer la seguridad del espacio de nombres, pero no se almacena como una cadena. Si no se especifica ningún descriptor de seguridad, se usa la seguridad predeterminada. Para obtener más información, consulte [configuración de descriptores de seguridad de espacio](setting-namespace-security-descriptors.md).

</dd> <dt>

<span id="Optional"></span><span id="optional"></span><span id="OPTIONAL"></span>**Opta**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: parámetros

Indica que un parámetro no es necesario y que tiene un valor predeterminado con el comportamiento correcto.

</dd> <dt>

<span id="Privileges"></span><span id="privileges"></span><span id="PRIVILEGES"></span>**Privilegios**
</dt> <dd>

Tipo de datos: **matriz de cadenas**

Se aplica a: propiedades, métodos

Conjunto de valores que se usa para informar al cliente de los privilegios necesarios para crear instancias, rellenar propiedades o realizar métodos. El valor predeterminado es **false**.

</dd> <dt>

<span id="PropertyContext"></span><span id="propertycontext"></span><span id="PROPERTYCONTEXT"></span>**PropertyContext**
</dt> <dd>

Tipo de datos: **VT \_ BSTR**

Se aplica a: propiedades

Indica que una propiedad de instancia contiene los valores proporcionados por los proveedores de propiedades dinámicas.

Debe especificar este calificador en una propiedad de este tipo. El valor se pasa al proveedor de propiedades como argumento a [**IWbemPropertyProvider:: GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty).

</dd> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Presta**
</dt> <dd>

Tipo de datos: **VT \_ BSTR**

Se aplica a: clases

El valor de este calificador es el nombre del proveedor dinámico que proporciona instancias de clase y actualiza los datos de instancia. Este nombre se debe registrar con WMI mediante la creación de una instancia de la clase [**\_ \_ Win32Provider**](--win32provider.md) con la propiedad **Name** que contiene este nombre. Cuando se especifica este calificador en una clase cuyas instancias se proporcionan dinámicamente, también se debe especificar el calificador **dinámico** .

</dd> <dt>

<span id="RequiresEncryption"></span><span id="requiresencryption"></span><span id="REQUIRESENCRYPTION"></span>**RequiresEncryption**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: instancias de espacio de nombres

Si se establece en **true**, **RequiresEncryption** marca un espacio de nombres para que las aplicaciones cliente y los scripts se deben conectar con la autenticación cifrada. El nivel de autenticación debe establecerse **en \_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C en C++. En scripting o Visual Basic, el nivel de autenticación debe establecerse en **WbemAuthenticationLevelPktPrivacy**. Para obtener más información, consulte [configuración de descriptores de seguridad de espacio](setting-namespace-security-descriptors.md). El calificador se utiliza en [*MOF*](gloss-m.md) con el comando de preprocesador de espacio de nombres pragma.

Para obtener más información, vea [establecer el nivel de seguridad de proceso predeterminado mediante C++](setting-the-default-process-security-level-using-c-.md) o [establecer el nivel de seguridad de proceso predeterminado mediante VBScript](setting-the-default-process-security-level-using-vbscript.md). Los niveles de autenticación de scripting se definen en [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).

</dd> <dt>

<span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Simple**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: clases

Designa una clase que solo puede tener una instancia y que no contiene propiedades de clave.

Solo se permite el valor **true** (predeterminado).

</dd> <dt>

<span id="Static"></span><span id="static"></span><span id="STATIC"></span>**Estático**
</dt> <dd>

Tipo de datos: **booleano**

Se aplica a: métodos

Indica si se puede llamar a un método utilizando la definición de clase o sus instancias.

No se puede invocar el método desde una instancia de.

</dd> <dt>

<span id="SubType"></span><span id="subtype"></span><span id="SUBTYPE"></span>**Subtipo**
</dt> <dd>

Tipo de datos: **VT \_ BSTR**

Se aplica a: propiedades

Indica que una propiedad de tipo **\_ DateTime de CIM** representa un intervalo de tiempo en lugar de una hora específica.

Para identificar la propiedad como un intervalo, el valor de este calificador debe ser "Interval". El resto de los valores de este calificador se reservan para uso futuro.

</dd> <dt>

<span id="UUID"></span><span id="uuid"></span>**UUID**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: clases

Identificador único universal que se aplica a la clase.

</dd> <dt>

<span id="ClassVersion"></span><span id="classversion"></span><span id="CLASSVERSION"></span>**ClassVersion**
</dt> <dd>

Tipo de datos: **cadena**

Se aplica a: clases

Número de versión del objeto de clase. El valor predeterminado es **null**. El número de versión se incrementa cuando se realizan cambios en la clase.

</dd> <dt>

<span id="WritePrivileges"></span><span id="writeprivileges"></span><span id="WRITEPRIVILEGES"></span>**WritePrivileges**
</dt> <dd>

Tipo de datos: **matriz de cadenas**

Se aplica a: propiedades

Conjunto de valores que indican qué privilegios del sistema deben estar disponibles y habilitados para una operación de escritura correcta.

</dd> </dl>

## <a name="remarks"></a>Observaciones

### <a name="locale-codes"></a>Códigos de configuración regional

Un código de configuración regional tiene el formato "MS \_ <Three Digit Language ID> ". Por ejemplo, la configuración regional en inglés es MS \_ 409. En la tabla siguiente se enumeran los identificadores de idioma.



| Idioma              | IDENTIFICADOR de idioma (hexadecimal) |
|-----------------------|---------------------------|
| Árabe                | 401                       |
| Portugués (Brasil)   | 416                       |
| Chino (simplificado)  | 804                       |
| Chino (tradicional) | 404                       |
| Checo                 | 405                       |
| Danés                | 406                       |
| Neerlandés                 | 413                       |
| Inglés (predeterminado)     | 409                       |
| Finés               | 40b                       |
| Francés                | 40c                       |
| Alemán                | 407                       |
| Griego                 | 408                       |
| Hebreo                | 40d                       |
| Húngaro             | 40e                       |
| Italiano               | 410                       |
| Japonés              | 411                       |
| Coreano                | 412                       |
| Noruego             | 414                       |
| Polaco                | 415                       |
| Portugués (Portugal) | 816                       |
| Ruso               | 419                       |
| Español               | c0a                       |
| Sueco               | 41D                       |
| Turco               | 41f                       |



 

### <a name="using-the-bypass_getobject-qualifier"></a>Usar el \_ calificador de GetObject bypass

El uso del calificador **\_ GetObject bypass** en un método puede generar resultados confusos.

En el ejemplo siguiente se definen las clases de **forma** y **círculo** . Tenga en cuenta que la clase **Circle** se deriva de la clase **Shape** .


```VB
class Shape
{
   string Name;
   uint32 DrawIt();  // - draws an irregular geometric shape
};

class Circle : Shape
{
   uint32 DrawIt();  // - draws a circle
};
```



La siguiente llamada a **ExecMethod** usa un objeto **Circle** denominado "Circle" para dibujar un círculo.


```VB
ExecMethod("Shape.Name='MyCircle'","DrawIt");
```



En el escenario anterior, WMI llama a **GetObject**; detecta que "Shape. name = ' Circle '" es un **círculo**; y ejecutan la implementación del **círculo** de **DrawIt**. Sin embargo, si usa el calificador **bypass \_ GetObject** en **DrawIt**, WMI no llama a **GetObject**, no detecta que "Shape. name = ' Circle '" es un **círculo** y ejecuta la implementación de la **forma** de **DrawIt** en lugar de la implementación de **Circle** de **DrawIt**.

La siguiente llamada a **ExecMethod** siempre invoca la implementación correcta de **DrawIt**.


```VB
ExecMethod("Circle.Name='MyCircle'","DrawIt");
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Configuración de descriptores de seguridad de espacio](setting-namespace-security-descriptors.md)
</dt> <dt>

[Calificadores WMI](wmi-qualifiers.md)
</dt> <dt>

[Adición de un calificador](adding-a-qualifier.md)
</dt> </dl>

 

