---
description: Proporciona reglas para asignar clases WMI a Active Directory.
ms.assetid: 295d3233-5729-4eb0-9fa3-1cf64fef2909
ms.tgt_platform: multiple
title: Asignar Active Directory clases
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a606cfacc2e9d56ef07973df182f5ce1a65be35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716431"
---
# <a name="mapping-active-directory-classes"></a>Asignar Active Directory clases

Dado que Active Directory tiene una amplia variedad de objetos posibles, WMI no puede crear una asignación unívoca directa. En su lugar, el proveedor de servicios de directorio utiliza reglas para asignar clases entre las dos tecnologías.

En este tema se describen las siguientes secciones:

-   [Clases de asignación](#mapping-classes)
-   [Atributos de asignación](#mapping-attributes)
-   [Clases de asociación](#association-classes)

> [!Note]  
> Para obtener más información acerca de la compatibilidad y la instalación de este componente en un sistema operativo específico, consulte [disponibilidad del sistema operativo de los componentes de WMI](operating-system-availability-of-wmi-components.md).

 

## <a name="mapping-classes"></a>Clases de asignación

En la lista siguiente se describen las instrucciones que usa el proveedor de servicios de directorio para asignar Active Directory clases a clases WMI:

-   Cada clase abstracta del esquema de Active Directory se asigna a una clase abstracta en el esquema de WMI.

    En el esquema de WMI, cada clase abstracta tiene el prefijo DS \_ . Por ejemplo, la clase **Person** del esquema Active Directory se asigna a la clase WMI **\_ Person de DS** .

-   Cada clase no abstracta del esquema de Active Directory se asigna a las dos clases siguientes en el esquema de WMI:

    -   La primera clase asignada tiene como prefijo ADS \_ . Se trata de clases abstractas asignadas según las reglas siguientes.
    -   La segunda clase asignada es una clase no abstracta con el \_ Prefijo de nombre de DS. Esta clase se deriva de la \_ clase abstracta ADS, con la adición del calificador de [**proveedor**](/windows/desktop/api/Provider/nl-provider-provider) .

    Por ejemplo, la clase de **usuario** de la Active Directory esquema se asigna a dos clases. La primera clase es la clase abstracta de **\_ usuario ADS** , asignada según las reglas siguientes. La segunda clase es la clase no abstracta **\_ usuario de DS** . Se deriva del **\_ usuario ADS** y tiene el calificador de [**proveedor**](/windows/desktop/api/Provider/nl-provider-provider) agregado.

-   A menos que se especifique lo contrario, el nombre de una clase asignada es el valor alterado de la propiedad **LDAP-Display-Name** en la clase Active Directory.
-   Si la **subclase de** la propiedad está presente en la clase Active Directory, la clase asignada por WMI se deriva de la clase especificada.

    Si no está presente la **subclase de** la propiedad, la clase asignada por WMI se deriva de la clase de **\_ \_ \_ clase raíz DS LDAP** , tal y como se especifica en el archivo MOF.

    > [!Note]  
    > Esta clase tiene la propiedad clave **ADSIPath** , con un tipo **VT \_ BSTR**. Esta es la ruta de acceso ADSI única que identifica esta instancia. Active Directory solo admite la herencia única, por lo que funciona.

     

-   Se crea un calificador **dinámico** de tipo **VT \_ bool** y Flavor `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` establecido en **true** para cada clase. Se trata de un calificador WMI estándar que indica que las instancias de esta clase se proporcionan dinámicamente.
-   Si la clase no es abstracta, el proveedor crea un calificador de [**proveedor**](/windows/desktop/api/Provider/nl-provider-provider) de tipo **VT \_ BSTR bool** y el tipo de calificador `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` establecido en "proveedor de instancia de DS" para cada clase. Se trata de un calificador WMI estándar que indica el nombre del proveedor que proporciona de forma dinámica las instancias de esta clase.

El resto de las propiedades ADSI se asignan a los calificadores y propiedades de clase según las tablas siguientes. Todos los calificadores se asignan con un valor de marca de calificador de `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` .

A continuación se enumera la información de asignación de la clase Active Directory, que muestra el calificador WMI y el tipo de calificador WMI para cada propiedad Active Directory.

<dl> <dt>

**Nombre común**
</dt> <dd>

**CN** (**VT \_ BSTR**)

Se asigna directamente desde el valor de cadena.

</dd> <dt>

**Default-Object-Category**
</dt> <dd>

**DefaultObjectCategory** (**VT \_ BSTR**)

Se asigna directamente desde el valor de cadena.

</dd> <dt>

**Default-Security-Descriptor**
</dt> <dd>

**DefaultSecurityDescriptor** (**VT \_ BSTR**)

Se asigna directamente desde el valor de cadena.

</dd> <dt>

**Controla el identificador**
</dt> <dd>

**GovernsId** (**VT \_ BSTR**)

Asignada a partir de la representación de cadena del OID; por ejemplo, "{1 3 3 6}".

</dd> <dt>

**Clase de objeto**
</dt> <dd>

N/D

No asignado.

</dd> <dt>

**Objeto-clase-categoría**
</dt> <dd>

**ObjectClassCategory** (**VT \_ I4**)

Se asigna directamente desde el valor entero. Además, si el valor es abstracto (2), también se crea el calificador de CIM de **VT \_** estándar, denominado calificador **"abstracto"** .

</dd> <dt>

**RDN-ATT-ID**
</dt> <dd>

**RDNATTID** (**VT \_ BSTR**)

Asignada a partir de la representación de cadena del valor de OID; por ejemplo, "{1 3 3 6}". Además, la propiedad identificada aquí se anota con el calificador de CIM **indexado** estándar establecido en **true**.

</dd> <dt>

**Solo del sistema**
</dt> <dd>

**SystemOnly** (**VT \_ bool**)

Se asigna directamente desde el valor booleano.

</dd> </dl>

 

A continuación se enumeran las propiedades de clase de Active Directory asignadas a las propiedades de clase WMI.

<dl> <dt>

**Puede contener**
</dt> <dd>

Cada propiedad de esta lista se asigna a una propiedad WMI.

</dd> <dt>

**Debe contener**
</dt> <dd>

Cada propiedad de esta lista se asigna a una propiedad WMI. Se crea el calificador de CIM estándar **not \_ null** para cada uno de ellos.

</dd> <dt>

**Sistema: puede contener**
</dt> <dd>

Cada propiedad de esta lista se asigna a una propiedad WMI. Además, cada propiedad se anota con un calificador **del sistema** , establecido en **true**.

</dd> <dt>

**Sistema: debe contener**
</dt> <dd>

Cada propiedad de esta lista se asigna a una propiedad WMI. Se crea el calificador de CIM estándar **not \_ null** para cada uno de ellos. Además, cada propiedad se anota con un calificador **del sistema** , establecido en **true**.

</dd> </dl>

## <a name="mapping-attributes"></a>Atributos de asignación

El proveedor de servicios de directorio asigna cada atributo de una clase Active Directory a exactamente una propiedad de la clase WMI correspondiente según las reglas de esta sección. En general, el proveedor de servicios de directorio denomina la propiedad WMI como la versión alterada del valor **LDAP-Display-Name** del atributo Active Directory.

Si la propiedad Active Directory **tiene el valor** **false**, esta propiedad WMI se combina con el operador OR con una **\_ \_ matriz de marca CIM**. Tenga en cuenta que cada propiedad se etiqueta con el calificador **\_ BSTR de VT** , **ADSyntax**. Representa la sintaxis de Active Directory subyacente.

En la tabla siguiente se muestra la asignación de la sintaxis de Active Directory al tipo de datos de la propiedad WMI.



| Elemento Active Directory                                      | Tipo de datos WMI                                                           |
|---------------------------------------------------------------|-------------------------------------------------------------------------|
| [**Punto de acceso**](/windows/desktop/ADSchema/s-object-access-point)            | **\_cadena CIM**                                                         |
| [**Booleano**](/windows/desktop/ADSchema/s-boolean)                             | **\_BOOLEANO CIM**                                                        |
| **Cadena sin distinción entre mayúsculas y minúsculas**                                   | **\_cadena CIM**                                                         |
| [**Cadena que distingue mayúsculas de minúsculas**](/windows/desktop/ADSchema/s-string-case-sensitive) | **\_cadena CIM**                                                         |
| [**Nombre distintivo**](/windows/desktop/ADSchema/s-object-ds-dn)             | **\_cadena CIM**                                                         |
| [**DN: binario**](/windows/desktop/ADSchema/s-object-dn-binary)                  | Objeto incrustado de la clase **DN \_ con el \_ binario** definido a continuación.<br/> |
| [**Cadena DN**](/windows/desktop/ADSchema/s-object-dn-string)                  | Objeto incrustado de la clase **DN \_ con la \_ cadena** que se define a continuación.<br/> |
| [**Enumeración**](/windows/desktop/ADSchema/s-enumeration)                     | **\_SINT32 CIM**                                                         |
| [**Enumeración**](/windows/desktop/ADSchema/s-enumeration)                     | **\_cadena CIM**                                                         |
| [**Entero**](/windows/desktop/ADSchema/s-integer)                             | **\_SINT32 CIM**                                                         |
| [**LargeInteger**](/windows/desktop/ADSchema/s-largeinteger)                   | **\_cadena CIM**                                                         |
| Descriptor de seguridad                                           | Objeto incrustado de la clase **, uint8array** que se define a continuación.<br/>       |
| Cadena numérica                                                | **\_cadena CIM**                                                         |
| Identificador de objeto                                                     | **\_cadena CIM**                                                         |
| Cadena de octeto                                                  | Objeto incrustado de la clase **, uint8array** que se define a continuación.<br/>       |
| O nombre                                                       | **\_cadena CIM**                                                         |
| Presentation-Address                                          | Objeto incrustado de la clase **, uint8array** que se define a continuación.<br/>       |
| Cadena de caso de impresión                                             | **\_cadena CIM**                                                         |
| Vínculo de réplica                                                  | Objeto incrustado de la clase **, uint8array** que se define a continuación.<br/>       |
| [**Cadena (SID)**](/windows/desktop/ADSchema/s-string-sid)                      | Objeto incrustado de la clase **, uint8array** que se define a continuación.<br/>       |
| Hora                                                          | **\_fecha y hora de CIM**                                                       |
| Hora codificada UTC                                                | **\_fecha y hora de CIM**                                                       |
| Cadena Unicode                                                | **\_cadena CIM**                                                         |



 

La sintaxis de la cadena de octetos, que hace referencia a una matriz de valores **Uint8** , presenta un problema cuando se asigna a WMI porque WMI permite propiedades de tipos **Uint8** y matrices de **Uint8**, mientras que Active Directory permite propiedades de tipo cadena de octetos, así como matrices de cadenas de octetos.

En el ejemplo siguiente se muestra la clase de proveedor de servicios de directorio que se usa para asignar una matriz de propiedades de tipo de cadena de octeto.

``` syntax
Class Uint8Array 
{
    uint8 values[];
    uint32 numberOfValues;
};
```

WMI asigna todas las cadenas de octetos Active Directory valores de propiedad a las instancias incrustadas de **, uint8array**. Del mismo modo, WMI asigna matrices de cadenas de octetos a matrices de objetos **, uint8array** insertados.

En el ejemplo siguiente se muestran las clases asignadas por WMI para DN-Binary y DN-String los valores de propiedad de DS.

``` syntax
Class DN_With_String
{
    string dnString;
    string value;
};

Class DN_With_Binary
{
    string dnString;
    uint8 value[];
};
```

En la tabla siguiente se muestra cómo asigna WMI el resto de las propiedades de la interfaz de atributo de Active Directory a los calificadores de propiedad WMI.



| Active Directory nombre de propiedad de atributo | Calificador de WMI       | Tipo de datos    | Información de asignación                               |
|------------------------------------------|---------------------|--------------|---------------------------------------------------|
| **Sintaxis de atributo**                     | **AttributeSyntax** | **VT \_ BSTR** | Asignada a partir de la representación de cadena del OID. |
| **Nombre común**                          | **CN**              | **VT \_ BSTR** | Asignado desde el valor de cadena.                     |
| **Solo del sistema**                          | **Sistema**          | **VT \_ bool** | Asignado desde el valor booleano.                    |



 

> [!Note]  
> WMI asigna todos los calificadores de Active Directory con los `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` tipos de calificador.

 

## <a name="association-classes"></a>Clases de asociación

El servicio de directorio es esencialmente un almacén jerárquico de objetos. Los objetos que pueden aparecer en un nivel no hoja en la jerarquía se denominan "contenedores". La estructura de esta jerarquía se controla más en las propiedades "Poss-superior" y "System-Poss-superior" de una clase en el esquema. En conjunto, se especifica el conjunto de clases cuyas instancias pueden estar contenidas en una instancia de una clase contenedora.

En el ejemplo siguiente se modela una asociación CIM como instancias de la clase de asociación estática [**\_ \_ \_ contención de clase LDAP de DS**](/previous-versions/windows/desktop/dsprov/ds-ldap-class-containment).

``` syntax
//  DS Class Associations Provider 

// Create a class of which instances are
// provided by this provider

[
  Association : ToInstance,
  dynamic,
  HasClassRefs,
  Provider("Microsoft|DSLDAPClassAssociationProvider|V1.0")
]
class DS_LDAP_Class_Containment
{
    [key, classref{"DS_LDAP_Root_Class"} : ToInstance ToSubClass]
    object Ref ChildClass;

    [key, classref{"DS_LDAP_Root_Class"} : ToInstance ToSubClass] 
    object Ref ParentClass; // The parent DS Class
};


// Create an instance of the provider class for registration
instance of __Win32Provider as $AssociationsProvider
{
    Name = "Microsoft|DSLDAPClassAssociationProvider|V1.0";
    Clsid = "{33831ED4-42B8-11d2-93AD-00805F853771}";
    ImpersonationLevel = 1;
};    

// Specification of the instances and operation
// provided by the provider
instance of __InstanceProviderRegistration
{
    Provider = $AssociationsProvider;
    SupportsGet = TRUE;
    SupportsPut = FALSE;
    SupportsDelete = FALSE;
    SupportsEnumeration = TRUE;
};
```

El proveedor de clases de asociación admite los métodos [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) y [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) .

 

