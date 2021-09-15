---
description: Recupera un valor booleano que indica si la extensión KeyUsage está presente.
ms.assetid: d666049a-4b40-42b6-8c2d-c27a1bb4c48a
title: KeyUsage.IsPresent, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f70754c15a248cda69f93fcab2a0052bd8351261
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473460"
---
# <a name="keyusageispresent-property"></a>KeyUsage.IsPresent, propiedad

\[La **propiedad IsPresent** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use la clase [**X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **propiedad IsPresent** recupera un valor booleano que indica si la [**extensión KeyUsage**](keyusage.md) está presente.

Esta propiedad es la propiedad predeterminada del [**objeto KeyUsage.**](keyusage.md)

## <a name="syntax"></a>Sintaxis


```VB
KeyUsage.IsPresent As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si **es true**, la extensión KeyUsage está presente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
