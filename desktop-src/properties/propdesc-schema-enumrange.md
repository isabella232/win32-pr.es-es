---
description: Asigna texto de enumeración a un intervalo de valores. Cada elemento enumRange especifica un valor mínimo y se extiende hasta el valor mínimo del elemento siguiente, o hasta que no hay más elementos enumRange.
ms.assetid: 00c56c2d-6693-4b09-b28a-21d69930bf35
title: enumRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 964835c376c5496d23e8d277409575758002a0d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001573"
---
# <a name="enumrange"></a>enumRange

Asigna texto de enumeración a un intervalo de valores. Cada elemento [enumRange]() especifica un valor mínimo y se extiende hasta el valor mínimo del elemento siguiente, o hasta que no hay más elementos enumRange.

## <a name="syntax"></a>Sintaxis

``` syntax
<!-- enumRange -->
<xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="image" minOccurs="0" maxOccurs="1"/>
        </xs:sequence>
            <xs:attribute name="minValue" type="xs:integer" use="required"/>
            <xs:attribute name="setValue" type="xs:integer"/>
            <xs:attribute name="text" type="xs:string"/>
            <xs:attribute name="name" type="canonical-name"/> <!--Maximum of 64 characters-->
            <xs:attribute name="mnemonics" type="xs:string"/> 
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a>Información de elemento



| Elemento primario                                         | Elementos secundarios |
|--------------------------------------------------------|----------------|
| [enumeratedList](./propdesc-schema-enumeratedlist.md) | ninguno           |



 

## <a name="attributes"></a>Atributos



| Atributo | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| minValue  | Público. Obligatorio. Valor mínimo del intervalo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| setValue  | Público. Opcional. Cuando un usuario selecciona esta enumeración desde un control de propiedad ListBox, este valor discreto se asigna como el valor de propiedad.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| text      | Público. Opcional. Texto que se usa para mostrar el valor enumerado. La sintaxis permite una cadena de presentación directa o una referencia de cadena de presentación indirecta; Utilice la cadena de presentación indirecta para que se pueda localizar.                                                                                                                                                                                                                                                                                                                                                                                                   |
| teclas de acceso | **Windows 7 y versiones posteriores.** Público. Opcional. Una lista de valores de tecla de tecla que se pueden usar para hacer referencia a la propiedad en consultas de búsqueda. La lista está delimitada por el \| carácter ' '.                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| name      | Necesario. Nombre canónico de la propiedad, único para el sistema; por ejemplo, System. Rating. Este atributo está limitado a 64 caracteres. El nombre distingue mayúsculas de minúsculas y debe usar la sintaxis siguiente: Publisher. Application. PropertyName. Los métodos siguientes devuelven este valor: [**IExplorerCommand:: GetCanonicalName**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getcanonicalname), [**IPropertyDescription:: GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname), [**IPropertyDescription2:: GetCanonicalName**](/windows/desktop/api/Propsys/nn-propsys-ipropertydescription2)y [**IPropertyUI:: GetCanonicalName**](/previous-versions/windows/desktop/legacy/dd758076(v=vs.85)). |



 

 

 
