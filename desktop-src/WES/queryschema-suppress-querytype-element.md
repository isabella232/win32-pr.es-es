---
title: Elemento Suppress (QueryType)
description: Consulta XPath que identifica los eventos que se excluirán del conjunto de resultados de la consulta.
ms.assetid: 41304a3c-bde1-49c3-8cb3-e95fc428bd96
keywords:
- Suprimir elemento EventLog
topic_type:
- apiref
api_name:
- Suppress
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2612a98c282627154a9107f2f9f77a3ddb52c191e00dbcb394c8db4d7c796b79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032015"
---
# <a name="suppress-querytype-element"></a>Elemento Suppress (QueryType)

Consulta XPath que identifica los eventos que se excluirán del conjunto de resultados de la consulta.

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

El tipo complejo [**QueryType**](queryschema-querytype-complextype.md) define el elemento **Suppress.**

## <a name="attributes"></a>Atributos



| Nombre | Tipo   | Descripción                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| Path | anyURI | Nombre del canal o la ruta de acceso al archivo de registro que contiene los eventos.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Elemento primario**
</dt> <dt>

[**Query (QueryListType)**](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





