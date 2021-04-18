---
description: Recupera el objeto de firmante que representa el firmante indizado.
ms.assetid: a95f4e33-ab92-44e1-91ab-2c5335a04f05
title: Propiedad signers. Item
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
ms.openlocfilehash: 9b0b4179c1ea7e2ded5d945f64f03124eb864fdc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691054"
---
# <a name="signersitem-property"></a>Propiedad signers. Item

\[La propiedad **Item** está disponible para su uso en los sistemas operativos especificados en la sección requirements. En su lugar, use una colección de objetos CmsSigner. Para obtener más información, vea la [**clase CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propiedad **Item** recupera el objeto de [**firmante**](signer.md) que representa el firmante indizado. Esta es la propiedad predeterminada.

## <a name="syntax"></a>Sintaxis


```VB
Signers.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Valor de propiedad

Objeto de [**firmante**](signer.md) que representa el firmante indizado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Firmantes**](signers.md)
</dt> </dl>

 

 
