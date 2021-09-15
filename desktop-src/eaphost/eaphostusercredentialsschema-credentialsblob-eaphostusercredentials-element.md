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
ms.openlocfilehash: 1fe7514c3aff50a7ecddadb3d8073a37b6c770eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568776"
---
# <a name="credentialsblob-eaphostusercredentials-element"></a>Elemento CredentialsBlob (EapHostUserCredentials)

El **elemento CredentialsBlob (EapHostUserCredentials)** se usa cuando la configuración del método es un BLOB binario en lugar de en formato de texto XML.

``` syntax
<xs:element name="CredentialsBlob"
    type="hexBinary"
 />
```

El **elemento CredentialsBlob** se define mediante el [**elemento EapHostUserCredentials.**](eaphostusercredentialsschema-eaphostusercredentials-element.md)

## <a name="remarks"></a>Observaciones

Los [**elementos Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) y **CredentialsBlob** no se pueden usar simultáneamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

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

[esquema eaphostusercredentials](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





