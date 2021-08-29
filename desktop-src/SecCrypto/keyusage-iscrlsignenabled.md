---
description: Recupera un valor booleano que indica si se establece el bit CRLSign.
ms.assetid: 76ca86e3-55f7-4720-9fa5-d465db2a7b5a
title: Propiedad KeyUsage.IsCRLSignEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsCRLSignEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 47efa230eafe21918f33abcf409d8e1bba73a2c0d7ae0a3e9d1096018e33a11e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867695"
---
# <a name="keyusageiscrlsignenabled-property"></a>Propiedad KeyUsage.IsCRLSignEnabled

\[La **propiedad IsCRLSignEnabled** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use la clase [**X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **propiedad IsCRLSignEnabled** recupera un valor booleano que indica si se establece el bit CRLSign.

## <a name="syntax"></a>Syntax


```VB
KeyUsage.IsCRLSignEnabled As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si **es true,** se establece el bit CRLSign.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
