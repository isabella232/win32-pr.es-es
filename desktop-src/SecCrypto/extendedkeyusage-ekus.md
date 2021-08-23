---
description: Devuelve la colección EKUs del certificado.
ms.assetid: 64211a00-7d4d-4381-a134-9cd570ed7dbb
title: Propiedad ExtendedKeyUsage.EKUs
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.EKUs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6b6cb0ee020935ea80bc0d676ad8979267396589a46604f49a5cb833d68eefa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007403"
---
# <a name="extendedkeyusageekus-property"></a>Propiedad ExtendedKeyUsage.EKUs

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la clase [**X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **propiedad EKUs** devuelve la [**colección EKUs**](ekus.md) del certificado.

## <a name="syntax"></a>Syntax


```VB
ExtendedKeyUsage.EKUs As EKUs
```



## <a name="property-value"></a>Valor de propiedad

Colección [**EKUs**](ekus.md) que contiene los [**objetos EKU**](eku.md) para el certificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ExtendedKeyUsage**](extendedkeyusage.md)
</dt> </dl>

 

 
