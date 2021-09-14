---
description: En este tema se presenta el esquema de descripción de propiedades utilizado por el sistema de propiedades de Shell.
ms.assetid: cac93c31-d90d-4116-b846-0cf593d1d56e
title: Descripción del esquema de descripción de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51d9e7c2b6fb4b599f977c0c49ad1cb2514fe8d8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361090"
---
# <a name="understanding-the-property-description-schema"></a>Descripción del esquema de descripción de propiedades

En este tema se presenta el esquema de descripción de propiedades utilizado por el sistema de propiedades de Shell.

La introducción de nuevas características para Windows Vista y versiones posteriores requería que el sistema de propiedades de Shell existente se ampliara a:

-   Admite un sistema de descripción de propiedades enriquecido y extensible que proporciona información sobre las propiedades, incluidos los nombres para mostrar, el tipo, el tipo de presentación, el comportamiento de ordenación y grupo, y otros atributos necesarios para presentar y operar sobre las propiedades.
-   Admite una lista de valores de tipos de propiedades (combinada con la interfaz de usuario que puede editar esos tipos en distintas vistas, como la vista de lista, el panel de vista previa, los cuadros de diálogo de propiedades, entre otros) que se pueden asociar a varias propiedades.
-   Proporcione listas de descripción de propiedades, que definen el conjunto de propiedades que se muestran en varias vistas.
-   Proporcione una interfaz simplificada, [**IPropertyStore,**](/windows/win32/api/propsys/nn-propsys-ipropertystore)para que los controladores de propiedades se puedan escribir más fácilmente y para que las propiedades se puedan conservar en archivos.
-   Compatibilidad con controladores de propiedades que no son de archivo para exponer propiedades en la vista.

Estas características se logran en una arquitectura que proporciona acceso abstracto a las propiedades de un elemento de Shell. Esta abstracción se denomina sistema de propiedades de Shell.

