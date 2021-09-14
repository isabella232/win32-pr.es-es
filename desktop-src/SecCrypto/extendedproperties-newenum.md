---
description: La \_ propiedad NewEnum de ExtendedProperties recupera una interfaz IEnumVARIANT en un objeto que se puede usar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).
ms.assetid: 2692f607-3bec-4674-9d8d-3c872d523ace
title: ExtendedProperties._NewEnum propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 62f07fe7a1a193f93fc0d3bf4c04fbfc5d76ecf9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173202"
---
# <a name="extendedproperties_newenum-property"></a>ExtendedProperties. \_ Propiedad NewEnum

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use Platform Invocation Services (PInvoke) para llamar a la función de API [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) de Win32 y obtener las propiedades. Para obtener información sobre PInvoke, vea [Tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). Las subsecciones .NET y CryptoAPI a través de [P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y .NET y CryptoAPI a través de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Subsecciones de la parte 2 de Extensión de criptografía de .NET con [CAPICOM y P/Invoke](/previous-versions/ms867087(v=msdn.10)) también pueden resultar útiles.\]

La **\_ propiedad NewEnum** recupera una [**interfaz IEnumVARIANT en**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) un objeto que se puede usar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).

## <a name="syntax"></a>Sintaxis


```VB
ExtendedProperties._NewEnum As IUnknown
```



## <a name="property-value"></a>Valor de propiedad

Interfaz [**IEnumVARIANT en**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) un objeto que se puede usar para enumerar la colección.

## <a name="remarks"></a>Observaciones

Esta propiedad se usa automáticamente internamente cuando se usa la construcción `For Each In` en Visual Basic Scripting Edition (VBScript).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
