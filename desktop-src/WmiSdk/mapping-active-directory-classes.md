---
description: Proporciona reglas para asignar clases WMI a Active Directory.
ms.assetid: 295d3233-5729-4eb0-9fa3-1cf64fef2909
ms.tgt_platform: multiple
title: Clases de Active Directory asignación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc38e91d52b59a206a0b64465d0f9710f6d515c9487853824477b7f4f6a126aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992905"
---
# <a name="mapping-active-directory-classes"></a>Clases de Active Directory asignación

Dado Active Directory tiene una amplia variedad de objetos posibles, WMI no puede crear una asignación uno a uno directa. En su lugar, el proveedor de servicios de directorio usa reglas para asignar clases entre las dos tecnologías.

En este tema se de abordan las siguientes secciones:

-   [Clases de asignación](#mapping-classes)
-   [Atributos de asignación](#mapping-attributes)
-   [Clases de asociación](#association-classes)

> [!Note]  
> Para obtener más información sobre la compatibilidad y la instalación de este componente en un sistema operativo específico, vea Disponibilidad del [sistema operativo de componentes WMI](operating-system-availability-of-wmi-components.md).

 

## <a name="mapping-classes"></a>Clases de asignación

En la lista siguiente se describen las directrices que usa el proveedor de servicios de directorio para asignar Active Directory a clases WMI:

-   Cada clase abstracta del esquema Active Directory asigna a una clase abstracta en el esquema WMI.

    En el esquema WMI, cada clase abstracta tiene el prefijo DS \_ . Por ejemplo, la **clase person** del esquema Active Directory asigna a la clase WMI **\_ de persona DS.**

-   Cada clase no existente del esquema Active Directory asigna a las dos clases siguientes del esquema WMI:

    -   La primera clase asignada tiene el prefijo ADS \_ . Se trata de clases abstractas, asignadas según las reglas siguientes.
    -   La segunda clase asignada es una clase noabstract con el prefijo de \_ nombre DS. Esta clase se deriva de la clase \_ abstracta ADS, con la adición del [**calificador Provider.**](/windows/desktop/api/Provider/nl-provider-provider)

    Por ejemplo, la **clase de** usuario del esquema Active Directory asigna a dos clases. La primera clase es la clase **\_ abstracta de usuario** ads, asignada según las reglas siguientes. La segunda clase es la clase no administradora del usuario **DS. \_** Se deriva del usuario **ads \_ y** tiene el [**calificador Provider**](/windows/desktop/api/Provider/nl-provider-provider) agregado.

-   A menos que se especifique lo contrario, el nombre de una clase asignada es el valor desasignado de la propiedad **LDAP-Display-Name** de la Active Directory asignación.
-   Si la **propiedad Sub-Class-Of** está presente en la clase Active Directory, la clase asignada a WMI se deriva de la clase especificada.

    Si la **propiedad Sub-Class-Of** no está presente, la clase asignada a WMI se deriva de la clase raíz LDAP de **DS, \_ \_ \_** tal como se especifica en el archivo MOF.

    > [!Note]  
    > Esta clase tiene la **propiedad de clave ADSIPath,** con un tipo **VT \_ BSTR**. Esta es la ruta de acceso adsi única que identifica esta instancia. Active Directory solo admite la herencia única, por lo que esto funciona.

     

-   Se **crea un** calificador dinámico de tipo VT **\_ BOOL** y un tipo establecido en `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` **TRUE** para cada clase. Se trata de un calificador WMI estándar que indica que las instancias de esta clase se proporcionan dinámicamente.
-   Si la clase no es abstracta, el proveedor crea un calificador [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) de tipo **VT \_ BSTR BOOL** y un tipo de calificador establecido en `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` "DS Instance Provider" para cada clase. Se trata de un calificador WMI estándar que indica el nombre del proveedor que proporciona dinámicamente instancias de esta clase.

El resto de las propiedades adsi se asignan a calificadores de clase y propiedades según las tablas siguientes. Todos los calificadores se asignan con un valor de marca calificador de `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` .

A continuación se muestra información de asignación para la clase Active Directory, que muestra el calificador WMI y el tipo de calificador WMI para cada Active Directory propiedad.

<dl> <dt>

**Common-Name**
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

**Governs-Id**
</dt> <dd>

**GovernsId** (**VT \_ BSTR**)

Asignado a partir de la representación de cadena del OID; por ejemplo, "{ 1 3 3 6 }".

</dd> <dt>

**Object-Class**
</dt> <dd>

N/D

No asignado.

</dd> <dt>

**Object-Class-Category**
</dt> <dd>

**ObjectClassCategory** (**VT \_ I4**)

Asignado directamente desde el valor entero. Además, si el valor es Abstract(2), también se crea el calificador **CIM \_ DE VT BOOL** estándar, denominado calificador **"Abstract".**

</dd> <dt>

**RDN-ATT-ID**
</dt> <dd>

**RDNATTID** (**VT \_ BSTR**)

Asignado a partir de la representación de cadena del valor OID; por ejemplo, "{ 1 3 3 6 }". Además, la propiedad identificada aquí se anota con el calificador CIM **indexado** estándar establecido en **TRUE.**

</dd> <dt>

**Solo sistema**
</dt> <dd>

**SystemOnly** (**VT \_ BOOL**)

Se asigna directamente desde el valor booleano.

</dd> </dl>

 

A continuación se enumeran las Active Directory de clase asignadas a las propiedades de clase WMI.

<dl> <dt>

**Puede contener**
</dt> <dd>

Cada propiedad de esta lista se asigna a una propiedad WMI.

</dd> <dt>

**Must-Contain**
</dt> <dd>

Cada propiedad de esta lista se asigna a una propiedad WMI. Se crea **el \_ calificador** CIM not null estándar para cada uno de ellos.

</dd> <dt>

**System-May-Contain**
</dt> <dd>

Cada propiedad de esta lista se asigna a una propiedad WMI. Además, cada propiedad se anota con un calificador **system,** establecido en **TRUE.**

</dd> <dt>

**Debe contener el sistema**
</dt> <dd>

Cada propiedad de esta lista se asigna a una propiedad WMI. Se crea **el \_ calificador** CIM not null estándar para cada uno de ellos. Además, cada propiedad se anota con un calificador **system,** establecido en **TRUE.**

</dd> </dl>

## <a name="mapping-attributes"></a>Atributos de asignación

El proveedor de Servicios de directorio asigna cada atributo de una clase Active Directory a exactamente una propiedad de la clase WMI correspondiente según las reglas de esta sección. En general, el proveedor de servicios de directorio asigna a la propiedad WMI el nombre de la versión modificada del valor **LDAP-Display-Name** del atributo Active Directory ldap.

Si la Active Directory propiedad **Is-Single-Valued** es **FALSE,** esta propiedad WMI se combina con el operador OR con **CIM FLAG \_ \_ ARRAY**. Tenga en cuenta que cada propiedad se etiqueta con el **\_ calificador VT BSTR,** **ADSyntax**. Representa la sintaxis Active Directory subyacente.

En la tabla siguiente se muestra la asignación de la sintaxis Active Directory al tipo de datos de propiedad WMI.



| Active Directory elemento                                      | Tipo de datos WMI                                                           |
|---------------------------------------------------------------|-------------------------------------------------------------------------|
| [**Punto de acceso**](/windows/desktop/ADSchema/s-object-access-point)            | **CIM \_ STRING**                                                         |
| [**Booleana**](/windows/desktop/ADSchema/s-boolean)                             | **CIM \_ BOOLEAN**                                                        |
| **Cadena que no tiene en cuenta mayúsculas de minúsculas**                                   | **CIM \_ STRING**                                                         |
| [**Cadena que distingue mayúsculas de minúsculas**](/windows/desktop/ADSchema/s-string-case-sensitive) | **CIM \_ STRING**                                                         |
| [**Nombre distintivo**](/windows/desktop/ADSchema/s-object-ds-dn)             | **CIM \_ STRING**                                                         |
| [**DN-Binary**](/windows/desktop/ADSchema/s-object-dn-binary)                  | Objeto incrustado de la **clase DN \_ con \_ binario** definido a continuación.<br/> |
| [**Cadena DN**](/windows/desktop/ADSchema/s-object-dn-string)                  | Objeto incrustado de la **clase DN \_ con la \_ cadena** definida a continuación.<br/> |
| [**Enumeración**](/windows/desktop/ADSchema/s-enumeration)                     | **CIM \_ SINT32**                                                         |
| [**Enumeración**](/windows/desktop/ADSchema/s-enumeration)                     | **CIM \_ STRING**                                                         |
| [**Entero**](/windows/desktop/ADSchema/s-integer)                             | **CIM \_ SINT32**                                                         |
| [**LargeInteger**](/windows/desktop/ADSchema/s-largeinteger)                   | **CIM \_ STRING**                                                         |
| Descriptor de seguridad                                           | Objeto incrustado de la **clase Uint8Array** definido a continuación.<br/>       |
| Cadena numérica                                                | **CIM \_ STRING**                                                         |
| Identificador de objeto                                                     | **CIM \_ STRING**                                                         |
| Octet String                                                  | Objeto incrustado de la **clase Uint8Array** definido a continuación.<br/>       |
| Nombre OR                                                       | **CIM \_ STRING**                                                         |
| Presentation-Address                                          | Objeto incrustado de la **clase Uint8Array** definido a continuación.<br/>       |
| Cadena de mayúsculas y minúsculas de impresión                                             | **CIM \_ STRING**                                                         |
| Vínculo de réplica                                                  | Objeto incrustado de la **clase Uint8Array** definido a continuación.<br/>       |
| [**String(Sid)**](/windows/desktop/ADSchema/s-string-sid)                      | Objeto incrustado de la **clase Uint8Array** definido a continuación.<br/>       |
| Time                                                          | **CIM \_ DATETIME**                                                       |
| Hora codificada UTC                                                | **CIM \_ DATETIME**                                                       |
| Cadena Unicode                                                | **CIM \_ STRING**                                                         |



 

La sintaxis de cadena de octeto, que hace referencia a una matriz de valores **uint8,** presenta un problema cuando se asigna a WMI porque WMI permite propiedades de tipos **uint8** y matrices de **uint8,** mientras que Active Directory permite propiedades de tipo Octet String, así como matrices de Octet String.

En el ejemplo siguiente se muestra la clase Proveedor de servicios de directorio que se usa para asignar una matriz de propiedades de tipo Octet String.

``` syntax
Class Uint8Array 
{
    uint8 values[];
    uint32 numberOfValues;
};
```

WMI asigna todos los valores de propiedad string Active Directory octetos a instancias incrustadas de **Uint8Array**. De forma similar, WMI asigna matrices de Octet String a matrices de **objetos Uint8Array incrustados.**

En el ejemplo siguiente se muestran las clases asignadas por WMI para DN-Binary y DN-String de propiedad DS.

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

En la tabla siguiente se muestra cómo WMI asigna el resto de las propiedades Active Directory interfaz de atributo a calificadores de propiedad WMI.



| Active Directory nombre de la propiedad de atributo | Calificador WMI       | Tipo de datos    | Información de asignación                               |
|------------------------------------------|---------------------|--------------|---------------------------------------------------|
| **Sintaxis de atributos**                     | **AttributeSyntax** | **VT \_ BSTR** | Asignado a partir de la representación de cadena del OID. |
| **Common-Name**                          | **CN**              | **VT \_ BSTR** | Asignado a partir del valor de cadena.                     |
| **Solo sistema**                          | **Sistema**          | **VT \_ BOOL** | Asignado a partir del valor booleano.                    |



 

> [!Note]  
> WMI asigna todos los Active Directory calificadores con las clases `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` de calificador.

 

## <a name="association-classes"></a>Clases de asociación

El servicio de directorio es básicamente un almacén jerárquico de objetos. Los objetos que pueden aparecer en un nivel no pan en la jerarquía se denominan "contenedores". La estructura de esta jerarquía se controla aún más mediante las propiedades "Poss-Superiors" y "System-Poss-Superiors" de una clase del esquema. Estos, juntos, especifican el conjunto de clases cuyas instancias se pueden contener dentro de una instancia de una clase contenedora.

En el ejemplo siguiente se modela una asociación CIM como instancias de la clase de asociación [**estática DS \_ LDAP Class \_ \_ Containment**](/previous-versions/windows/desktop/dsprov/ds-ldap-class-containment).

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

El proveedor de clases de asociación [**admite los métodos GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) [**y CreateClassEnumAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)

 

