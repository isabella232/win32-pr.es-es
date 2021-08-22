---
description: Recupera un valor booleano que indica si la extensión de plantilla está presente.
ms.assetid: cc7f9853-8212-470d-b372-43a4bbd517f7
title: Propiedad Template.IsPresent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0492f6abccf2ade6e652dba2c4ea13d9bbfc28f1a3d3c34008eb3338ccb1e426
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897400"
---
# <a name="templateispresent-property"></a>Propiedad Template.IsPresent

\[La **propiedad IsPresent** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use la clase [**X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID de la plantilla de certificado para recuperar la plantilla de extensión de certificado.\]

La **propiedad IsPresent** recupera un valor booleano que indica si la extensión de plantilla está presente.

## <a name="syntax"></a>Syntax


```VB
Template.IsPresent As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si **es true,** la extensión de plantilla está presente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Plantilla**](template.md)
</dt> </dl>

 

 
