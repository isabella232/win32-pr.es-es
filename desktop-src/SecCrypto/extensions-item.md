---
description: La propiedad Item recupera una extensión, por índice, de la colección. Esta es la propiedad predeterminada.
ms.assetid: 0242dc14-abf2-49df-b75a-9005b2376cfc
title: Extensions. Item (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extensions.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b2cefe9ac1dd278c17161cc8e2349c051dccabff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690211"
---
# <a name="extensionsitem-property"></a>Extensions. Item (propiedad)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propiedad **Item** recupera una extensión, por índice, de la colección. Esta es la propiedad predeterminada.

## <a name="syntax"></a>Sintaxis


```VB
Extensions.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Valor de propiedad

Objeto de [**extensión**](extension.md) que representa la extensión de certificado indizada de la colección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Extensiones**](extensions.md)
</dt> </dl>

 

 
