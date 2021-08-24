---
title: Método IGatherNotify OnDataChange (en desuso)
description: Este Windows interfaz de búsqueda de escritorio está en desuso y se sustituye por la API Windows Search ISearchPersistentItemsChangedSink en el SDK Windows. | Método IGatherNotify OnDataChange (en desuso)
ms.assetid: 0cbfa6b7-44f0-41f0-93a3-d5941b5822de
keywords:
- Método OnDataChange (en desuso) Heredado Windows Environment Features
- Método OnDataChange (en desuso) Heredado Windows environment Features , IGatherNotify (interfaz)
- IGatherNotify interface Legacy Windows Environment Features , OnDataChange (Deprecated) method
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataChange (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 95533a7937136a0f828a292efe7e398258e3c880974e031d9d7d2797f721f2a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481599"
---
# <a name="igathernotifyondatachange-deprecated-method"></a>Método IGatherNotify::OnDataChange (en desuso)

\[**OnDataChange puede** modificarse o no estar disponible en versiones posteriores del sistema operativo o del producto.\]

Este Windows interfaz de búsqueda de escritorio está en desuso y se sustituye por la API Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) en el SDK Windows.

Este método notifica al indexador los datos que han cambiado. Cuando envía la notificación al indexador, incluye el tipo de cambio, la dirección física y la dirección lógica.

## <a name="syntax"></a>Sintaxis


```C++
void OnDataChange (Deprecated)(
  [in] long eChangeAdvise,
  [in] BSTR bstrPhysicalAddress,
  [in] BSTR bstrLogicalAddress
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*eChangeAdvise* \[ En\]
</dt> <dd>

Tipo: **long**

Valor enumerado que especifica el tipo de cambio.

</dd> <dt>

*bstrPhysicalAddress* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Dirección física del elemento que ha cambiado.

</dd> <dt>

*bstrLogicalAddress* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Dirección lógica del elemento que ha cambiado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

 

 
