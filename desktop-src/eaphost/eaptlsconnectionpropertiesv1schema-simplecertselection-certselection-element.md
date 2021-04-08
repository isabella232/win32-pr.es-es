---
title: Elemento SimpleCertSelection (CertSelection)
description: Obtenga información sobre el elemento SimpleCertSelection (CertSelection). Este elemento determina el modo en que el usuario selecciona un certificado.
ms.assetid: 28454877-fd07-4b47-9544-f2b4e91c6651
keywords:
- Elemento SimpleCertSelection EAPHost
topic_type:
- apiref
api_name:
- SimpleCertSelection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 30af9872f7583232e91b037c5b8961e18c7ce863
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078381"
---
# <a name="simplecertselection-certselection-element"></a>Elemento SimpleCertSelection (CertSelection)

El elemento **SimpleCertSelection (CertSelection)** determina el modo en que el usuario selecciona un certificado.

``` syntax
<xs:element name="SimpleCertSelection"
    type="boolean"
 />
```

El elemento **SimpleCertSelection** se define mediante el tipo complejo de [**CertSelection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) .

## <a name="remarks"></a>Observaciones

**SimpleCertSelection** es true de forma predeterminada. Si **SimpleCertSelection** es true, EAP-TLS realiza una búsqueda de certificados simple sin ninguna lista desplegable para la selección de certificados. Si **SimpleCertSelection** es false, EAP-TLS muestra al usuario el certificado adecuado que se va a seleccionar.

## <a name="requirements"></a>Requisitos



| Role | Versión mínima del SO admitida |
|------|----------------------|
| Remoto<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**CertSelection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**CertificateStore (CredentialsSourceParameters)**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementos de esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





