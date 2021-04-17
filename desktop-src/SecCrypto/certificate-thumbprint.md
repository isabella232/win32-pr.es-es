---
description: Recupera una cadena hexadecimal que contiene el hash SHA-1 del certificado.
ms.assetid: 6fd6f3ba-f7a9-43a3-a8da-8fd826649a92
title: Propiedad Certificate. Thumbprint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Thumbprint
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c576c46ecf669d215c5bd20a80a0e5a65e3d4706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690034"
---
# <a name="certificatethumbprint-property"></a>Propiedad Certificate. Thumbprint

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propiedad **huella digital** recupera una cadena hexadecimal que contiene el hash [*SHA-1*](../secgloss/s-gly.md) del certificado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Certificate.Thumbprint As String
```



## <a name="property-value"></a>Valor de propiedad

Cadena hexadecimal que contiene el hash SHA-1 del certificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Certificado**](certificate.md)
</dt> </dl>

 

 
