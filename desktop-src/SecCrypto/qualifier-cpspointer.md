---
description: Recupera el URI que señala a una declaración de prácticas de certificación (CPS) publicada por la entidad de certificación (CA).
ms.assetid: fd030c1c-137c-4036-bf13-ae989a9703cc
title: Propiedad Qualifier. CPSPointer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.CPSPointer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: db16e8faa25fc929e884358fcd885943adc17e32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650033"
---
# <a name="qualifiercpspointer-property"></a>Propiedad Qualifier. CPSPointer

\[La propiedad **CPSPointer** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para procesar calificadores que formen parte de la información de directivas en la extensión de directivas de certificado.\]

La propiedad **CPSPointer** recupera el URI que señala a una declaración de prácticas de certificación (CPS) publicada por la entidad de certificación (CA).

## <a name="syntax"></a>Sintaxis


```VB
Qualifier.CPSPointer As String
```



## <a name="property-value"></a>Valor de propiedad

El URI que apunta a una CPS publicada por la CA.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Qualifier**](qualifier.md)
</dt> </dl>

 

 
