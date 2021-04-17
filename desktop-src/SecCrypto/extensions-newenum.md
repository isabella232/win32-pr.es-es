---
description: La \_ propiedad NewEnum de Extensions recupera una interfaz IEnumVARIANT en un objeto que se puede utilizar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).
ms.assetid: 0e461683-bb48-4961-91ef-36af1c3f863e
title: Propiedad Extensions._NewEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extensions._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5b605241e8173b8a41779fa00b661a9e2f383ac7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670675"
---
# <a name="extensions_newenum-property"></a>Extensiones. \_ Propiedad NewEnum

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propiedad **\_ NewEnum** recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).

## <a name="syntax"></a>Sintaxis


```VB
Extensions._NewEnum As IUnknown
```



## <a name="property-value"></a>Valor de propiedad

Una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección.

## <a name="remarks"></a>Observaciones

Esta propiedad se utiliza internamente de forma automática cuando se usa la `For Each In` construcción en Visual Basic Scripting Edition (VBScript).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Extensiones**](extensions.md)
</dt> </dl>

 

 
