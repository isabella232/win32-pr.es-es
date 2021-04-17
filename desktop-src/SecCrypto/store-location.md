---
description: Recupera la ubicación del almacén de certificados que este objeto representa.
ms.assetid: 756ee7cb-5f9f-4fb2-bf10-79b543895189
title: Store. Location (propiedad)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650175"
---
# <a name="storelocation-property"></a>Store. Location (propiedad)

\[La propiedad **Ubicación** está disponible para su uso en los sistemas operativos especificados en la sección requisitos. En su lugar, use la [**clase X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propiedad **Location** recupera la ubicación del almacén de certificados que este objeto representa.

## <a name="syntax"></a>Sintaxis


```VB
Store.Location As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a>Valor de propiedad

Valor [**de \_ \_ Ubicación del almacén de CAPICOM**](capicom-store-location.md) que representa la ubicación del almacén de certificados.

## <a name="remarks"></a>Observaciones

El valor de la propiedad **Location** es el mismo que el valor proporcionado para el parámetro *StoreLocation* del método [**Open**](store-open.md) cuando se abre el almacén.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,1 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Store**](store.md)
</dt> </dl>

 

 
