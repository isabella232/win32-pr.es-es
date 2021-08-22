---
description: Establece o recupera el tipo de algoritmo hash utilizado.
ms.assetid: 3f8e83f2-0e46-494b-ac63-658e663680ea
title: Propiedad HashedData.Algorithm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 16562f3b954c9968899b7af63729a105956c7f809d094bdfa6c508a160a6d51d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006653"
---
# <a name="hasheddataalgorithm-property"></a>Propiedad HashedData.Algorithm

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase HashAlgorithm en**](/previous-versions/windows/) el espacio de nombres [**System.Security.Cryptography.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

La **propiedad Algorithm** establece o recupera el tipo de algoritmo hash utilizado.

## <a name="syntax"></a>Syntax


```VB
HashedData.Algorithm As CAPICOM_HASH_ALGORITHM
```



## <a name="property-value"></a>Valor de propiedad

Valor de la enumeración [**CAPICOM \_ HASH \_ ALGORITHM**](capicom-hash-algorithm.md) que define un algoritmo hash. El valor predeterminado es CAPICOM \_ HASH \_ ALGORITHM \_ SHA1. En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                               | Significado                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_HASH_ALGORITHM_SHA1"></span><span id="capicom_hash_algorithm_sha1"></span><dl> <dt>**ALGORITMO \_ HASH CAPICOM \_ \_ SHA1**</dt> </dl>           | Algoritmo hash SHA1.<br/>                                                                          |
| <span id="CAPICOM_HASH_ALGORITHM_MD2"></span><span id="capicom_hash_algorithm_md2"></span><dl> <dt>**ALGORITMO \_ HASH CAPICOM \_ \_ MD2**</dt> </dl>              | Algoritmo de hash MD2.<br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_MD4"></span><span id="capicom_hash_algorithm_md4"></span><dl> <dt>**ALGORITMO \_ HASH CAPICOM \_ \_ MD4**</dt> </dl>              | Algoritmo de hash MD4.<br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_MD5"></span><span id="capicom_hash_algorithm_md5"></span><dl> <dt>**ALGORITMO \_ HASH CAPICOM \_ \_ MD5**</dt> </dl>              | Algoritmo de hash MD5.<br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_256"></span><span id="capicom_hash_algorithm_sha_256"></span><dl> <dt>**ALGORITMO \_ HASH CAPICOM SHA \_ \_ \_ 256**</dt> </dl> | Algoritmo hash SHA-256.<br/> **CAPICOM 2.0.0.3 y versiones anteriores:** Este valor no se admite.<br/> |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_384"></span><span id="capicom_hash_algorithm_sha_384"></span><dl> <dt>**ALGORITMO \_ HASH CAPICOM SHA \_ \_ \_ 384**</dt> </dl> | Algoritmo hash SHA-384.<br/> **CAPICOM 2.0.0.3 y versiones anteriores:** Este valor no se admite.<br/> |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_512"></span><span id="capicom_hash_algorithm_sha_512"></span><dl> <dt>**ALGORITMO \_ HASH CAPICOM SHA \_ \_ \_ 512**</dt> </dl> | Algoritmo hash SHA-512.<br/> **CAPICOM 2.0.0.3 y versiones anteriores:** Este valor no se admite.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**HashedData**](hasheddata.md)
</dt> </dl>

 

 
