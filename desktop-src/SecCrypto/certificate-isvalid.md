---
description: Compila una cadena de comprobación de certificados para un certificado y devuelve un objeto CertificateStatus que contiene el estado de validez del certificado.
ms.assetid: 4463e4ac-60a5-4845-93b3-35d2f83bd86e
title: ICertificate2::IsValid (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.IsValid
- ICertificate2.IsValid
- ICertificate.IsValid
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 97e31129497759fa73abb4456ea8d1b8d20748bef76629d6dd857954863f5aec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126985"
---
# <a name="icertificate2isvalid-method"></a>ICertificate2::IsValid (método)

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **método IsValid** crea una cadena de comprobación de certificados para un certificado y devuelve un objeto [**CertificateStatus**](certificatestatus.md) que contiene el estado de validez del certificado.

## <a name="syntax"></a>Sintaxis


```VB
Certificate.IsValid()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Objetos de criptografía](cryptography-objects.md)
</dt> <dt>

[**Certificado**](certificate.md)
</dt> </dl>

 

 
