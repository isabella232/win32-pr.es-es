---
description: Recupera la fecha de finalización de la validez del certificado.
ms.assetid: 25e76b25-9a18-439c-acb8-e0af97b6fcd5
title: Propiedad Certificate. ValidToDate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.ValidToDate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 08f6c0748c38ec31085c937eda37a413a3644f13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690395"
---
# <a name="certificatevalidtodate-property"></a>Propiedad Certificate. ValidToDate

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propiedad **ValidToDate** recupera la fecha de finalización de la validez del certificado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Certificate.ValidToDate As Date
```



## <a name="property-value"></a>Valor de propiedad

Fecha que indica la fecha de finalización de la validez del certificado.

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

 

 
