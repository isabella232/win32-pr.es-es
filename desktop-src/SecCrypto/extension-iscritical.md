---
description: Recupera un valor booleano que indica si la extensión está marcada como crítica.
ms.assetid: 71f55d63-a51c-472c-81fc-59212c97bb34
title: Propiedad Extension.IsCritical
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extension.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f37f3c8549835da95949123aecc3a35b2aa896285bd3ec614228a6b851080468
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006883"
---
# <a name="extensioniscritical-property"></a>Propiedad Extension.IsCritical

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **propiedad IsCritical** recupera un valor booleano que indica si la extensión está marcada como crítica.

## <a name="syntax"></a>Syntax


```VB
Extension.IsCritical As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si **es true,** la extensión se marca como crítica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
