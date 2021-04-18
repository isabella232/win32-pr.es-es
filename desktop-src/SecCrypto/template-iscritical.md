---
description: Recupera un valor booleano que indica si la extensión de plantilla está marcada como crítica.
ms.assetid: 37e2000a-d3c8-46b5-84e5-a3904fdbaeea
title: Propiedad template. IsCritical
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649853"
---
# <a name="templateiscritical-property"></a>Propiedad template. IsCritical

\[La propiedad **IsCritical** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID de la plantilla de certificado para recuperar la plantilla de extensión de certificado.\]

La propiedad **IsCritical** recupera un valor booleano que indica si la extensión de plantilla está marcada como crítica.

## <a name="syntax"></a>Sintaxis


```VB
Template.IsCritical As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si es **true**, la extensión de plantilla se marca como crítica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Plantilla**](template.md)
</dt> </dl>

 

 
