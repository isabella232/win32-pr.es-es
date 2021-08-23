---
description: Recupera un valor booleano que indica si se establece el bit keyCertSign.
ms.assetid: c0331293-4a65-40f0-a404-87d8546349c2
title: Propiedad KeyUsage.IsKeyCertSignEnabled
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
ms.openlocfilehash: 61c5ca1e9ae36159293e1e9afe1f79b5ff30cbd659b01a400797ae35aac8873c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515885"
---
# <a name="keyusageiskeycertsignenabled-property"></a>Propiedad KeyUsage.IsKeyCertSignEnabled

\[La **propiedad IsKeyCertSignEnabled** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use la clase [**X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **propiedad IsKeyCertSignEnabled** recupera un valor booleano que indica si se establece el bit keyCertSign.

## <a name="syntax"></a>Syntax


```VB
KeyUsage.IsKeyCertSignEnabled As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si **es true,** se establece el bit keyCertSign.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
