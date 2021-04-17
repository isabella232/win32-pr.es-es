---
description: Recupera una colección de los calificadores de la Directiva.
ms.assetid: aa5e2225-0a39-40bc-868c-d96f5953edaa
title: PolicyInformation. Qualifiers (propiedad) (iAds. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation.Qualifiers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 89f24e21acd24cbcaa021f7c668fc8c208102c0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690024"
---
# <a name="policyinformationqualifiers-property"></a>PolicyInformation. Qualifiers (propiedad)

\[La propiedad **calificadores** está disponible para su uso en los sistemas operativos especificados en la sección requisitos. En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para procesar la información de la Directiva en la extensión de directivas de certificado.\]

La propiedad **calificadores** recupera una colección de los calificadores de la Directiva.

## <a name="syntax"></a>Sintaxis


```VB
PolicyInformation.Qualifiers As Qualifiers
```



## <a name="property-value"></a>Valor de propiedad

Calificador del informe de prácticas de certificación (CPS) de la Directiva o calificadores de aviso de usuario, como un objeto de [**calificadores**](qualifiers.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Encabezado<br/>          | <dl> <dt>IAds. h</dt> </dl>      |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PolicyInformation**](policyinformation.md)
</dt> </dl>

 

 
