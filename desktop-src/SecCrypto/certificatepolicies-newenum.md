---
description: La \_ propiedad NewEnum de CertificatePolicies recupera una interfaz IEnumVARIANT en un objeto que se puede usar para enumerar la colección.
ms.assetid: 631a11c8-4442-493e-9406-bc63f79db548
title: Propiedad CertificatePolicies._NewEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2d5e90d4b906661119936ca1e893e3b6e17c9bf5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690589"
---
# <a name="certificatepolicies_newenum-property"></a>CertificatePolicies. \_ Propiedad NewEnum

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para que las directivas de certificado recuperen las directivas de certificado.\]

La propiedad **\_ NewEnum** recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).

## <a name="syntax"></a>Sintaxis


```VB
CertificatePolicies._NewEnum As IUnknown
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



 

 
