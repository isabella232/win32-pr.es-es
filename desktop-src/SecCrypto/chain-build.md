---
description: Crea una cadena de comprobación de certificados desde un certificado final al certificado raíz de confianza y devuelve un valor booleano que indica la validez global de la cadena.
ms.assetid: 878f09ba-d79b-4f14-b4f6-ecb54771f56f
title: 'IChain2:: Build (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.Build
- IChain2.Build
- IChain.Build
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 66ad51d94fdbd361a34e25b4b76289139abb87f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670298"
---
# <a name="ichain2build-method"></a>IChain2:: Build (método)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

El método **Build** crea una cadena de comprobación de certificados desde un certificado final al [*certificado raíz*](../secgloss/r-gly.md) de confianza y devuelve un valor booleano que indica la validez global de la cadena.

## <a name="syntax"></a>Sintaxis


```VB
Chain.Build( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Certificado* \[ de de\]
</dt> <dd>

Objeto de [**certificado**](certificate.md) que representa el certificado final en el que se va a compilar la cadena de comprobación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Valor booleano que indica la validez global de la cadena. La validez general se basa en la Directiva de comprobación de validez vigente.

## <a name="remarks"></a>Observaciones

La cadena se genera mediante la propiedad [**CertificateStatus. CheckFlag**](certificatestatus-checkflag.md) , así como las directivas de aplicación y de certificado especificadas por un objeto [**CertificateStatus**](certificatestatus.md) . La colección devuelta está ordenada; el primer certificado de la colección, Certificates **. Item**(1), es el certificado final de la cadena. El último certificado de la colección, Certificates **. Item**(**Certificates. Count**), es el [*certificado raíz*](../secgloss/r-gly.md) de la cadena. **Certificates. Item**(0) representa la cadena completa.

Cada vez que se llama al método **Chain. Build** , se restablece el [*Estado*](../secgloss/s-gly.md) del objeto de [**cadena**](chain.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> <dt>

[**IAM**](chain.md)
</dt> </dl>

 

 
