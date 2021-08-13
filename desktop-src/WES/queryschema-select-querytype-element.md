---
title: Elemento Select (QueryType)
description: Consulta XPath que identifica los eventos que se incluirán en el conjunto de resultados de la consulta.
ms.assetid: b6aa747b-3586-460b-b51c-52fb112739c3
keywords:
- Seleccionar elemento EventLog
topic_type:
- apiref
api_name:
- Select
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b38a4f24746425bcdbea845b1c23ea5dadfdbcbefa41ebc5fa502147aba2ec67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587408"
---
# <a name="select-querytype-element"></a>Elemento Select (QueryType)

Consulta XPath que identifica los eventos que se incluirán en el conjunto de resultados de la consulta.

``` syntax
<xs:element name="Select">
    <xs:complexType
        mixed="true"
    >
        <xs:attribute name="Path"
            type="anyURI"
         />
    </xs:complexType>
</xs:element>
```

El tipo complejo **QueryType** define el elemento [**Select.**](queryschema-querytype-complextype.md)

## <a name="attributes"></a>Atributos



| Nombre | Tipo   | Descripción                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| Path | anyURI | Nombre del canal o la ruta de acceso al archivo de registro que contiene los eventos.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| para aplicaciones para UWP\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Elemento primario**
</dt> <dt>

[**Query (QueryListType)**](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





