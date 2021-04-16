---
description: Recupera un valor booleano que indica si se ha establecido el bit nonRepudiationEnabled.
ms.assetid: d9bcf0fc-8b2d-408c-b587-71903ef5f5f6
title: Propiedad KeyUsage. IsNonRepudiationEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsNonRepudiationEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 30e0a532cd39f2150591a3eb74ed9bbba83a7080
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670290"
---
# <a name="keyusageisnonrepudiationenabled-property"></a>Propiedad KeyUsage. IsNonRepudiationEnabled

\[La propiedad **IsNonRepudiationEnabled** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**clase X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propiedad **IsNonRepudiationEnabled** recupera un valor booleano que indica si se ha establecido el bit nonRepudiationEnabled.

## <a name="syntax"></a>Sintaxis


```VB
KeyUsage.IsNonRepudiationEnabled As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si es **true**, se establece el bit nonRepudiationEnabled.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
