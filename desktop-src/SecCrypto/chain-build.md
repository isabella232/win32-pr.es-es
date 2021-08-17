---
description: Compila una cadena de comprobación de certificados desde un certificado final hasta el certificado raíz de confianza y devuelve un valor booleano que indica la validez general de la cadena.
ms.assetid: 878f09ba-d79b-4f14-b4f6-ecb54771f56f
title: IChain2::Build (método)
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
ms.openlocfilehash: 5001fe6855a02ad487b16b56d01eb83d28c25c8ef5ba52e6249c9de1bd2fc8a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769754"
---
# <a name="ichain2build-method"></a>IChain2::Build (método)

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **método Build** crea una cadena de comprobación de certificados desde un certificado final hasta el certificado [*raíz*](../secgloss/r-gly.md) de confianza y devuelve un valor booleano que indica la validez general de la cadena.

## <a name="syntax"></a>Sintaxis


```VB
Chain.Build( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Certificado* \[ En\]
</dt> <dd>

Objeto [**Certificate**](certificate.md) que representa el certificado final en el que se va a crear la cadena de comprobación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Valor booleano que indica la validez general de la cadena. La validez general se basa en la directiva de comprobación de validez que se ha puesto en marcha.

## <a name="remarks"></a>Comentarios

La cadena se basa en la [**propiedad CertificateStatus.CheckFlag,**](certificatestatus-checkflag.md) así como en las directivas de aplicación y certificado especificadas por [**un objeto CertificateStatus.**](certificatestatus.md) Se ordena la colección devuelta; El primer certificado de la colección, **Certificates.Item**(1), es el certificado final de la cadena. El último certificado de la colección, **Certificates.Item**(**Certificates.Count**), es el [*certificado raíz*](../secgloss/r-gly.md) de la cadena. **Certificates.Item**(0) representa toda la cadena.

Cada vez que se llama al método **Chain.Build,** se [*restablece*](../secgloss/s-gly.md) el estado del [**objeto Chain.**](chain.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objetos criptografía**](cryptography-objects.md)
</dt> <dt>

[**Cadena**](chain.md)
</dt> </dl>

 

 
