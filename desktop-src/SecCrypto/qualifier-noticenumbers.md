---
description: Recupera la colección de números de aviso de usuario.
ms.assetid: 5db38a53-e71b-4e80-9374-69b0c044fbc5
title: Propiedad Qualifier. NoticeNumbers
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
ms.openlocfilehash: 2ef9b2c4c70e011cc33f0aa9d9f2bbcc9f530bec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649878"
---
# <a name="qualifiernoticenumbers-property"></a>Propiedad Qualifier. NoticeNumbers

\[La propiedad **NoticeNumbers** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para procesar calificadores que formen parte de la información de directivas en la extensión de directivas de certificado.\]

La propiedad **NoticeNumbers** recupera la colección de números de aviso de usuario. Esta propiedad puede estar vacía.

## <a name="syntax"></a>Sintaxis


```VB
Qualifier.NoticeNumbers As NoticeNumbers
```



## <a name="property-value"></a>Valor de propiedad

La colección de números de aviso de usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Qualifier**](qualifier.md)
</dt> </dl>

 

 
