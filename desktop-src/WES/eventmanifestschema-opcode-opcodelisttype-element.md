---
title: OpCode (OpcodeListType) (elemento)
description: Contiene un valor numérico que identifica la actividad o un punto dentro de una actividad que la aplicación estaba realizando cuando generó el evento (por ejemplo, inicialización o cierre).
ms.assetid: 8c5cfbd3-6a74-452c-a12f-41d663426e2c
keywords:
- elemento OpCode EventLog
topic_type:
- apiref
api_name:
- opcode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e9d02b77b4a36bac26d52d7bf8d849eab8731d27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151068"
---
# <a name="opcode-opcodelisttype-element"></a>OpCode (OpcodeListType) (elemento)

Contiene un valor numérico que identifica la actividad o un punto dentro de una actividad que la aplicación estaba realizando cuando generó el evento (por ejemplo, inicialización o cierre).

``` syntax
<xs:element name="opcode"
    type="OpcodeType"
 />
```

El elemento **OpCode** se define mediante el tipo complejo [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Elementos primarios**
</dt> <dt>

[**códigos de la (TaskType)**](eventmanifestschema-opcodes-tasktype-element.md)
</dt> <dt>

[**códigos de la (ProviderType)**](eventmanifestschema-opcodes-providertype-element.md)
</dt> <dt>

[**OpCodes (MetadataType)**](eventmanifestschema-opcodes-metadatatype-element.md)
</dt> </dl>

 

 





