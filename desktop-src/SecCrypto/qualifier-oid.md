---
description: Recupera el identificador de objeto del calificador.
ms.assetid: 58ec2af7-f085-43bc-8ea8-926cb840abe9
title: Propiedad Qualifier.OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 42c2f83d4fa8be31991a98b6fe4cfc6a741e2190cd12d54bfd5e968951472bcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901055"
---
# <a name="qualifieroid-property"></a>Propiedad Qualifier.OID

\[La **propiedad OID** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use la clase [**X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para procesar calificadores que forman parte de la información de directiva en la extensión Directivas de certificado.\]

La **propiedad OID** recupera el identificador de objeto del calificador. Esta es la propiedad predeterminada.

## <a name="syntax"></a>Sintaxis


```VB
Qualifier.OID As OID
```



## <a name="property-value"></a>Valor de propiedad

Objeto [**OID**](oid.md) que identifica el calificador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Qualifier**](qualifier.md)
</dt> </dl>

 

 
