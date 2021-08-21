---
description: Recupera el número de versión principal de la plantilla.
ms.assetid: efde3a7c-48e0-4bfe-9118-3098c7ef8771
title: Propiedad Template.MajorVersion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.MajorVersion
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ce6564dcf1dfcdc00e9b4f9e246ee5d81f6255ef171be734625456aedad8b2f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117972126"
---
# <a name="templatemajorversion-property"></a>Propiedad Template.MajorVersion

\[La **propiedad MajorVersion** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use la clase [**X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID de la plantilla de certificado para recuperar la plantilla de extensión de certificado.\]

La **propiedad MajorVersion** recupera el número de versión principal de la plantilla.

## <a name="syntax"></a>Syntax


```VB
Template.MajorVersion As Long
```



## <a name="property-value"></a>Valor de propiedad

Número de versión principal de la plantilla.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Plantilla**](template.md)
</dt> </dl>

 

 
