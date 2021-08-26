---
description: Establece o recupera el algoritmo utilizado para firmar, envolver y cifrar operaciones. Esta es la propiedad predeterminada.
ms.assetid: e1144a9c-a352-4f73-a91c-ea66f3d61608
title: Algorithm.Name propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4d9860e9a3f04f2f17ebcda08a4ec2610c5af3cbb5fbb5e7afa98227264992b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119880155"
---
# <a name="algorithmname-property"></a>Algorithm.Name propiedad

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista, Windows XP. En su lugar, use [**la clase AlgorithmIdentifier en**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) el espacio de nombres [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

La **propiedad Name** establece o recupera el algoritmo utilizado para firmar, envolver y cifrar operaciones. Esta es la propiedad predeterminada.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
Algorithm.Name As CAPICOM_ENCRYPTION_ALGORITHM
```



## <a name="property-value"></a>Valor de propiedad

Valor de la enumeración [**CAPICOM \_ ENCRYPTION \_ ALGORITHM**](capicom-encryption-algorithm.md) que especifica qué algoritmo se va a usar. En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                                       | Significado                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_RC2"></span><span id="capicom_encryption_algorithm_rc2"></span><dl> <dt>**ALGORITMO DE CIFRADO \_ CAPICOM \_ \_ RC2**</dt> </dl>    | Use el cifrado RC2.<br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_RC4"></span><span id="capicom_encryption_algorithm_rc4"></span><dl> <dt>**ALGORITMO DE CIFRADO \_ CAPICOM \_ \_ RC4**</dt> </dl>    | Use el cifrado RC4.<br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_DES"></span><span id="capicom_encryption_algorithm_des"></span><dl> <dt>**CAPICOM \_ ENCRYPTION \_ ALGORITHM \_ DES**</dt> </dl>    | Use el cifrado DES.<br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_3DES"></span><span id="capicom_encryption_algorithm_3des"></span><dl> <dt>**ALGORITMO DE CIFRADO CAPICOM \_ \_ \_ 3DES**</dt> </dl> | Use el cifrado de DES triple.<br/> |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_AES"></span><span id="capicom_encryption_algorithm_aes"></span><dl> <dt>**CAPICOM \_ ENCRYPTION \_ ALGORITHM \_ AES**</dt> </dl>    | Use el algoritmo AES.<br/>     |



 

## <a name="remarks"></a>Comentarios

Cuando se restablece el valor de esta propiedad, directa o indirectamente, se restablece todo el estado del objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
