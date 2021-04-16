---
description: Identifica el APN o la cadena de marcado que se va a utilizar para establecer una conexión de datos.
ms.assetid: e791ffa1-b417-480c-adb8-b1dda7547d89
title: Elemento AccessString (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AccessString
api_type:
- Schema
ms.openlocfilehash: 8cf0d37b8a1870011ae6ae3ea6febf22a98cdeb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686838"
---
# <a name="accessstring-contexttype-element"></a>Elemento AccessString (contextType)

El elemento **AccessString (contextType)** identifica el APN o la cadena de marcado que se utilizará para establecer una conexión de datos.

Este elemento puede tener una longitud máxima de 100 caracteres.

Este elemento es opcional.

``` syntax
<xs:element name="AccessString">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:minLength
                value="1"
             />
            <xs:maxLength
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

El elemento **AccessString** se define mediante el tipo complejo de [**contextType**](schema-contexttype-complextype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**contextType**](schema-contexttype-complextype.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**Contexto (MBNProfile)**](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




