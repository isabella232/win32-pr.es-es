---
title: Tipo complejo de CertSelection
description: Obtenga información sobre el tipo complejo de CertSelection. Este tipo determina el modo en que el usuario selecciona un certificado.
ms.assetid: f5a37258-8ab0-4736-9721-6c2800769c74
keywords:
- Tipo complejo CertSelection EAPHost
topic_type:
- apiref
api_name:
- CertSelection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ba22df8dca61696f214e495542319168183dd2bf
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104359420"
---
# <a name="certselection-complex-type"></a>Tipo complejo de CertSelection

El tipo complejo de **CertSelection** determina el modo en que el usuario selecciona un certificado.

``` syntax
<xs:complexType name="CertSelection">
    <xs:sequence>
        <xs:element name="SimpleCertSelection"
            type="boolean"
            minOccurs="0"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                                     | Tipo    | Descripción                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SimpleCertSelection**](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) | boolean | Es TRUE de forma predeterminada. Si [**SimpleCertSelection**](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) es true, EAP-TLS realiza una búsqueda de certificados simple sin ninguna lista desplegable para la selección de certificados. Si **SimpleCertSelection** es false, EAP-TLS muestra al usuario el certificado adecuado que se va a seleccionar.<br/> |



## <a name="requirements"></a>Requisitos



| Role | Versión mínima admitida del sistema operativo |
|------|------------------------------|
| Remoto<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Tipos complejos de esquema de eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





