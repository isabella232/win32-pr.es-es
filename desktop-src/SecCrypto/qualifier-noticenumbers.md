---
description: Recupera la colección de números de aviso de usuario.
ms.assetid: 5db38a53-e71b-4e80-9374-69b0c044fbc5
title: Qualifier.NoticeNumbers, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.NoticeNumbers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f45954107dd452243985d246524fb3e1826e6361fd3d72583a27ec7a33c5960f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117975812"
---
# <a name="qualifiernoticenumbers-property"></a>Qualifier.NoticeNumbers, propiedad

\[La **propiedad NoticeNumbers** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use la clase [**X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para procesar calificadores que forman parte de la información de directiva en la extensión Directivas de certificado.\]

La **propiedad NoticeNumbers** recupera la colección de números de aviso de usuario. Esta propiedad puede estar vacía.

## <a name="syntax"></a>Syntax


```VB
Qualifier.NoticeNumbers As NoticeNumbers
```



## <a name="property-value"></a>Valor de propiedad

Colección de números de aviso de usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Qualifier**](qualifier.md)
</dt> </dl>

 

 
