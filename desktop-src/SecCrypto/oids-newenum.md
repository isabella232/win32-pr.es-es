---
description: La \_ propiedad NewEnum de OID recupera una interfaz IEnumVARIANT en un objeto que se puede utilizar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).
ms.assetid: 7c09fd11-064b-451e-bd6b-e6c13ab228a0
title: Propiedad OIDs._NewEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d20856c17dda18a10b85c01453cbe043144742d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690065"
---
# <a name="oids_newenum-property"></a>OID. \_ Propiedad NewEnum

\[La propiedad **\_ NewEnum** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**clase OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propiedad **\_ NewEnum** recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).

## <a name="syntax"></a>Sintaxis


```VB
OIDs._NewEnum As IUnknown
```



## <a name="property-value"></a>Valor de propiedad

Una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección.

## <a name="remarks"></a>Observaciones

Esta propiedad se utiliza internamente de forma automática cuando se usa la `For Each In` construcción en Visual Basic Scripting Edition (VBScript).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**OID**](oids.md)
</dt> </dl>

 

 
