---
description: Recupera el número de objetos EKU de la colección.
ms.assetid: a38ac480-4f9b-4d69-a7e6-fae4993fe2cf
title: Propiedad EKUs.Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4ef512c62058d2f4726c21aa8631fef5230ec35ecfe39a3b8dc5470fc93b74e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767169"
---
# <a name="ekuscount-property"></a>Propiedad EKUs.Count

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **propiedad Count** recupera el número de objetos [**EKU**](eku.md) de la colección.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
EKUs.Count As Long
```



## <a name="property-value"></a>Valor de propiedad

Número de objetos [**EKU**](eku.md) de la colección. Cada **objeto EKU** representa una única propiedad de uso de clave extendida (EKU) de un certificado.

## <a name="remarks"></a>Comentarios

La **propiedad Count** se puede usar para especificar el último objeto [**EKU**](eku.md) de una colección al recuperar un objeto **EKU** específico mediante la [**propiedad EKUs.Item.**](ekus-item.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
