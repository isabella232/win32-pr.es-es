---
description: Novedades de Windows 7. Identifica una propiedad que está relacionada con la propiedad definida en el archivo de descripción de la propiedad.
ms.assetid: 30167942-141A-4f37-B019-0811BA654124
title: relatedProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cabde093a47a25834598659d3ad38e0847c1351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360559"
---
# <a name="relatedproperty"></a>relatedProperty

Novedades de Windows 7. Identifica una propiedad que está relacionada con la propiedad definida en el archivo de descripción de la propiedad. Puede haber tantos elementos [relatedProperty]() dentro de un [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) como sea necesario.

## <a name="syntax"></a>Sintaxis


```
<!-- relatedPropertyInfo -->
<xs:element name="relatedProperty" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:attribute name="relationshipName" type="canonical-name" use="required"/>
        <xs:attribute name="propertyName" type="canonical-name" use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Información de elemento



| Elemento primario                                                   | Elementos secundarios |
|------------------------------------------------------------------|----------------|
| [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) | None           |



 

## <a name="attributes"></a>Atributos



| Atributo        | Descripción                                                        |
|------------------|--------------------------------------------------------------------|
| relationshipName | Público. Obligatorio. Nombre canónico de la relación de propiedad. |
| propertyName     | Público. Obligatorio. Nombre canónico de la propiedad relacionada.      |



 

## <a name="remarks"></a>Observaciones

Este elemento le permite asignar una propiedad a otra. Por ejemplo, puede asignar el texto de su propiedad personalizada, fabrikam. StorageCapacity, a System. Capacity:


```
<!-- relatedPropertyInfo -->
<propertyDescription name="Fabrikam.StorageCapacity" ... >
    ...
    <relatedPropertyInfo>
        <relatedProperty relationshipName="System.RelatedProperty.Text" propertyName="System.Capacity"/>
    </relatedPropertyInfo>
</propertyDescription>
```



 

 
