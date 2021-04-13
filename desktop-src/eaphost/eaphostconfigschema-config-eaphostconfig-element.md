---
title: Elemento config (EapHostConfig)
description: Se usa cuando la configuración del método está en formato de texto XML en lugar de un BLOB binario.
ms.assetid: f47bec23-745f-47db-84db-2556beb6a9e9
keywords:
- Elemento de configuración EAPHost
topic_type:
- apiref
api_name:
- Config
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a81c90063a57a9d55d8ab6d9c18486315c187f0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491062"
---
# <a name="config-eaphostconfig-element"></a>Elemento config (EapHostConfig)

El elemento de **configuración (EapHostConfig)** se usa cuando la configuración del método está en formato de texto XML en lugar de un BLOB binario.

``` syntax
<xs:element name="Config"
    type="BaseEapMethodConfig"
 />
```

El elemento de **configuración** se define mediante el elemento [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md) .

## <a name="remarks"></a>Observaciones

Los elementos **config** y [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) no se pueden usar simultáneamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaphostconfig](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





