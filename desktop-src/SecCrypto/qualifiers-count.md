---
description: Recupera el número de objetos de calificador de la colección.
ms.assetid: 9dafb83a-ff7f-4317-8ed4-2a46dcebf409
title: Propiedad Qualifiers. Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ffb79941a78602bfda8f5287b0f4df7205d4d86
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691014"
---
# <a name="qualifierscount-property"></a>Propiedad Qualifiers. Count

\[La propiedad **Count** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para procesar calificadores que formen parte de la información de directivas en la extensión de directivas de certificado.\]

La propiedad **Count** recupera el número de objetos de [**calificador**](qualifier.md) de la colección.

## <a name="syntax"></a>Sintaxis


```VB
Qualifiers.Count As Long
```



## <a name="property-value"></a>Valor de propiedad

Número de objetos de [**calificador**](qualifier.md) de la colección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Calificadores**](qualifiers.md)
</dt> </dl>

 

 
