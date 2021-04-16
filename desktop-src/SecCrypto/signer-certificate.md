---
description: Establece o recupera el objeto de certificado que representa el certificado de un firmante de los datos.
ms.assetid: 92ac209e-59b5-4a75-922d-d61629ca41b1
title: Propiedad Signer. Certificate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Certificate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 96652f85e6058682dedd3370965ea7ff2408b3b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689974"
---
# <a name="signercertificate-property"></a>Propiedad Signer. Certificate

\[La propiedad de **certificado** está disponible para su uso en los sistemas operativos especificados en la sección requisitos. En su lugar, use la [**clase CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propiedad de **certificado** establece o recupera el objeto de [**certificado**](certificate.md) que representa el certificado de un firmante de los datos. Esta es la propiedad predeterminada.

## <a name="syntax"></a>Sintaxis


```VB
Signer.Certificate As Certificate
```



## <a name="property-value"></a>Valor de propiedad

Objeto de [**certificado**](certificate.md) que representa el certificado de un firmante de los datos.

## <a name="remarks"></a>Observaciones

Cuando el valor de esta propiedad se restablece, directa o indirectamente, se restablece el [*Estado*](../secgloss/s-gly.md) completo del objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Firmante**](signer.md)
</dt> </dl>

 

 
