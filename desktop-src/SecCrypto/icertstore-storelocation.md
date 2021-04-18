---
description: Establece o recupera la \_ \_ Ubicación del almacén de CAPICOM de un almacén de certificados.
ms.assetid: 2bb76f51-f092-4dbe-93e9-1fdc185c7c50
title: 'ICertStore:: StoreLocation (propiedad)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.StoreLocation
- ICertStore.get_StoreLocation
- ICertStore.put_StoreLocation
- CertStore.StoreLocation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 97bca7ed9dae20c129d202910b40f7c26d54a576
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670919"
---
# <a name="icertstorestorelocation-property"></a>ICertStore:: StoreLocation (propiedad)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.\]

La propiedad **StoreLocation** establece o recupera la [**\_ \_ Ubicación del almacén de CAPICOM**](capicom-store-location.md) de un almacén de certificados.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
CertStore.StoreLocation As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a>Valor de propiedad

Ubicación del almacén de certificados.

## <a name="error-codes"></a>Códigos de error

Si los métodos de acceso de propiedad **colocan \_ StoreLocation** y **Get \_ StoreLocation** se ejecutan correctamente, devuelven los valores \_ correctos.

Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ICertStore**](icertstore.md)
</dt> </dl>

 

 




