---
description: Recupera la ubicación del almacén de certificados que representa este objeto.
ms.assetid: 756ee7cb-5f9f-4fb2-bf10-79b543895189
title: Store.Location, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Location
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 42afe40dffde5a0375928d355508ec75a4076f17
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071144"
---
# <a name="storelocation-property"></a>Store.Location, propiedad

\[La **propiedad** Ubicación está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use [**la clase X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **propiedad Location** recupera la ubicación del almacén de certificados que representa este objeto.

## <a name="syntax"></a>Sintaxis


```VB
Store.Location As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a>Valor de propiedad

Valor [**CAPICOM \_ STORE LOCATION \_ que**](capicom-store-location.md) representa la ubicación del almacén de certificados.

## <a name="remarks"></a>Observaciones

El valor de la **propiedad Location** es el mismo que el valor proporcionado para el parámetro *StoreLocation* del [**método Open**](store-open.md) cuando se abrió el almacén.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.1 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tienda**](store.md)
</dt> </dl>

 

 
