---
description: Recupera un valor booleano que indica si se establece el bit keyAgreement.
ms.assetid: 3dd1f6c7-893d-453e-92dc-ffeffd879519
title: Propiedad KeyUsage.IsKeyAgreementEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsKeyAgreementEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 74369996d9e525746e315d1dd2934ef854ffd110
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473463"
---
# <a name="keyusageiskeyagreementenabled-property"></a>Propiedad KeyUsage.IsKeyAgreementEnabled

\[La **propiedad IsKeyAgreementEnabled** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use la clase [**X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **propiedad IsKeyAgreementEnabled** recupera un valor booleano que indica si se establece el bit keyAgreement.

## <a name="syntax"></a>Sintaxis


```VB
KeyUsage.IsKeyAgreementEnabled As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si **es true,** se establece el bit keyAgreement.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
