---
description: Establece o recupera los datos que se firmarán. Esta es la propiedad predeterminada.
ms.assetid: 554ca500-403d-4c2a-868e-9e635d0b358e
title: Propiedad SignedData.Content
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b9f4439f7fc7c2a71887fcb78991cf54a814a8682f991545ec33301e2fb9bc95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118899239"
---
# <a name="signeddatacontent-property"></a>Propiedad SignedData.Content

\[La **propiedad Content** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use [**la clase SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

La **propiedad Content** establece o recupera los datos que se firmarán. Esta es la propiedad predeterminada.

## <a name="syntax"></a>Syntax


```VB
SignedData.Content As String
```



## <a name="property-value"></a>Valor de propiedad

Datos que van a firmar.

## <a name="remarks"></a>Comentarios

Esta propiedad se debe inicializar antes de llamar [**al método Sign.**](signeddata-sign.md) Cuando se restablece el valor de esta propiedad, [](../secgloss/s-gly.md) directa o indirectamente, se restablece todo el estado del objeto y se pierde cualquier firma asociada al objeto antes de cambiar la propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
