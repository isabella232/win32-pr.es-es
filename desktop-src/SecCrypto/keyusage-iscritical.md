---
description: Recupera un valor booleano que indica si la extensión KeyUsage está marcada como crítica.
ms.assetid: f7d53570-2b89-40a9-ab56-fcae4e4cb70c
title: Propiedad KeyUsage. IsCritical
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
ms.openlocfilehash: b1829da9c9ddbcf5261f4cc595b72b8596193078
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689922"
---
# <a name="keyusageiscritical-property"></a>Propiedad KeyUsage. IsCritical

\[La propiedad **IsCritical** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**clase X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propiedad **IsCritical** recupera un valor booleano que indica si la extensión KeyUsage está marcada como crítica.

## <a name="syntax"></a>Sintaxis


```VB
KeyUsage.IsCritical As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si es **true**, la extensión KeyUsage se marca como crítica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
