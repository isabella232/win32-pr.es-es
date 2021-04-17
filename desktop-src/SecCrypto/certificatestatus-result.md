---
description: La propiedad resultado recupera un valor que indica si el certificado es válido. Esta es la propiedad predeterminada.
ms.assetid: b1edfbde-9d54-4e9c-ba9b-33e4c354c23f
title: CertificateStatus. Result (propiedad)
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
ms.openlocfilehash: df13e9a9fb0454d30ce855b3d272fa521e96e0f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670333"
---
# <a name="certificatestatusresult-property"></a>CertificateStatus. Result (propiedad)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**estructura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propiedad **resultado** recupera un valor que indica si el certificado es válido. Esta es la propiedad predeterminada.

## <a name="syntax"></a>Sintaxis


```VB
CertificateStatus.Result As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si es **true**, el certificado es válido. La validez del certificado se comprueba con la configuración actual de la propiedad [**CheckFlag**](certificatestatus-checkflag.md) y de las distintas configuraciones de directiva.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
