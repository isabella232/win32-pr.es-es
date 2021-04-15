---
description: Establece o recupera la hora a la que se ha comprobado el certificado.
ms.assetid: 1bd17df3-2fa1-4b99-ab00-659b4ad5fcd9
title: Propiedad CertificateStatus. VerificationTime
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.VerificationTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 178402861c9830efbea78a31081ae7e8b31800b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689944"
---
# <a name="certificatestatusverificationtime-property"></a>Propiedad CertificateStatus. VerificationTime

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**estructura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propiedad **VerificationTime** establece o recupera la hora a la que se ha comprobado el certificado.

## <a name="syntax"></a>Sintaxis


```VB
CertificateStatus.VerificationTime As Date
```



## <a name="property-value"></a>Valor de propiedad

La hora a la que se comprobó el certificado.

## <a name="remarks"></a>Observaciones

Si no se establece esta propiedad, se utiliza la hora actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
