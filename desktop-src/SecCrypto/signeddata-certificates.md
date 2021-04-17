---
description: Recupera la colección de certificados asociada al objeto SignedData. Después de recuperarse, se pueden enumerar los objetos de certificado individuales de la colección.
ms.assetid: 94741fee-2462-4a18-bc14-c52e9cac374b
title: Propiedad SignedData. Certificates
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670817"
---
# <a name="signeddatacertificates-property"></a>Propiedad SignedData. Certificates

\[La propiedad **certificados** está disponible para su uso en los sistemas operativos especificados en la sección requisitos. En su lugar, use la [**clase SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propiedad **Certificates** recupera la colección de [**certificados**](certificates.md) asociada al objeto [**SignedData**](signeddata.md) . Después de recuperarse, se pueden enumerar los objetos de [**certificado**](certificate.md) individuales de la colección.

## <a name="syntax"></a>Sintaxis


```VB
SignedData.Certificates As Certificates
```



## <a name="property-value"></a>Valor de propiedad

Colección de [**certificados**](certificates.md) que está asociada al objeto [**SignedData**](signeddata.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
