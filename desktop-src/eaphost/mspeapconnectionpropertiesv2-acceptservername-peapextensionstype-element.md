---
title: Elemento AcceptServerName (PeapExtensionsType)
description: El elemento AcceptServerName (PeapExtensionsType) indica si el nombre del servidor se valida con la cadena de nombre especificada en ServerNames en el esquema mspeapconnectionpropertiesv2.
ms.assetid: 24409775-d00d-439f-bb0b-a9fe5fb736a7
keywords:
- Elemento AcceptServerName EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 64e82defae9c5ae9f7cf60056cfdac8b58373602
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989480"
---
# <a name="acceptservername-peapextensionstype-element"></a>Elemento AcceptServerName (PeapExtensionsType)

El **elemento AcceptServerName (PeapExtensionsType)** indica si el nombre del servidor se valida con la cadena de nombre especificada en el elemento [**ServerNames (ServerValidationParameters).**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)

``` syntax
<xs:element name="AcceptServerName"
    type="xs:boolean"
 />
```

El **elemento AcceptServerName** se define mediante el [**elemento PeapExtensionsType.**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)

## <a name="remarks"></a>Comentarios

El **elemento AcceptServerName** es opcional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[ R2\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Mspeapconnectionpropertiesv2 Schema](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Elementos de esquema mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





