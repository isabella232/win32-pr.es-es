---
description: Establece o recupera la UBICACIÓN DEL ALMACÉN CAPICOM \_ de un almacén de \_ certificados.
ms.assetid: 2bb76f51-f092-4dbe-93e9-1fdc185c7c50
title: Propiedad ICertStore::StoreLocation
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
ms.openlocfilehash: ea11da4fc908a2a3b665b2491614dbffeaa3034a3127617c562c3365522df835
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005613"
---
# <a name="icertstorestorelocation-property"></a>Propiedad ICertStore::StoreLocation

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.\]

La **propiedad StoreLocation** establece o recupera la [**UBICACIÓN DE CAPICOM \_ STORE \_**](capicom-store-location.md) de un almacén de certificados.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
CertStore.StoreLocation As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a>Valor de propiedad

Ubicación del almacén de certificados.

## <a name="error-codes"></a>Códigos de error

Si los métodos de acceso de **propiedad \_ ponen StoreLocation** **y \_ obtienen StoreLocation** correctamente, devuelven S \_ OK.

Cualquier otro **valor HRESULT** indica que se ha dado error en la llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ICertStore**](icertstore.md)
</dt> </dl>

 

 




