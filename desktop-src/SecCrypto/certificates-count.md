---
description: Recupera el número de objetos Certificate de la colección.
ms.assetid: 95931721-3b0c-4915-805f-039d1d5510fa
title: Propiedad Certificates.Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a67554530ce8c8dfdc1bfcfba1198cf778397ac2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476490"
---
# <a name="certificatescount-property"></a>Propiedad Certificates.Count

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase X509Certificate2Collection en**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **propiedad Count** recupera el número de objetos [**Certificate**](certificate.md) de la colección.

## <a name="syntax"></a>Sintaxis


```VB
Certificates.Count As Long
```



## <a name="property-value"></a>Valor de propiedad

Número de objetos [**Certificate**](certificate.md) de la colección. Cada **objeto Certificate** representa un único certificado de la colección.

## <a name="remarks"></a>Observaciones

CAPICOM solo admite un solo certificado para el [*almacén de tarjetas inteligentes.*](../secgloss/s-gly.md) Incluso si el almacén de tarjetas inteligentes contiene más de un certificado, esta propiedad contendrá 1. Para obtener más información sobre el almacén de tarjetas inteligentes, vea el miembro **CAPICOM \_ SMART CARD USER \_ \_ \_ STORE** de la [**enumeración CAPICOM \_ STORE \_ LOCATION.**](capicom-store-location.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Certificados**](certificates.md)
</dt> </dl>

 

 
