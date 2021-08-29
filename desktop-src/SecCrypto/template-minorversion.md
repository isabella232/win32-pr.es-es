---
description: Recupera el número de versión secundaria de la plantilla.
ms.assetid: 3fc51d43-9113-4b4b-88ab-27cf6e5c4fa0
title: Propiedad Template.MinorVersion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.MinorVersion
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 695bde72274f9fe1e6df6e77eed1f956052a46201ae4be10e0848e8285cfa3b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897410"
---
# <a name="templateminorversion-property"></a>Propiedad Template.MinorVersion

\[La **propiedad MinorVersion** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use la clase [**X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID de la plantilla de certificado para recuperar la plantilla de extensión de certificado.\]

La **propiedad MinorVersion** recupera el número de versión secundaria de la plantilla.

## <a name="syntax"></a>Syntax


```VB
Template.MinorVersion As Long
```



## <a name="property-value"></a>Valor de propiedad

Número de versión secundaria de la plantilla.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Plantilla**](template.md)
</dt> </dl>

 

 
