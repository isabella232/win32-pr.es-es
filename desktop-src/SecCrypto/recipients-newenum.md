---
description: La propiedad NewEnum de Recipients recupera una interfaz IEnumVARIANT en un objeto que se puede usar \_ para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).
ms.assetid: affdc695-b78c-48b5-b66d-5f94e1a86ff2
title: Recipients._NewEnum propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a4a1e7db31ceead23509604edddee05ec64380ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476378"
---
# <a name="recipients_newenum-property"></a>Destinatarios. \_ Propiedad NewEnum

\[La **\_ propiedad NewEnum** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use [**la clase CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

La **\_ propiedad NewEnum** recupera una [**interfaz IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede usar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).

## <a name="syntax"></a>Sintaxis


```VB
Recipients._NewEnum As IUnknown
```



## <a name="property-value"></a>Valor de propiedad

Interfaz [**IEnumVARIANT en**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) un objeto que se puede usar para enumerar la colección.

## <a name="remarks"></a>Observaciones

Esta propiedad se usa automáticamente internamente cuando se usa la construcción `For Each In` en Visual Basic Scripting Edition (VBScript).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Recipients**](recipients.md)
</dt> </dl>

 

 
