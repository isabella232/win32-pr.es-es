---
description: Agrega el objeto OID especificado a la colección.
ms.assetid: 0ae087d6-768a-4538-b834-0f936680de05
title: OID. Add (método)
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
ms.openlocfilehash: d2fa007798a0657991ec8e37a7dddc9fb4c95b2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690561"
---
# <a name="oidsadd-method"></a>OID. Add (método)

\[El método **Add** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**clase OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

El método **Add** agrega el objeto [**OID**](oid.md) especificado a la colección.

## <a name="syntax"></a>Sintaxis


```VB
OIDs.Add( _
  ByVal OID _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*OID* \[ de\]
</dt> <dd>

Objeto [**OID**](oid.md) que se va a agregar a la colección. El objeto **OID** se agrega en el criterio de ordenación según su valor de puntos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
