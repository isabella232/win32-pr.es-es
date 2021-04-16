---
description: Establece o recupera el nombre para mostrar del identificador.
ms.assetid: 53f84d0d-c189-4fd2-a383-29fd0d22de08
title: OID. FriendlyName (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID.FriendlyName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1976980d1a22f4246f0ace686941cc4bcec87c92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671496"
---
# <a name="oidfriendlyname-property"></a>OID. FriendlyName (propiedad)

\[La propiedad **FriendlyName** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**clase OID**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propiedad **FriendlyName** establece o recupera el nombre para mostrar del identificador.

## <a name="syntax"></a>Sintaxis


```VB
OID.FriendlyName As String
```



## <a name="property-value"></a>Valor de propiedad

Nombre para mostrar del [**OID**](oid.md).

## <a name="remarks"></a>Observaciones

Si se establece la propiedad **FriendlyName** , la propiedad [**Value**](oid-value.md) se establece en el valor punteado correspondiente. Si se establece la propiedad **Value** , la propiedad **FriendlyName** se establece en el nombre para mostrar correspondiente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**OID**](oid.md)
</dt> </dl>

 

 
