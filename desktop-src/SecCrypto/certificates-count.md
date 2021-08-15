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
ms.openlocfilehash: 703b929ee4b9cbe69a0f2ff37ad7e1d0c2c0005c0aa461fc38a14baa8a8ab443
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770554"
---
# <a name="certificatescount-property"></a>Propiedad Certificates.Count

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **propiedad Count** recupera el número de objetos [**Certificate**](certificate.md) de la colección.

## <a name="syntax"></a>Syntax


```VB
Certificates.Count As Long
```



## <a name="property-value"></a>Valor de propiedad

Número de objetos [**Certificate**](certificate.md) de la colección. Cada **objeto** Certificate representa un único certificado de la colección.

## <a name="remarks"></a>Comentarios

CAPICOM solo admite un único certificado para el [*almacén de tarjetas inteligentes.*](../secgloss/s-gly.md) Incluso si el almacén de tarjetas inteligentes contiene más de un certificado, esta propiedad contendrá 1. Para obtener más información sobre la tienda de tarjetas inteligentes, vea el miembro **CAPICOM \_ SMART CARD USER \_ \_ \_ STORE** de la [**enumeración CAPICOM \_ STORE \_ LOCATION.**](capicom-store-location.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Certificados**](certificates.md)
</dt> </dl>

 

 
