---
description: Recupera un valor booleano que indica si se establece el bit dataEncipherment.
ms.assetid: 9b29a76f-1494-4db3-a5d7-69fe631ca1dd
title: Propiedad KeyUsage.IsDataEnciphermentEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsDataEnciphermentEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1ca5e71de36503406e5cc45f136fc7e86eb3ec2cc0324d4a1a75d81cf1bc6fa4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100785"
---
# <a name="keyusageisdataenciphermentenabled-property"></a>Propiedad KeyUsage.IsDataEnciphermentEnabled

\[La **propiedad IsDataEnciphermentEnabled** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use la clase [**X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **propiedad IsDataEnciphermentEnabled** recupera un valor booleano que indica si se establece el bit dataEncipherment.

## <a name="syntax"></a>Syntax


```VB
KeyUsage.IsDataEnciphermentEnabled As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si **es true,** se establece el bit dataEncipherment.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
