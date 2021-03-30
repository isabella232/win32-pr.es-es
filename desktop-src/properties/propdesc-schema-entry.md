---
description: En este tema se presenta el esquema de descripción de propiedades que usa el sistema de propiedades de Shell.
ms.assetid: cac93c31-d90d-4116-b846-0cf593d1d56e
title: Descripción del esquema de descripción de propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51d9e7c2b6fb4b599f977c0c49ad1cb2514fe8d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082421"
---
# <a name="understanding-the-property-description-schema"></a><span data-ttu-id="4e451-103">Descripción del esquema de descripción de propiedad</span><span class="sxs-lookup"><span data-stu-id="4e451-103">Understanding the Property Description Schema</span></span>

<span data-ttu-id="4e451-104">En este tema se presenta el esquema de descripción de propiedades que usa el sistema de propiedades de Shell.</span><span class="sxs-lookup"><span data-stu-id="4e451-104">This topic introduces the property description schema used by the Shell property system.</span></span>

<span data-ttu-id="4e451-105">La introducción de nuevas características para Windows Vista y versiones posteriores requería que el sistema de propiedades de Shell existente se extienda a:</span><span class="sxs-lookup"><span data-stu-id="4e451-105">The introduction of new features for Windows Vista and later required that the existing Shell property system be extended to:</span></span>

-   <span data-ttu-id="4e451-106">Admite un sistema de descripción de propiedades enriquecido y extensible que proporciona información sobre las propiedades, incluidos los nombres para mostrar, el tipo, el tipo de presentación, el comportamiento de ordenación y de grupo, y otros atributos necesarios para presentar y operar sobre las propiedades.</span><span class="sxs-lookup"><span data-stu-id="4e451-106">Support a rich and extensible property description system that provides information about properties including display names, type, display type, sort and group behavior, and other attributes needed to present and operate over the properties.</span></span>
-   <span data-ttu-id="4e451-107">Admite una lista de acciones de tipos de propiedad (combinada con la interfaz de usuario que puede editar esos tipos en vistas diferentes, como ListView, panel de vista previa, cuadros de diálogo de propiedades, etc.) que se pueden asociar a diversas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4e451-107">Support a stock list of property types (combined with UI that can edit those types in different views like the listview, preview pane, property dialogs, and so on) that can be associated with various properties.</span></span>
-   <span data-ttu-id="4e451-108">Proporcione listas de descripción de propiedades, que definen el conjunto de propiedades que se muestran en varias vistas.</span><span class="sxs-lookup"><span data-stu-id="4e451-108">Supply property description lists, which define the set of properties displayed in various views.</span></span>
-   <span data-ttu-id="4e451-109">Proporcionar una interfaz simplificada, [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore), por lo que los controladores de propiedades se pueden escribir más fácilmente y, por tanto, las propiedades se pueden conservar en los archivos.</span><span class="sxs-lookup"><span data-stu-id="4e451-109">Provide a simplified interface, [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore), so property handlers can be written more easily and so properties can be persisted to files.</span></span>
-   <span data-ttu-id="4e451-110">Compatibilidad con controladores de propiedades que no son de archivo para exponer propiedades en la vista.</span><span class="sxs-lookup"><span data-stu-id="4e451-110">Support for non-file property handlers to expose properties in the view.</span></span>

<span data-ttu-id="4e451-111">Estas características se logran en una arquitectura que proporciona acceso abstracto a las propiedades de un elemento de Shell.</span><span class="sxs-lookup"><span data-stu-id="4e451-111">These features are achieved on an architecture that provides abstract access to the properties of a Shell item.</span></span> <span data-ttu-id="4e451-112">Esta abstracción se denomina sistema de propiedades de Shell.</span><span class="sxs-lookup"><span data-stu-id="4e451-112">This abstraction is called the Shell property system.</span></span>

