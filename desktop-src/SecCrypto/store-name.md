---
description: Recupera el nombre del almacén de certificados que representa este objeto.
ms.assetid: db61b464-0e8e-4b19-be12-04e00d6bba53
title: Store.Name propiedad
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071139"
---
# <a name="storename-property"></a>Store.Name propiedad

\[La [**propiedad**](store-location.md) Name está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use [**la clase X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La [**propiedad Name**](store-location.md) recupera el nombre del almacén de certificados que representa este objeto.

## <a name="syntax"></a>Sintaxis


```VB
Store.Name As String
```



## <a name="property-value"></a>Valor de propiedad

Valor **string** que representa el nombre del almacén de certificados.

## <a name="remarks"></a>Observaciones

Algunos ejemplos de nombres de almacén de certificados son My y Root.

El valor de la [**propiedad Name**](store-location.md) es el mismo que el valor proporcionado para el parámetro *StoreName* del método [**Open**](store-open.md) cuando se abrió el almacén.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.1 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tienda**](store.md)
</dt> </dl>

 

 
