---
description: La propiedad Result recupera un valor que indica si el certificado es válido. Esta es la propiedad predeterminada.
ms.assetid: b1edfbde-9d54-4e9c-ba9b-33e4c354c23f
title: Propiedad CertificateStatus.Result
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.Result
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dd67cd554fce84edc61b1b48e8a539b58a330ec1163b87b17dd8847b31fb15e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993225"
---
# <a name="certificatestatusresult-property"></a>Propiedad CertificateStatus.Result

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la estructura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **propiedad Result** recupera un valor que indica si el certificado es válido. Esta es la propiedad predeterminada.

## <a name="syntax"></a>Syntax


```VB
CertificateStatus.Result As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si **es true,** el certificado es válido. La validez del certificado se comprueba mediante la configuración actual de la [**propiedad CheckFlag**](certificatestatus-checkflag.md) y las distintas configuraciones de directiva.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
