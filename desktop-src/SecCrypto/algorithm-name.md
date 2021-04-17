---
description: Establece o recupera el algoritmo utilizado para la firma, la envoltura y el cifrado de las operaciones. Esta es la propiedad predeterminada.
ms.assetid: e1144a9c-a352-4f73-a91c-ea66f3d61608
title: Propiedad Algorithm.Name
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
ms.openlocfilehash: 35ff147d8db7fb409787fa938a951dfc0a2320e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670394"
---
# <a name="algorithmname-property"></a>Propiedad Algorithm.Name

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase AlgorithmIdentifier**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propiedad **Name** establece o recupera el algoritmo utilizado para la firma, la envoltura y las operaciones de cifrado. Esta es la propiedad predeterminada.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
Algorithm.Name As CAPICOM_ENCRYPTION_ALGORITHM
```



## <a name="property-value"></a>Valor de propiedad

Valor de la enumeración del [**\_ \_ algoritmo de cifrado CAPICOM**](capicom-encryption-algorithm.md) que especifica el algoritmo que se va a utilizar. En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                                       | Significado                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_RC2"></span><span id="capicom_encryption_algorithm_rc2"></span><dl> <dt>**\_Algoritmo de cifrado de CAPICOM \_ \_ RC2**</dt> </dl>    | Use el cifrado RC2.<br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_RC4"></span><span id="capicom_encryption_algorithm_rc4"></span><dl> <dt>**\_Algoritmo de cifrado de CAPICOM \_ \_ RC4**</dt> </dl>    | Usar el cifrado RC4.<br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_DES"></span><span id="capicom_encryption_algorithm_des"></span><dl> <dt>**\_ \_ algoritmo des de cifrado de CAPICOM \_**</dt> </dl>    | Use el cifrado DES.<br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_3DES"></span><span id="capicom_encryption_algorithm_3des"></span><dl> <dt>**\_Algoritmo de cifrado \_ \_ 3DES de CAPICOM**</dt> </dl> | Use el cifrado Triple DES.<br/> |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_AES"></span><span id="capicom_encryption_algorithm_aes"></span><dl> <dt>**\_algoritmo de cifrado de CAPICOM \_ \_ AES**</dt> </dl>    | Use el algoritmo AES.<br/>     |



 

## <a name="remarks"></a>Observaciones

Cuando el valor de esta propiedad se restablece, directa o indirectamente, se restablece el estado completo del objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
