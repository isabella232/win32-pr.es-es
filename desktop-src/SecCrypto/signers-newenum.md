---
description: La \_ propiedad NewEnum de Signers recupera una interfaz IEnumVARIANT en un objeto que se puede usar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).
ms.assetid: 99d7ddd3-a552-4125-b220-d1b28f20d1ed
title: Signers._NewEnum propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 866b85d8bfd5eee89a8c8766acb10baa024aa35e4f81b7d7289a6430d345fa6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898402"
---
# <a name="signers_newenum-property"></a>Firmantes. \_ Propiedad NewEnum

\[La **\_ propiedad NewEnum** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use una colección de objetos CmsSigner. Para obtener más información, vea [**cmsSigner (clase)**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

La **\_ propiedad NewEnum** recupera una [**interfaz IEnumVARIANT en**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) un objeto que se puede usar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).

## <a name="syntax"></a>Syntax


```VB
Signers._NewEnum As IUnknown
```



## <a name="property-value"></a>Valor de propiedad

Interfaz [**IEnumVARIANT en**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) un objeto que se puede usar para enumerar la colección.

## <a name="remarks"></a>Comentarios

Esta propiedad se usa automáticamente internamente cuando se usa la construcción `For Each In` en Visual Basic Scripting Edition (VBScript).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Firmantes**](signers.md)
</dt> </dl>

 

 
