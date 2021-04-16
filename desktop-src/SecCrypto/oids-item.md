---
description: Recupera un objeto OID de la colección. Esta es la propiedad predeterminada.
ms.assetid: af0de567-e520-411d-850d-fbdbcb2ace69
title: OID. Item (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dfdf65f013c5e5e1a031c03c19af9d08b8fc72c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690066"
---
# <a name="oidsitem-property"></a>OID. Item (propiedad)

\[La propiedad **Item** está disponible para su uso en los sistemas operativos especificados en la sección requirements. En su lugar, use la [**clase OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propiedad **Item** recupera un objeto [**OID**](oid.md) de la colección. Esta es la propiedad predeterminada.

## <a name="syntax"></a>Sintaxis


```VB
OIDs.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Valor de propiedad

Objeto [**OID**](oid.md) en el índice especificado o el objeto **OID** con el valor de puntos especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**OID**](oids.md)
</dt> </dl>

 

 
