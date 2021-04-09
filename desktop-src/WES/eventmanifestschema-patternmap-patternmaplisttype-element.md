---
title: Elemento patternMap (PatternMapListType)
description: Define una asignación entre dos expresiones regulares. Una expresión se utiliza para buscar una cadena coincidente en la cadena de mensaje y la otra se usa para modificar la cadena antes de que el servicio la vuelva a colocar en la cadena de mensaje.
ms.assetid: 5cf28d38-4cc3-4a7b-a64b-3ad1cb42ebef
keywords:
- elemento patternMap EventLog
topic_type:
- apiref
api_name:
- patternMap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3ae29d60e39515a7c4b4db334f947abc44df5ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078800"
---
# <a name="patternmap-patternmaplisttype-element"></a>Elemento patternMap (PatternMapListType)

Define una asignación entre dos expresiones regulares. Una expresión se utiliza para buscar una cadena coincidente en la cadena de mensaje y la otra se usa para modificar la cadena antes de que el servicio la vuelva a colocar en la cadena de mensaje.

``` syntax
<xs:element name="patternMap"
    type="PatternMapType"
 />
```

El elemento **patternMap** se define mediante el tipo complejo de [**PatternMapListType**](eventmanifestschema-patternmaplisttype-complextype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Elemento primario**
</dt> <dt>

[**patternMaps (NamedQueryType)**](eventmanifestschema-patternmaps-namedquerytype-element.md)
</dt> </dl>

 

 





