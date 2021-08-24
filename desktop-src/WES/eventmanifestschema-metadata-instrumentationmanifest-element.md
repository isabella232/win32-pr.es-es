---
title: elemento metadata (instrumentationManifest)
description: Contiene valores globales a los que puede hacer referencia en otros manifiestos.
ms.assetid: 5bf3bb1e-47c9-4d6e-86e3-3316e21b76b3
keywords:
- elemento de metadatos EventLog
topic_type:
- apiref
api_name:
- metadata
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eaa22cc13c611b90ace42a2a71517fe0771d6e9ed03d6d964f11a4e4c93cda43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136328"
---
# <a name="metadata-instrumentationmanifest-element"></a>elemento metadata (instrumentationManifest)

Contiene valores globales a los que puede hacer referencia en otros manifiestos. Para obtener un ejemplo, consulte el Winmeta.xml incluido en la \\ carpeta Include del SDK Windows.

``` syntax
<xs:element name="metadata"
    type="MetadataType"
 />
```

El **elemento de** metadatos se define mediante el elemento [**instrumentationManifest.**](eventmanifestschema-instrumentationmanifest-element.md)

## <a name="remarks"></a>Comentarios

Aunque puede crear un manifiesto que contenga una sección de metadatos, el servicio no lo usará; los únicos metadatos que el servicio reconoce son los metadatos que se encuentran en el Winmeta.xml archivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Elemento primario**
</dt> <dt>

[**instrumentationManifest**](eventmanifestschema-instrumentationmanifest-element.md)
</dt> </dl>

 

 





