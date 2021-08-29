---
description: Recupera un valor booleano que indica si la extensión KeyUsage está marcada como crítica.
ms.assetid: f7d53570-2b89-40a9-ab56-fcae4e4cb70c
title: KeyUsage.IsCritical, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f1f383281d174b1a954566fb751fc3f3fa9f087648a60ede740f9efd5ec66007
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408885"
---
# <a name="keyusageiscritical-property"></a>KeyUsage.IsCritical, propiedad

\[La **propiedad IsCritical** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use la clase [**X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **propiedad IsCritical** recupera un valor booleano que indica si la extensión KeyUsage está marcada como crítica.

## <a name="syntax"></a>Syntax


```VB
KeyUsage.IsCritical As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si **es true,** la extensión KeyUsage se marca como crítica.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
