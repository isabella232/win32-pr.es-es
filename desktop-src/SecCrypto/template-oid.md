---
description: Recupera un objeto OID que identifica el objeto de plantilla.
ms.assetid: bdd9d401-e9c4-4307-9817-7dcb55c539f8
title: Template. OID (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4a8599ac999c7d6a3e3403d94ff2c6daf0eba48b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649976"
---
# <a name="templateoid-property"></a>Template. OID (propiedad)

\[La propiedad **OID** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID de la plantilla de certificado para recuperar la plantilla de extensión de certificado.\]

La propiedad **OID** recupera un objeto [**OID**](oid.md) que identifica el objeto de [**plantilla**](template.md) .

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Template.OID As OID
```



## <a name="property-value"></a>Valor de propiedad

Objeto [**OID**](oid.md) que identifica el objeto de [**plantilla**](template.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Plantilla**](template.md)
</dt> </dl>

 

 
