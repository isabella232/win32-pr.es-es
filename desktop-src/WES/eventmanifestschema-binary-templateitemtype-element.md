---
title: Elemento binario (TemplateItemType)
description: Contiene los datos binarios proporcionados por la API del registro de eventos.
ms.assetid: 3ad9c119-9395-49d3-b920-9a071bcc6a04
keywords:
- EventLog del elemento binario
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105696002"
---
# <a name="binary-templateitemtype-element"></a>Elemento binario (TemplateItemType)

Contiene los datos binarios proporcionados por la API del [registro de eventos](/windows/desktop/EventLog/event-logging) .

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

El elemento **binario** se define mediante el tipo complejo [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) .

## <a name="attributes"></a>Atributos



| Nombre | Tipo   | Descripción                                          |
|------|--------|------------------------------------------------------|
| name | string | Nombre asociado a los datos binarios.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Elemento primario**
</dt> <dt>

[**plantilla (TemplateListType)**](eventmanifestschema-template-templatelisttype-element.md)
</dt> </dl>

 

