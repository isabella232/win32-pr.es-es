---
description: Especifica información acerca de una red de telefonía móvil.
ms.assetid: 52d07b64-7939-4f1c-9793-be07af098053
title: Tipo complejo de providerType (banda ancha móvil)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerType
api_type:
- Schema
ms.openlocfilehash: 1520425cf6ec1bc246f26f2db2d75f79f45a3dae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666505"
---
# <a name="providertype-complex-type"></a>Tipo complejo de providerType

El tipo complejo de **providerType** especifica información sobre una red de telefonía móvil.

``` syntax
<xs:complexType name="providerType">
    <xs:sequence>
        <xs:element name="ProviderID"
            type="providerIdType"
         />
        <xs:element name="ProviderName"
            type="providerNameType"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                          | Tipo                                                           | Descripción               |
|------------------------------------------------------------------|----------------------------------------------------------------|---------------------------|
| [**ProviderID**](schema-providerid-providertype-element.md)     | [**providerIdType**](schema-provideridtype-simpletype.md)     | IDENTIFICADOR del proveedor.<br/>   |
| [**ProviderName**](schema-providername-providertype-element.md) | [**providerNameType**](schema-providernametype-simpletype.md) | Nombre del proveedor.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                         |



 

 




