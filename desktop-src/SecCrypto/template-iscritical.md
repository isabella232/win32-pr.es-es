---
description: Recupera un valor booleano que indica si la extensión de plantilla está marcada como crítica.
ms.assetid: 37e2000a-d3c8-46b5-84e5-a3904fdbaeea
title: Template.IsCritical, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 66f9dc90828cd474497478872f154adbd3fcd12a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160706"
---
# <a name="templateiscritical-property"></a>Template.IsCritical, propiedad

\[La **propiedad IsCritical** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use la clase [**X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para plantilla de certificado para recuperar la plantilla de extensión de certificado.\]

La **propiedad IsCritical** recupera un valor booleano que indica si la extensión de plantilla está marcada como crítica.

## <a name="syntax"></a>Sintaxis


```VB
Template.IsCritical As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si **es true,** la extensión de plantilla se marca como crítica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Plantilla**](template.md)
</dt> </dl>

 

 