-   [¿Qué es el esquema de descripción de la propiedad?](#what-is-the-property-description-schema)
-   [¿Por qué usar un esquema?](#why-use-a-schema)
-   [¿Cuáles son las partes principales del esquema?](#what-are-the-major-schema-parts)
-   [Cambios para Windows 7](#changes-for-windows-7)
-   [Temas relacionados](#related-topics)

## <a name="what-is-the-property-description-schema"></a>¿Qué es el esquema de descripción de la propiedad?

El subsistema de esquema consta de lo siguiente:

-   Uno o varios archivos de esquema .propdesc que definen descripciones de propiedades. El esquema de descripción de propiedad se define en una colección de archivos de esquema XML (mediante la extensión de archivo .propdesc) en tiempo de ejecución en el sistema. Estos archivos se cargan de forma diferida cuando una parte del sistema de propiedades los requiere.
-   Memoria caché de esquemas en memoria que se usa para almacenar los archivos de esquema analizadas, que incluyen todas las descripciones de propiedades introducidas en el subsistema. No es necesario volver a utilizar los archivos de configuración .propdesc que describen el esquema. Para obtener más información, [**vea PSRegisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema), [**PSUnregisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psunregisterpropertyschema)y [**PSRefreshPropertySchema**](/windows/win32/api/propsys/nf-propsys-psrefreshpropertyschema).
-   Objeto de subsistema que implementa [**IPropertySystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem), que se usa para obtener o trabajar con descripciones de propiedades.
-   Objeto de subsistema que implementa [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription), que se usa para informar y operar en función de una descripción de propiedad.
-   Objeto de subsistema que implementa [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), que se usa como una colección de descripciones de propiedades.

> [!Note]  
> Debe agregar al `xmlns=http://schemas.microsoft.com/windows/2006/propertydescription` elemento de esquema raíz de los archivos .propdesc.

 

## <a name="why-use-a-schema"></a>¿Por qué usar un esquema?

Las propiedades, por sí mismas, no son seguras para tipos. Un componente puede asignar un valor numérico a la propiedad System.Author o una marca de [**fecha FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) al sistema. Música. Propiedad AlbumTitle y, sin ninguna otra aplicación ni guía, los almacenes de propiedades la permitirán. Por lo tanto, necesitamos una noción para "esquematizar" las propiedades, lo que nos lleva al subsistema de esquema.

## <a name="what-are-the-major-schema-parts"></a>¿Cuáles son las partes principales del esquema?

El esquema de descripción de propiedades utilizado por el sistema de propiedades de Shell se compone de un único elemento [propertyDescriptionList,](./propdesc-schema-propertydescriptionlist.md) así como un atributo *schemaVersion,* que indica la versión de este formato de definición de esquema. Nota: el valor debe ser "1.0".


```
<!-- schema -->
    <xs:element name="schema">
      <xs:complexType>
        <xs:sequence>
          <xs:element ref="propertyDescriptionList" minOccurs="1" maxOccurs="1"/>
        </xs:sequence>
        <xs:attribute name="schemaVersion"  type="xs:string"/>
      </xs:complexType>
    </xs:element>
```



[PropertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) se compone de uno o varios [elementos propertyDescription,](./propdesc-schema-propertydescription.md) así como atributos *de publicador* *y producto.*


```
<!-- propertyDescriptionList -->
    <xs:element name="propertyDescriptionList">
      <xs:complexType>
        <xs:sequence>
          <xs:element ref="propertyDescription" minOccurs="1" maxOccurs="unbounded"/>
        </xs:sequence>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product"   type="xs:string"/>
      </xs:complexType>
    </xs:element>
```



Una [propiedadDescription](./propdesc-schema-propertydescription.md) se compone de un [elemento searchInfo](./propdesc-schema-searchinfo.md) y cero o un elemento [labelInfo,](./propdesc-schema-labelinfo.md) [typeInfo](./propdesc-schema-typeinfo.md)y [displayInfo,](./propdesc-schema-displayinfo.md) así como los atributos *formatID,* *propID,* *propstr* y *name.*

Debe haber un [elemento propertyDescription](./propdesc-schema-propertydescription.md) para cada nombre de propiedad canónica único que esté diseñado para estar disponible en el sistema. Los atributos de cadena tienen un límite de 512 caracteres. Los valores de más de 512 caracteres se truncan.


```
<!-- propertyDescription -->
    <xs:element name="propertyDescription">
      <xs:complexType>
        <xs:all>
          <xs:element name="description"    type="xs:string" minOccurs="0" maxOccurs="1"/>
          <xs:element ref="searchInfo"   minOccurs="1" maxOccurs="1"/>
          <xs:element ref="labelInfo"    minOccurs="0" maxOccurs="1"/>
          <xs:element ref="typeInfo"     minOccurs="0" maxOccurs="1"/>
          <xs:element ref="displayInfo"  minOccurs="0" maxOccurs="1"/>
        </xs:all>
        <xs:attribute name="formatID"  type="upcase-uuid" use="required""/>
        <xs:attribute name="propID"    type="xs:nonNegativeInteger" use="required""/>
        <xs:attribute name="name"      type="canonical-name" use="required"/>
      </xs:complexType>
    </xs:element>
```



## <a name="changes-for-windows-7"></a>Cambios para Windows 7

El esquema de descripción de la propiedad se ha cambiado para Windows 7. Se trata de cambios no importantes. Si un elemento o atributo de propiedad ya no se admite en Windows 7, el sistema operativo Windows 7 omite el elemento o atributos Windows Vista. De forma similar, Windows Vista omite los nuevos Windows 7 elementos o atributos de propiedad.

Sin embargo, se recomienda actualizar las propiedades personalizadas Windows 7 para una experiencia de usuario mejor y más coherente.

Los siguientes son nuevos elementos y atributos:

-   [elementos relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) [y relatedProperty](./propdesc-schema-relatedproperty.md)
-   [elemento image](./propdesc-schema-image.md)
-   Atributo mnemonics del [elemento searchInfo](./propdesc-schema-searchinfo.md)
-   Atributo mnemonics del elemento [enum](./propdesc-schema-enum.md)
-   Atributo searchRawValue del [elemento typeInfo](./propdesc-schema-typeinfo.md)

Los siguientes elementos y atributos han cambiado:

-   [enumeratedList,](./propdesc-schema-enumeratedlist.md) [enum](./propdesc-schema-enum.md)y [enumRange,](./propdesc-schema-enumrange.md) elementos
-   [elemento drawControl](./propdesc-schema-drawcontrol.md)
-   [elemento editControl](./propdesc-schema-editcontrol.md)
-   Atributo propID del [elemento propertyDescription](./propdesc-schema-propertydescription.md)
-   Atributo columnIndexType del [elemento searchInfo](./propdesc-schema-searchinfo.md)

Se han quitado los siguientes elementos y atributos:

-   [elemento queryControl](./propdesc-schema-querycontrol.md)
-   Atributo isQueryable del [elemento typeInfo](./propdesc-schema-typeinfo.md)
-   Atributo includeInFullTextQuery del [elemento typeInfo](./propdesc-schema-typeinfo.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[typeInfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[stringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[numberFormat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[filterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> <dt>

[image](./propdesc-schema-image.md)
</dt> </dl>

 

 
