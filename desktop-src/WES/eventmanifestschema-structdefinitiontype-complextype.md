---
title: Tipo complejo StructDefinitionType
description: Define una estructura que incluye uno o varios elementos de datos que desea incluir con el evento . | Tipo complejo StructDefinitionType
ms.assetid: eb6b3682-1035-472b-8027-583d43c31748
keywords:
- EventLog de tipo complejo StructDefinitionType
topic_type:
- apiref
api_name:
- StructDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 01e739077d38dec94c0a407e5779bec90369ffb9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476288"
---
# <a name="structdefinitiontype-complex-type"></a>Tipo complejo StructDefinitionType

Define una estructura que incluye uno o varios elementos de datos que desea incluir con el evento .

``` syntax
<xs:complexType name="StructDefinitionType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="data"
            type="DataDefinitionType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
        use="required"
     />
    <xs:attribute name="length"
        type="LengthType"
        use="optional"
     />
    <xs:attribute name="count"
        type="CountType"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                               | Tipo                                                                             | Descripción                                                               |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [**Datos**](eventmanifestschema-data-structdefinitiontype-element.md) | [**DataDefinitionType**](eventmanifestschema-datadefinitiontype-complextype.md) | Define un elemento de datos que desea incluir en la estructura .<br/> |



## <a name="attributes"></a>Atributos



| Nombre   | Tipo                                                            | Descripción                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| count  | [**CountType**](eventmanifestschema-counttype-simpletype.md)   | Número de elementos de una matriz de estructuras. Este atributo indica que la estructura está definiendo una matriz de estructuras. Puede especificar el recuento real o el nombre de un elemento de datos fuera de la estructura que contiene el recuento. <br/>                               |
| length | [**LengthType**](eventmanifestschema-lengthtype-simpletype.md) | No disponible.<br/> **Windows Server 2008 y Windows Vista:** Longitud de esta estructura, en bytes. No disponible a partir de Windows 7.<br/>                                                                                                                            |
| name   | string                                                          | Nombre de la estructura. Puede usar el nombre para hacer referencia al elemento de datos en el fragmento XML si especifica una [**sección UserData**](eventmanifestschema-userdata-templateitemtype-element.md) en la plantilla.<br/> **Windows Vista:** Este atributo es opcional.<br/> |



## <a name="remarks"></a>Observaciones

Los proveedores escriben la estructura como un blob y no como miembros individuales de la estructura. Si la estructura de C que está escribiendo contiene punteros (por ejemplo, un puntero de tipo LPWSTR), los datos del evento contendrán el valor del puntero, no los datos desreferenciados.

No debe usar estructuras, sino que debe definir elementos de datos para cada miembro y escribirlos por separado. Si decide usar structure, la estructura solo debe contener tipos enteros y debe asegurarse de que los miembros de la estructura se alinean con un límite de 8 bytes. Si no lo hace, es probable que reciba errores de alineación al intentar acceder a los datos. Considere la posibilidad de \# usar la directiva pragma pack() para forzar la alineación en un límite de 8 bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





