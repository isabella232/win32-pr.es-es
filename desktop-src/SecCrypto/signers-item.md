---
description: Recupera el objeto Signer que representa el firmante indizado.
ms.assetid: a95f4e33-ab92-44e1-91ab-2c5335a04f05
title: Signers.Item, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 33630586282b745da94a442c13a0e85574c5f2e06fc04ab909e4ebf59fc2707b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898412"
---
# <a name="signersitem-property"></a>Signers.Item, propiedad

\[La **propiedad Item** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use una colección de objetos CmsSigner. Para obtener más información, vea [**cmsSigner (clase)**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

La **propiedad Item** recupera el objeto [**Signer**](signer.md) que representa el firmante indizado. Esta es la propiedad predeterminada.

## <a name="syntax"></a>Syntax


```VB
Signers.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Valor de propiedad

Objeto [**Signer**](signer.md) que representa el firmante indexado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Firmantes**](signers.md)
</dt> </dl>

 

 
