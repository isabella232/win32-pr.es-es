---
description: Recupera el número de objetos de certificado de la colección.
ms.assetid: 95931721-3b0c-4915-805f-039d1d5510fa
title: Certificates. Count (propiedad)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690447"
---
# <a name="certificatescount-property"></a>Certificates. Count (propiedad)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propiedad **Count** recupera el número de objetos de [**certificado**](certificate.md) de la colección.

## <a name="syntax"></a>Sintaxis


```VB
Certificates.Count As Long
```



## <a name="property-value"></a>Valor de propiedad

Número de objetos de [**certificado**](certificate.md) de la colección. Cada objeto de **certificado** representa un único certificado de la colección.

## <a name="remarks"></a>Observaciones

CAPICOM solo admite un único certificado para el almacén de [*tarjetas inteligentes*](../secgloss/s-gly.md) . Aunque el almacén de tarjetas inteligentes contenga más de un certificado, esta propiedad contendrá 1. Para obtener más información acerca del almacén de tarjetas inteligentes, consulte el miembro del **\_ almacén de \_ \_ usuarios \_ de tarjetas inteligentes CAPICOM** de la enumeración de la [**Ubicación del \_ almacén \_ de CAPICOM**](capicom-store-location.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Certificados**](certificates.md)
</dt> </dl>

 

 
