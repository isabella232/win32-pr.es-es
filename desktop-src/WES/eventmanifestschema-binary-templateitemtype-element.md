---
title: elemento binary (TemplateItemType)
description: Contiene los datos binarios proporcionados por la API de registro de eventos.
ms.assetid: 3ad9c119-9395-49d3-b920-9a071bcc6a04
keywords:
- elemento binario EventLog
topic_type:
- apiref
api_name:
- binary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c3e281da662b4cdd0ecacc81a88f1a5728f90da
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126885481"
---
# <a name="binary-templateitemtype-element"></a>elemento binary (TemplateItemType)

Contiene los datos binarios proporcionados por la API [de registro de](/windows/desktop/EventLog/event-logging) eventos.

``` syntax
<xs:element name="binary">
    <xs:complexType>
        <xs:attribute name="name"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

El **tipo** complejo [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) define el elemento binario.

## <a name="attributes"></a>Atributos



| Nombre | Tipo   | Descripción                                          |
|------|--------|------------------------------------------------------|
| name | string | Nombre asociado a los datos binarios.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Elemento primario**
</dt> <dt>

[**template (TemplateListType)**](eventmanifestschema-template-templatelisttype-element.md)
</dt> </dl>

 

