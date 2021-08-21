---
description: Recupera una colección de calificadores de la directiva.
ms.assetid: aa5e2225-0a39-40bc-868c-d96f5953edaa
title: Propiedad PolicyInformation.Qualifiers (Iads.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation.Qualifiers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 14184d8fd338d8b7dbfe34519b815a8fac38c6212d887c2c7d1bc9ad9a6ce058
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117978586"
---
# <a name="policyinformationqualifiers-property"></a>Propiedad PolicyInformation.Qualifiers

\[La **propiedad Calificadores** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use la clase [**X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para procesar la información de directiva en la extensión de directivas de certificado.\]

La **propiedad Qualifiers** recupera una colección de calificadores de la directiva.

## <a name="syntax"></a>Syntax


```VB
PolicyInformation.Qualifiers As Qualifiers
```



## <a name="property-value"></a>Valor de propiedad

Calificadores de aviso de usuario o puntero de instrucción de práctica de certificación (CPS) de la directiva, como [**un objeto Qualifiers.**](qualifiers.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Header<br/>          | <dl> <dt>Iads.h</dt> </dl>      |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PolicyInformation**](policyinformation.md)
</dt> </dl>

 

 
