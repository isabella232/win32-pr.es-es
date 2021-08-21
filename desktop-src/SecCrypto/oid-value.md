---
description: Establece o recupera el valor del número de puntos del OID del identificador.
ms.assetid: bb960e65-776e-4ae8-a557-62254dc10558
title: Oid. Propiedad Value
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: edaca987dbba57127c922161fbc6c6cd9473732ba1b7d1339618009335c904cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117979737"
---
# <a name="oidvalue-property"></a>Oid. Propiedad Value

\[La **propiedad Value** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use [**la clase Oid en**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) el espacio de nombres [**System.Security.Cryptography.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

La **propiedad Value** establece o recupera el valor del número de puntos del OID del identificador.

## <a name="syntax"></a>Syntax


```VB
OID.Value As String
```



## <a name="property-value"></a>Valor de propiedad

Valor del número de puntos del OID del identificador. Para ver los valores posibles, consulte Wincrypt.h.

## <a name="remarks"></a>Comentarios

Si se **establece** la propiedad Value, la [**propiedad FriendlyName**](oid-friendlyname.md) se establece en el nombre para mostrar correspondiente. Si se establece la propiedad **FriendlyName,** la **propiedad Value** se establece en el valor de puntos correspondiente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Oid**](oid.md)
</dt> </dl>

 

 
