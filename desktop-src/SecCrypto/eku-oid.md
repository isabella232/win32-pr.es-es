---
description: Establece o recupera una cadena que contiene un valor de cadena OID de EKU tal y como se define en Wincrypt. h.
ms.assetid: 2fdaeddc-5ed6-46a6-a4f7-827a605e890a
title: 'IEKU:: OID (propiedad)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKU.OID
- IEKU.get_OID
- IEKU.put_OID
- EKU.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 77a519051d2bd1cb3c948bf0e2271cced7d80a20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671237"
---
# <a name="iekuoid-property"></a>IEKU:: OID (propiedad)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propiedad **OID** establece o recupera una cadena que contiene un valor de cadena OID de EKU tal y como se define en Wincrypt. h.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
EKU.OID As String
```



## <a name="property-value"></a>Valor de propiedad

Cadena que contiene el valor de cadena OID del EKU tal y como se define en Wincrypt. h.

## <a name="remarks"></a>Observaciones

Esta propiedad no utiliza el objeto [**OID**](oid.md) incluido en CAPICOM 2,0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
