---
description: Establece o recupera la colección de certificados que se pueden usar para compilar la cadena de certificados.
ms.assetid: cdf378f9-0d71-4dd9-93cc-85f09a51c5fc
title: Propiedad CertificateStatus.Certificates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b049338bd741281c5b7f012fe4ae7ae443cc2c4b6f9dd7f29591e7616fb8b5dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770392"
---
# <a name="certificatestatuscertificates-property"></a>Propiedad CertificateStatus.Certificates

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la estructura [**X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **propiedad Certificates** establece o recupera la colección de certificados que se pueden usar para compilar la cadena de certificados.

## <a name="syntax"></a>Syntax


```VB
CertificateStatus.Certificates As Certificates
```



## <a name="property-value"></a>Valor de propiedad

Objeto [**Certificates**](certificates.md) que representa la colección de certificados que se pueden usar para compilar la cadena de certificados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.1 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
