---
description: Establece o recupera el valor del número de puntos del OID del identificador.
ms.assetid: bb960e65-776e-4ae8-a557-62254dc10558
title: OID. Propiedad Value
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
ms.openlocfilehash: d8c3c59cfd3eadfb8aec56c6814a2af6ce9ff900
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173154"
---
# <a name="oidvalue-property"></a>OID. Propiedad Value

\[La **propiedad Value** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use [**la clase Oid en**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) el espacio de nombres [**System.Security.Cryptography.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

La **propiedad Value** establece o recupera el valor del número de puntos del OID del identificador.

## <a name="syntax"></a>Sintaxis


```VB
OID.Value As String
```



## <a name="property-value"></a>Valor de propiedad

Valor del número de puntos del OID del identificador. Para ver los valores posibles, consulte Wincrypt.h.

## <a name="remarks"></a>Observaciones

Si se **establece** la propiedad Value, la [**propiedad FriendlyName**](oid-friendlyname.md) se establece en el nombre para mostrar correspondiente. Si se establece la propiedad **FriendlyName,** la **propiedad Value** se establece en el valor de puntos correspondiente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**OID**](oid.md)
</dt> </dl>

 

 
