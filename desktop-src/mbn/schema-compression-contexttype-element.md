---
description: Especifica si se usará la compresión en el vínculo de datos para el encabezado y la transferencia de datos.
ms.assetid: 2aee93e4-d124-43cb-b974-19f00eb4d6a6
title: Elemento Compression (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Compression
api_type:
- Schema
ms.openlocfilehash: 0da6665f69c2791669f75b91e847081dbcc351e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168150"
---
# <a name="compression-contexttype-element"></a>Elemento Compression (contextType)

El **elemento Compression (contextType)** especifica si se usará la compresión en el vínculo de datos para el encabezado y la transferencia de datos.

Este elemento puede ser uno de los siguientes valores.

| Value     | Significado                       |
|-----------|-------------------------------|
| "ENABLE"  | Se usará la compresión.     |
| "DISABLE" | No se usará la compresión. |



 

Este elemento es opcional. Si no se especifica este elemento, el sistema de banda ancha móvil no usará la compresión.

``` syntax
<xs:element name="Compression">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="DISABLE"
             />
            <xs:enumeration
                value="ENABLE"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

El **elemento Compression** se define mediante el tipo complejo [**contextType.**](schema-contexttype-complextype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio aplicaciones para \| UWP\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**contextType**](schema-contexttype-complextype.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**Context (MBNProfile)**](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




