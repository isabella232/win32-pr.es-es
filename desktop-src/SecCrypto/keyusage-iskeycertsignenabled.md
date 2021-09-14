---
description: Recupera un valor booleano que indica si el bit keyCertSign está establecido.
ms.assetid: c0331293-4a65-40f0-a404-87d8546349c2
title: KeyUsage.IsKeyCertSignEnabled, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsKeyCertSignEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d475565896910f76211e3843526e9a889586efa0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259487"
---
# <a name="keyusageiskeycertsignenabled-property"></a>KeyUsage.IsKeyCertSignEnabled, propiedad

\[La **propiedad IsKeyCertSignEnabled** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use la clase [**X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **propiedad IsKeyCertSignEnabled** recupera un valor booleano que indica si el bit keyCertSign está establecido.

## <a name="syntax"></a>Sintaxis


```VB
KeyUsage.IsKeyCertSignEnabled As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si **es true**, se establece el bit keyCertSign.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
