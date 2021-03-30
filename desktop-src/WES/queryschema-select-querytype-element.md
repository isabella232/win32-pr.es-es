---
title: Select (QueryType) (elemento)
description: Consulta XPath que identifica los eventos que se van a incluir en el conjunto de resultados de la consulta.
ms.assetid: b6aa747b-3586-460b-b51c-52fb112739c3
keywords:
- Elemento Select EventLog
topic_type:
- apiref
api_name:
- Select
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b1735f5de49853357eed1ce00b8d181edf2279ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422557"
---
# <a name="select-querytype-element"></a>Select (QueryType) (elemento)

Consulta XPath que identifica los eventos que se van a incluir en el conjunto de resultados de la consulta.

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

El elemento **Select** se define mediante el tipo complejo de [**QueryType**](queryschema-querytype-complextype.md) .

## <a name="attributes"></a>Atributos



| Nombre | Tipo   | Descripción                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| Path | anyURI | El nombre del canal o la ruta de acceso al archivo de registro que contiene los eventos.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]<br/>       |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Elemento primario**
</dt> <dt>

[**Consulta (QueryListType)**](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





