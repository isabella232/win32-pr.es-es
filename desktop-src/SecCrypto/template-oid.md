---
description: Recupera un objeto OID que identifica el objeto Template.
ms.assetid: bdd9d401-e9c4-4307-9817-7dcb55c539f8
title: Propiedad Template.OID
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
ms.openlocfilehash: ecfc56210d5fa81f6e7623b2c471cf0df1b5f091f7dab6c797b56f6af8d2496e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897390"
---
# <a name="templateoid-property"></a>Propiedad Template.OID

\[La **propiedad OID** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use la clase [**X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID de la plantilla de certificado para recuperar la plantilla de extensión de certificado.\]

La **propiedad OID** recupera un objeto [**OID**](oid.md) que identifica el [**objeto Template.**](template.md)

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Template.OID As OID
```



## <a name="property-value"></a>Valor de propiedad

Objeto [**OID**](oid.md) que identifica el [**objeto Template.**](template.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Plantilla**](template.md)
</dt> </dl>

 

 
