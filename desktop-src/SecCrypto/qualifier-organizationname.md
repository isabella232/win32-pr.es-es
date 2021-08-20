---
description: Recupera el nombre de la organización asociada al calificador.
ms.assetid: 4ceb2c0f-903d-4fcd-8446-abf3175fe8e0
title: Qualifier.OrganizationName, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.OrganizationName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f082a821779cc6e2182e88cf9742c87de0417e7ac297fda2f799ca5878d4ce67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117975775"
---
# <a name="qualifierorganizationname-property"></a>Qualifier.OrganizationName, propiedad

\[La **propiedad OrganizationName** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use la clase [**X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para procesar calificadores que forman parte de la información de directiva en la extensión Directivas de certificado.\]

La **propiedad OrganizationName** recupera el nombre de la organización asociada al calificador. Esta propiedad puede estar vacía.

## <a name="syntax"></a>Syntax


```VB
Qualifier.OrganizationName As String
```



## <a name="property-value"></a>Valor de propiedad

Nombre de la organización asociada al calificador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Qualifier**](qualifier.md)
</dt> </dl>

 

 
