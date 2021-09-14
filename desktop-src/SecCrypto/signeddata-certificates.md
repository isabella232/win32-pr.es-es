---
description: Recupera la colección Certificates asociada al objeto SignedData. Después de recuperarse, se pueden enumerar los objetos Certificate individuales de la colección.
ms.assetid: 94741fee-2462-4a18-bc14-c52e9cac374b
title: Propiedad SignedData.Certificates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 55c0fe432794289fabe67b37deeedfac43f7a7d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160720"
---
# <a name="signeddatacertificates-property"></a>Propiedad SignedData.Certificates

\[La **propiedad Certificados** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use [**la clase SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

La **propiedad Certificates** recupera la [**colección Certificates**](certificates.md) asociada al [**objeto SignedData.**](signeddata.md) Después de recuperarse, se pueden [**enumerar los objetos Certificate**](certificate.md) individuales de la colección.

## <a name="syntax"></a>Sintaxis


```VB
SignedData.Certificates As Certificates
```



## <a name="property-value"></a>Valor de propiedad

Colección [**Certificates**](certificates.md) asociada al [**objeto SignedData.**](signeddata.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
