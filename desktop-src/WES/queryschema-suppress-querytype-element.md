---
title: Suppress (QueryType) (elemento)
description: Consulta XPath que identifica los eventos que se van a excluir del conjunto de resultados de la consulta.
ms.assetid: 41304a3c-bde1-49c3-8cb3-e95fc428bd96
keywords:
- Elemento suprimir EventLog
topic_type:
- apiref
api_name:
- Suppress
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a1d7fcec98d32167155ebcafc4f13d2a727d59a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151169"
---
# <a name="suppress-querytype-element"></a>Suppress (QueryType) (elemento)

Consulta XPath que identifica los eventos que se van a excluir del conjunto de resultados de la consulta.

``` syntax
<xs:element name="Suppress">
    <xs:complexType
        mixed="true"
    >
        <xs:attribute name="Path"
            type="anyURI"
         />
    </xs:complexType>
</xs:element>
```

El elemento **Suppress** se define mediante el tipo complejo [**QueryType**](queryschema-querytype-complextype.md) .

## <a name="attributes"></a>Atributos



| Nombre | Tipo   | Descripción                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| Path | anyURI | El nombre del canal o la ruta de acceso al archivo de registro que contiene los eventos.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Elemento primario**
</dt> <dt>

[**Consulta (QueryListType)**](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





