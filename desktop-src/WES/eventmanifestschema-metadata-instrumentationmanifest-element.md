---
title: Elemento metadata (instrumentationManifest)
description: Contiene valores globales a los que se puede hacer referencia en otros manifiestos.
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
ms.openlocfilehash: c14dc8772dee66fcce9ff07e9918c11b463aa414
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149919"
---
# <a name="metadata-instrumentationmanifest-element"></a>Elemento metadata (instrumentationManifest)

Contiene valores globales a los que se puede hacer referencia en otros manifiestos. Para obtener un ejemplo, vea el archivo Winmeta.xml incluido en la \\ carpeta include del Windows SDK.

``` syntax
<xs:element name="metadata"
    type="MetadataType"
 />
```

El elemento de **metadatos** se define mediante el elemento [**instrumentationManifest**](eventmanifestschema-instrumentationmanifest-element.md) .

## <a name="remarks"></a>Observaciones

Aunque puede crear un manifiesto que contiene una sección de metadatos, el servicio no lo usará; los únicos metadatos que reconoce el servicio son los metadatos que se encuentran en el archivo de Winmeta.xml.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Elemento primario**
</dt> <dt>

[**instrumentationManifest**](eventmanifestschema-instrumentationmanifest-element.md)
</dt> </dl>

 

 