-   [<span data-ttu-id="4e451-113">¿Cuál es el esquema de descripción de la propiedad?</span><span class="sxs-lookup"><span data-stu-id="4e451-113">What Is the Property Description Schema?</span></span>](#what-is-the-property-description-schema)
-   [<span data-ttu-id="4e451-114">¿Por qué usar un esquema?</span><span class="sxs-lookup"><span data-stu-id="4e451-114">Why Use a Schema?</span></span>](#why-use-a-schema)
-   [<span data-ttu-id="4e451-115">¿Cuáles son los elementos de esquema principales?</span><span class="sxs-lookup"><span data-stu-id="4e451-115">What Are the Major Schema Parts?</span></span>](#what-are-the-major-schema-parts)
-   [<span data-ttu-id="4e451-116">Cambios para Windows 7</span><span class="sxs-lookup"><span data-stu-id="4e451-116">Changes for Windows 7</span></span>](#changes-for-windows-7)
-   [<span data-ttu-id="4e451-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4e451-117">Related topics</span></span>](#related-topics)

## <a name="what-is-the-property-description-schema"></a><span data-ttu-id="4e451-118">¿Cuál es el esquema de descripción de la propiedad?</span><span class="sxs-lookup"><span data-stu-id="4e451-118">What Is the Property Description Schema?</span></span>

<span data-ttu-id="4e451-119">El subsistema de esquema consta de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="4e451-119">The schema subsystem consists of the following:</span></span>

-   <span data-ttu-id="4e451-120">Uno o varios archivos de esquema. propDesc que definen descripciones de propiedad.</span><span class="sxs-lookup"><span data-stu-id="4e451-120">One or more .propdesc schema files that define property descriptions.</span></span> <span data-ttu-id="4e451-121">El esquema de descripción de propiedad se define en una colección de archivos de esquema XML (con la extensión de archivo. propDesc) en tiempo de ejecución en el sistema.</span><span class="sxs-lookup"><span data-stu-id="4e451-121">The property description schema is defined in a collection of XML schema files (using the .propdesc file extension) at runtime on the system.</span></span> <span data-ttu-id="4e451-122">Estos archivos se cargan de forma diferida cuando una parte del sistema de propiedades los requiere.</span><span class="sxs-lookup"><span data-stu-id="4e451-122">These files are lazy-loaded when a part of the property system requires them.</span></span>
-   <span data-ttu-id="4e451-123">Caché de esquema en memoria que se usa para almacenar los archivos de esquema analizados, que incluyen todas las descripciones de propiedades introducidas en el subsistema.</span><span class="sxs-lookup"><span data-stu-id="4e451-123">An in-memory schema cache used to store the parsed schema files, which include all property descriptions introduced to the subsystem.</span></span> <span data-ttu-id="4e451-124">No es necesario volver a analizar los archivos de configuración. propDesc que describen el esquema.</span><span class="sxs-lookup"><span data-stu-id="4e451-124">There is no need to reparse the .propdesc config files that describe the schema.</span></span> <span data-ttu-id="4e451-125">Para obtener más información, vea [**PSRegisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema), [**PSUnregisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psunregisterpropertyschema)y [**PSRefreshPropertySchema**](/windows/win32/api/propsys/nf-propsys-psrefreshpropertyschema).</span><span class="sxs-lookup"><span data-stu-id="4e451-125">For more information, see [**PSRegisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema), [**PSUnregisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psunregisterpropertyschema), and [**PSRefreshPropertySchema**](/windows/win32/api/propsys/nf-propsys-psrefreshpropertyschema).</span></span>
-   <span data-ttu-id="4e451-126">Objeto de subsistema que implementa [**IPropertySystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem), que se usa para obtener o trabajar con descripciones de propiedad.</span><span class="sxs-lookup"><span data-stu-id="4e451-126">A subsystem object that implements [**IPropertySystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem), which is used to obtain or work with property descriptions.</span></span>
-   <span data-ttu-id="4e451-127">Objeto de subsistema que implementa [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription), que se usa para informar y operar en función de una descripción de propiedad.</span><span class="sxs-lookup"><span data-stu-id="4e451-127">A subsystem object that implements [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription), which is used to inform and operate based on a property description.</span></span>
-   <span data-ttu-id="4e451-128">Objeto de subsistema que implementa [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), que se utiliza como una colección de descripciones de propiedad.</span><span class="sxs-lookup"><span data-stu-id="4e451-128">A subsystem object that implements [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), which is used as a collection of property descriptions.</span></span>

> [!Note]  
> <span data-ttu-id="4e451-129">Debe agregar `xmlns=http://schemas.microsoft.com/windows/2006/propertydescription` al elemento Schema raíz de los archivos. propDesc.</span><span class="sxs-lookup"><span data-stu-id="4e451-129">You must add `xmlns=http://schemas.microsoft.com/windows/2006/propertydescription` to the root schema element of your .propdesc files.</span></span>

 

## <a name="why-use-a-schema"></a><span data-ttu-id="4e451-130">¿Por qué usar un esquema?</span><span class="sxs-lookup"><span data-stu-id="4e451-130">Why Use a Schema?</span></span>

<span data-ttu-id="4e451-131">Las propiedades, por sí mismas, no tienen seguridad de tipos.</span><span class="sxs-lookup"><span data-stu-id="4e451-131">Properties, by themselves, are not type-safe.</span></span> <span data-ttu-id="4e451-132">Un componente puede asignar un valor numérico a la propiedad System. Author o una marca de fecha de [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) a la propiedad System. Music. álbum y, sin ninguna otra exigencia o orientación, los almacenes de propiedades lo permitirán.</span><span class="sxs-lookup"><span data-stu-id="4e451-132">A component can assign a numerical value to the System.Author property, or a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) date-stamp to the System.Music.AlbumTitle property, and, without any further enforcement or guidance, the property stores will allow it.</span></span> <span data-ttu-id="4e451-133">Por lo tanto, se necesitaba una noción de "schematize" de las propiedades, que nos lleva al subsistema de esquema.</span><span class="sxs-lookup"><span data-stu-id="4e451-133">So, we needed a notion to "schematize" the properties, which brings us to the schema subsystem.</span></span>

## <a name="what-are-the-major-schema-parts"></a><span data-ttu-id="4e451-134">¿Cuáles son los elementos de esquema principales?</span><span class="sxs-lookup"><span data-stu-id="4e451-134">What Are the Major Schema Parts?</span></span>

<span data-ttu-id="4e451-135">El esquema de descripción de la propiedad que usa el sistema de propiedades de Shell se compone de un único elemento [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) , así como un atributo *schemaVersion* , que indica la versión de este formato de definición de esquema.</span><span class="sxs-lookup"><span data-stu-id="4e451-135">The property description schema used by the Shell property system is composed of a single [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) element, as well as a *schemaVersion* attribute, which indicates the version of this schema definition format.</span></span> <span data-ttu-id="4e451-136">Nota: el valor debe ser "1,0".</span><span class="sxs-lookup"><span data-stu-id="4e451-136">Note: value must be "1.0".</span></span>


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



<span data-ttu-id="4e451-137">El [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) se compone de uno o varios elementos [propertyDescription](./propdesc-schema-propertydescription.md) , así como los atributos del *Editor* y del *producto* .</span><span class="sxs-lookup"><span data-stu-id="4e451-137">The [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) is composed of one or more [propertyDescription](./propdesc-schema-propertydescription.md) elements, as well as *publisher* and *product* attributes.</span></span>


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



<span data-ttu-id="4e451-138">Un [propertyDescription](./propdesc-schema-propertydescription.md) se compone de un elemento [searchInfo](./propdesc-schema-searchinfo.md) y cero o un [labelInfo](./propdesc-schema-labelinfo.md), [typeInfo](./propdesc-schema-typeinfo.md)y [displayInfo](./propdesc-schema-displayinfo.md) , así como los atributos *formatID*, *propID*, *propstr* y *Name* .</span><span class="sxs-lookup"><span data-stu-id="4e451-138">A [propertyDescription](./propdesc-schema-propertydescription.md) is composed of one [searchInfo](./propdesc-schema-searchinfo.md) and zero or one [labelInfo](./propdesc-schema-labelinfo.md), [typeInfo](./propdesc-schema-typeinfo.md), and [displayInfo](./propdesc-schema-displayinfo.md) elements, as well as *formatID*, *propID*, *propstr*, and *name* attributes.</span></span>

<span data-ttu-id="4e451-139">Debe haber un elemento [propertyDescription](./propdesc-schema-propertydescription.md) para cada nombre de propiedad canónico único que esté previsto que esté disponible en el sistema.</span><span class="sxs-lookup"><span data-stu-id="4e451-139">There should be one [propertyDescription](./propdesc-schema-propertydescription.md) element for every unique canonical property name that is intended to be available in the system.</span></span> <span data-ttu-id="4e451-140">Los atributos de cadena tienen un límite de 512 caracteres.</span><span class="sxs-lookup"><span data-stu-id="4e451-140">The string attributes have a limit of 512 characters.</span></span> <span data-ttu-id="4e451-141">Se truncan los valores de más de 512 caracteres.</span><span class="sxs-lookup"><span data-stu-id="4e451-141">Values longer than 512 characters are truncated.</span></span>


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



## <a name="changes-for-windows-7"></a><span data-ttu-id="4e451-142">Cambios para Windows 7</span><span class="sxs-lookup"><span data-stu-id="4e451-142">Changes for Windows 7</span></span>

<span data-ttu-id="4e451-143">El esquema de descripción de la propiedad ha cambiado para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4e451-143">The property description schema has been changed for Windows 7.</span></span> <span data-ttu-id="4e451-144">Se trata de cambios no importantes.</span><span class="sxs-lookup"><span data-stu-id="4e451-144">These are non-breaking changes.</span></span> <span data-ttu-id="4e451-145">Si un elemento o atributo de propiedad ya no se admite en Windows 7, el sistema operativo Windows 7 omite el elemento o los atributos de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4e451-145">If a property element or attribute is no longer supported in Windows 7, the Windows 7 operating system ignores the Windows Vista element or attributes.</span></span> <span data-ttu-id="4e451-146">De forma similar, Windows Vista también omite los nuevos atributos o elementos de propiedad de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4e451-146">Similarly, Windows Vista ignores new Windows 7 property elements or attributes as well.</span></span>

<span data-ttu-id="4e451-147">Sin embargo, se recomienda actualizar las propiedades personalizadas para Windows 7 para ofrecer una experiencia de usuario mejor y más coherente.</span><span class="sxs-lookup"><span data-stu-id="4e451-147">However, updating custom properties for Windows 7 is recommended for a better and more consistent user experience.</span></span>

<span data-ttu-id="4e451-148">A continuación se muestran elementos y atributos nuevos:</span><span class="sxs-lookup"><span data-stu-id="4e451-148">The following are new elements and attributes:</span></span>

-   <span data-ttu-id="4e451-149">elementos [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) y [relatedProperty](./propdesc-schema-relatedproperty.md)</span><span class="sxs-lookup"><span data-stu-id="4e451-149">[relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) and [relatedProperty](./propdesc-schema-relatedproperty.md) elements</span></span>
-   <span data-ttu-id="4e451-150">elemento [Image](./propdesc-schema-image.md)</span><span class="sxs-lookup"><span data-stu-id="4e451-150">[image](./propdesc-schema-image.md) element</span></span>
-   <span data-ttu-id="4e451-151">atributo mnemónicos del elemento [searchInfo](./propdesc-schema-searchinfo.md)</span><span class="sxs-lookup"><span data-stu-id="4e451-151">mnemonics attribute of the [searchInfo](./propdesc-schema-searchinfo.md) element</span></span>
-   <span data-ttu-id="4e451-152">atributo mnemónicos del elemento [enum](./propdesc-schema-enum.md)</span><span class="sxs-lookup"><span data-stu-id="4e451-152">mnemonics attribute of the [enum](./propdesc-schema-enum.md) element</span></span>
-   <span data-ttu-id="4e451-153">atributo searchRawValue del elemento [typeInfo](./propdesc-schema-typeinfo.md)</span><span class="sxs-lookup"><span data-stu-id="4e451-153">searchRawValue attribute of the [typeInfo](./propdesc-schema-typeinfo.md) element</span></span>

<span data-ttu-id="4e451-154">Los siguientes elementos y atributos han cambiado:</span><span class="sxs-lookup"><span data-stu-id="4e451-154">The following elements and attributes have changed:</span></span>

-   <span data-ttu-id="4e451-155">elementos [enumeratedList](./propdesc-schema-enumeratedlist.md), [enum](./propdesc-schema-enum.md)y [enumRange](./propdesc-schema-enumrange.md)</span><span class="sxs-lookup"><span data-stu-id="4e451-155">[enumeratedList](./propdesc-schema-enumeratedlist.md), [enum](./propdesc-schema-enum.md), and [enumRange](./propdesc-schema-enumrange.md) elements</span></span>
-   <span data-ttu-id="4e451-156">elemento [drawControl](./propdesc-schema-drawcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="4e451-156">[drawControl](./propdesc-schema-drawcontrol.md) element</span></span>
-   <span data-ttu-id="4e451-157">elemento [editControl](./propdesc-schema-editcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="4e451-157">[editControl](./propdesc-schema-editcontrol.md) element</span></span>
-   <span data-ttu-id="4e451-158">atributo propID del elemento [propertyDescription](./propdesc-schema-propertydescription.md)</span><span class="sxs-lookup"><span data-stu-id="4e451-158">propID attribute of the [propertyDescription](./propdesc-schema-propertydescription.md) element</span></span>
-   <span data-ttu-id="4e451-159">atributo columnIndexType del elemento [searchInfo](./propdesc-schema-searchinfo.md)</span><span class="sxs-lookup"><span data-stu-id="4e451-159">columnIndexType attribute of the [searchInfo](./propdesc-schema-searchinfo.md) element</span></span>

<span data-ttu-id="4e451-160">Se han quitado los siguientes elementos y atributos:</span><span class="sxs-lookup"><span data-stu-id="4e451-160">The following elements and attributes have been removed:</span></span>

-   <span data-ttu-id="4e451-161">elemento [consulta](./propdesc-schema-querycontrol.md)</span><span class="sxs-lookup"><span data-stu-id="4e451-161">[queryControl](./propdesc-schema-querycontrol.md) element</span></span>
-   <span data-ttu-id="4e451-162">atributo isQueryable del elemento [typeInfo](./propdesc-schema-typeinfo.md)</span><span class="sxs-lookup"><span data-stu-id="4e451-162">isQueryable attribute of the [typeInfo](./propdesc-schema-typeinfo.md) element</span></span>
-   <span data-ttu-id="4e451-163">atributo includeInFullTextQuery del elemento [typeInfo](./propdesc-schema-typeinfo.md)</span><span class="sxs-lookup"><span data-stu-id="4e451-163">includeInFullTextQuery attribute of the [typeInfo](./propdesc-schema-typeinfo.md) element</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e451-164">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4e451-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e451-165">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="4e451-165">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="4e451-166">searchInfo</span><span class="sxs-lookup"><span data-stu-id="4e451-166">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="4e451-167">labelInfo</span><span class="sxs-lookup"><span data-stu-id="4e451-167">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="4e451-168">Requerida</span><span class="sxs-lookup"><span data-stu-id="4e451-168">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="4e451-169">displayInfo</span><span class="sxs-lookup"><span data-stu-id="4e451-169">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="4e451-170">stringFormat</span><span class="sxs-lookup"><span data-stu-id="4e451-170">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="4e451-171">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="4e451-171">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="4e451-172">Numérico</span><span class="sxs-lookup"><span data-stu-id="4e451-172">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="4e451-173">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="4e451-173">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="4e451-174">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="4e451-174">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="4e451-175">drawControl</span><span class="sxs-lookup"><span data-stu-id="4e451-175">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="4e451-176">editControl</span><span class="sxs-lookup"><span data-stu-id="4e451-176">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="4e451-177">filterControl</span><span class="sxs-lookup"><span data-stu-id="4e451-177">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="4e451-178">Consulta</span><span class="sxs-lookup"><span data-stu-id="4e451-178">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="4e451-179">image</span><span class="sxs-lookup"><span data-stu-id="4e451-179">image</span></span>](./propdesc-schema-image.md)
</dt> </dl>

 

 
