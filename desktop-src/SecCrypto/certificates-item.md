---
description: Recupera un objeto Certificate que representa el certificado indexado de la colección. Esta es la propiedad predeterminada.
ms.assetid: 733f2b93-c059-4041-b7cd-8c20218f1462
title: Propiedad Certificates.Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 927f52570b515c6699458cfb802b5c315201d401e9bcf5e0be76ab41863bd47e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770544"
---
# <a name="certificatesitem-property"></a>Propiedad Certificates.Item

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase X509Certificate2Collection en**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **propiedad Item** recupera un objeto [**Certificate**](certificate.md) que representa el certificado indexado de la colección. Esta es la propiedad predeterminada.

## <a name="syntax"></a>Syntax


```VB
Certificates.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Valor de propiedad

Objeto [**Certificate**](certificate.md) que representa el certificado indexado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Certificados**](certificates.md)
</dt> </dl>

 

 
