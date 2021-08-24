---
description: Novedad de Windows 7. Identifica una propiedad relacionada con la propiedad definida en el archivo de descripción de propiedad.
ms.assetid: 30167942-141A-4f37-B019-0811BA654124
title: relatedProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4285c0f8b0731ba790cd57105f907cd4df85b6faa41c3f649588aca7ef457418
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938685"
---
# <a name="relatedproperty"></a>relatedProperty

Novedad de Windows 7. Identifica una propiedad relacionada con la propiedad definida en el archivo de descripción de propiedad. Puede haber tantos [elementos relatedProperty]() dentro de [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) como sea necesario.

## <a name="syntax"></a>Syntax


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
| [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) | Ninguno           |



 

## <a name="attributes"></a>Atributos



| Atributo        | Descripción                                                        |
|------------------|--------------------------------------------------------------------|
| relationshipName | Público. Obligatorio. Nombre canónico de la relación de propiedad. |
| propertyName     | Público. Obligatorio. Nombre canónico de la propiedad relacionada.      |



 

## <a name="remarks"></a>Comentarios

Este elemento permite asignar una propiedad a otra. Por ejemplo, puede asignar el texto de la propiedad personalizada Fabrikam.StorageCapacity a System.Capacity:


```
<!-- relatedPropertyInfo -->
<propertyDescription name="Fabrikam.StorageCapacity" ... >
    ...
    <relatedPropertyInfo>
        <relatedProperty relationshipName="System.RelatedProperty.Text" propertyName="System.Capacity"/>
    </relatedPropertyInfo>
</propertyDescription>
```



 

 
