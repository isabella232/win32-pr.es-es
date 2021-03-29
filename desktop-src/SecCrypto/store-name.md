---
description: Recupera el nombre del almacén de certificados que este objeto representa.
ms.assetid: db61b464-0e8e-4b19-be12-04e00d6bba53
title: Propiedad Store.Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 85679bb594bdb59c41773b7f956deea95021381f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650199"
---
# <a name="storename-property"></a>Propiedad Store.Name

\[La propiedad [**nombre**](store-location.md) está disponible para su uso en los sistemas operativos especificados en la sección requisitos. En su lugar, use la [**clase X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propiedad [**Name**](store-location.md) recupera el nombre del almacén de certificados que este objeto representa.

## <a name="syntax"></a>Sintaxis


```VB
Store.Name As String
```



## <a name="property-value"></a>Valor de propiedad

Valor de **cadena** que representa el nombre del almacén de certificados.

## <a name="remarks"></a>Observaciones

Algunos ejemplos de nombres de almacenes de certificados son My y root.

El valor de la propiedad [**Name**](store-location.md) es el mismo que el valor proporcionado para el parámetro *StoreName* del método [**Open**](store-open.md) cuando se abrió el almacén.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,1 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Store**](store.md)
</dt> </dl>

 

 
