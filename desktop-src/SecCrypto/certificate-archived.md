---
description: Establece o recupera un valor booleano que indica si el certificado está archivado.
ms.assetid: a6526b0e-e76b-4f03-a6ba-9e380e362364
title: Propiedad Certificate.Archived
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Archived
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d2e3ab848caa24cb77a8cb45e992eeac7365af0de743fa148b07b484239fa658
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771954"
---
# <a name="certificatearchived-property"></a>Propiedad Certificate.Archived

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **propiedad Archived** establece o recupera un valor booleano que indica si el certificado está archivado.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
Certificate.Archived As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Valor booleano que indica si se archiva el certificado. Si **es true,** el certificado se archiva. Tenga en cuenta que al cambiar el valor **de false** **a true** se archiva el certificado.

## <a name="remarks"></a>Comentarios

Esta propiedad genera CAPICOM \_ E NOT ALLOWED cuando se crea un script desde una aplicación basada en \_ \_ web.

> [!Note]  
> Un certificado archivado no está visible en la interfaz de usuario de administración de certificados. Además, los certificados archivados no se incluirán en el método [**Store.Open**](store-open.md) a menos que se especifique CAPICOM \_ STORE OPEN INCLUDE \_ \_ \_ ARCHIVED.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
