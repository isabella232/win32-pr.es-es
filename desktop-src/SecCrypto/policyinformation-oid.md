---
description: Recupera el OID de la Directiva. Esta es la propiedad predeterminada.
ms.assetid: c78bbbcb-befd-491c-afbd-80c3ba124d29
title: Propiedad PolicyInformation. OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9acab40130ef6c55bf014058b3e5a6d935ed8a7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690025"
---
# <a name="policyinformationoid-property"></a>Propiedad PolicyInformation. OID

\[La propiedad **OID** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para procesar la información de la Directiva en la extensión de directivas de certificado.\]

La propiedad **OID** recupera el OID de la Directiva. Esta es la propiedad predeterminada.

## <a name="syntax"></a>Sintaxis


```VB
PolicyInformation.OID As OID
```



## <a name="property-value"></a>Valor de propiedad

Identificador de objeto de la Directiva como un objeto [**OID**](oid.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PolicyInformation**](policyinformation.md)
</dt> </dl>

 

 
