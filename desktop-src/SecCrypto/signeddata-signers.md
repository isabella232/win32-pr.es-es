---
description: Recupera los creadores de la firma de los datos.
ms.assetid: 3e28f08a-c4d8-4dd7-953a-e1500eb5bee0
title: Propiedad SignedData. Signers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Signers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5f4c58c2a69c483fc38412a6aa8377742d52d39a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690058"
---
# <a name="signeddatasigners-property"></a>Propiedad SignedData. Signers

\[La propiedad **signers** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**clase SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propiedad **signers** recupera los creadores de firmas de los datos.

## <a name="syntax"></a>Sintaxis


```VB
SignedData.Signers As Signers
```



## <a name="property-value"></a>Valor de propiedad

Colección de [**firmadores**](signers.md) que representa los creadores de firmas de los datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
