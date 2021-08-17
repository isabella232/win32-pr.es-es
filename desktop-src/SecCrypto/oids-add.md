---
description: Agrega el objeto OID especificado a la colección.
ms.assetid: 0ae087d6-768a-4538-b834-0f936680de05
title: Método OIDs.Add
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ff686ae816fa61d68e0a0c40326581025ced8f4c94fb5cffc633ff452ac4f0ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117979656"
---
# <a name="oidsadd-method"></a>Método OIDs.Add

\[El **método Add** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use [**la clase OidCollection en**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) el espacio de nombres [**System.Security.Cryptography.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

El **método Add** agrega el objeto [**OID**](oid.md) especificado a la colección.

## <a name="syntax"></a>Sintaxis


```VB
OIDs.Add( _
  ByVal OID _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*OID* \[ En\]
</dt> <dd>

Objeto [**OID**](oid.md) que se va a agregar a la colección. El **objeto OID** se agrega en orden ordenado en función de su valor de puntos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
