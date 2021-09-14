---
description: La propiedad NewEnum de Qualifiers recupera una interfaz IEnumVARIANT en un objeto que se puede usar \_ para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).
ms.assetid: e51f8ca1-ef1f-475b-8368-e8296fae0f04
title: Qualifiers._NewEnum propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 01a4d62604dabacd2d78d5d2f6cbee0db7189196
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173129"
---
# <a name="qualifiers_newenum-property"></a>Calificadores. \_ Propiedad NewEnum

\[La **\_ propiedad NewEnum** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use la clase [**X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para procesar calificadores que forman parte de la información de directiva en la extensión Directivas de certificado.\]

La **\_ propiedad NewEnum** recupera una [**interfaz IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede usar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).

## <a name="syntax"></a>Sintaxis


```VB
Qualifiers._NewEnum As IUnknown
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

[**Calificadores**](qualifiers.md)
</dt> </dl>

 

 
