---
description: Recupera la especificación de clave.
ms.assetid: 93c909cb-b1d1-4c2b-a66c-9d3f6dd9b340
title: Propiedad PrivateKey.KeySpec
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.KeySpec
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f9d0ba55ca48d5257a038845f84374544b7615b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170909"
---
# <a name="privatekeykeyspec-property"></a>Propiedad PrivateKey.KeySpec

\[La **propiedad KeySpec** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use la propiedad [**X509Certificate2.PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **propiedad KeySpec** recupera la especificación de clave.

## <a name="syntax"></a>Sintaxis


```VB
PrivateKey.KeySpec As CAPICOM_KEY_SPEC
```



## <a name="property-value"></a>Valor de propiedad

Valor de la [**enumeración CAPICOM \_ KEY \_ SPEC**](capicom-key-spec.md) que indica la especificación de clave. En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                        | Significado                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="CAPICOM_KEY_SPEC_KEYEXCHANGE"></span><span id="capicom_key_spec_keyexchange"></span><dl> <dt>**CAPICOM \_ KEY \_ SPEC \_ KEYEXCHANGE**</dt> </dl> | La clave se puede usar para el cifrado y la firma.<br/> |
| <span id="CAPICOM_KEY_SPEC_SIGNATURE"></span><span id="capicom_key_spec_signature"></span><dl> <dt>**CAPICOM \_ KEY \_ SPEC \_ SIGNATURE**</dt> </dl>       | La clave solo se puede usar para firmar.<br/>           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> </dl>

 

 
