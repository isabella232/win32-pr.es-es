---
description: Recupera el contenido del aviso de usuario.
ms.assetid: dcf73357-253d-4160-be4e-f826296f5eaa
title: Qualifier.ExplicitText, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.ExplicitText
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 60753e0e7fa9996f9584070d6fac2d12d3a483b681fa61b72cf2e59cc2898995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901116"
---
# <a name="qualifierexplicittext-property"></a>Qualifier.ExplicitText, propiedad

\[La **propiedad ExplicitText** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use la clase [**X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para procesar calificadores que forman parte de la información de directiva en la extensión Directivas de certificado.\]

La **propiedad ExplicitText** recupera el contenido del aviso de usuario. Esta propiedad puede estar vacía.

## <a name="syntax"></a>Syntax


```VB
Qualifier.ExplicitText As String
```



## <a name="property-value"></a>Valor de propiedad

Contenido del aviso de usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Qualifier**](qualifier.md)
</dt> </dl>

 

 
