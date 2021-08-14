---
title: Elemento CredentialsBlob (EapHostUserCredentials)
description: Se usa cuando la configuración del método es un BLOB binario en lugar de en formato de texto XML.
ms.assetid: 9d03374b-74f6-428e-8d3e-f8dccf51884e
keywords:
- Elemento CredentialsBlob EAPHost
topic_type:
- apiref
api_name:
- CredentialsBlob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e56fe90677d0988420a97510da75ea24bf9d50610f9b0b06555a127ef5f731c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118274479"
---
# <a name="credentialsblob-eaphostusercredentials-element"></a>Elemento CredentialsBlob (EapHostUserCredentials)

El **elemento CredentialsBlob (EapHostUserCredentials)** se usa cuando la configuración del método es un BLOB binario en lugar de en formato de texto XML.

``` syntax
<xs:element name="CredentialsBlob"
    type="hexBinary"
 />
```

El **elemento CredentialsBlob** se define mediante el [**elemento EapHostUserCredentials.**](eaphostusercredentialsschema-eaphostusercredentials-element.md)

## <a name="remarks"></a>Comentarios

Los [**elementos Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) y **CredentialsBlob** no se pueden usar simultáneamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**EapHostUserCredentials**](eaphostusercredentialsschema-eaphostusercredentials-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**EapHostUserCredentials**](eaphostusercredentialsschema-eaphostusercredentials-element.md)
</dt> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaphostusercredentials](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





