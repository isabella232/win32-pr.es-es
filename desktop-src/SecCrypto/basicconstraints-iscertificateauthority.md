---
description: Recupera un valor booleano que indica si el certificado es para una entidad de certificación (CA).
ms.assetid: 3ca43475-fe97-4eb4-875d-dbc15a0b953c
title: Propiedad BasicConstraints. IsCertificateAuthority
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsCertificateAuthority
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5d4878a8cb21f89f3abeeb9e4b530948ef12e9aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671413"
---
# <a name="basicconstraintsiscertificateauthority-property"></a>Propiedad BasicConstraints. IsCertificateAuthority

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]

La propiedad **IsCertificateAuthority** recupera un valor booleano que indica si el certificado es para una [*entidad de certificación*](../secgloss/c-gly.md) (CA).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
BasicConstraints.IsCertificateAuthority As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si es **true**, el certificado solo lo usará una CA.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
