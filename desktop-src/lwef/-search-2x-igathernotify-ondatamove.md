---
title: Método IGatherNotify OnDataMove (en desuso)
description: Este Windows interfaz de búsqueda de escritorio está en desuso y se sustituye por la API Windows Search ISearchPersistentItemsChangedSink en el SDK Windows. | Método IGatherNotify OnDataMove (en desuso)
ms.assetid: cc223d0f-6508-4e38-b365-c60660db5324
keywords:
- Método OnDataMove (en desuso) Heredado Windows Environment Features
- Método OnDataMove (en desuso) Heredado Windows Environment Features , IGatherNotify (interfaz)
- IGatherNotify interface Legacy Windows Environment Features , OnDataMove (Deprecated) method
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataMove (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2f3d4f7d91bc9e9741f227812997a820ab4180ccf438d52ae8cfea93f67dc0bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665875"
---
# <a name="igathernotifyondatamove-deprecated-method"></a>Método IGatherNotify::OnDataMove (en desuso)

\[**OnDataMove** puede modificarse o no estar disponible en versiones posteriores del sistema operativo o del producto.\]

Este Windows interfaz de búsqueda de escritorio está en desuso y se sustituye por la API Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) en el SDK Windows.

Este método notifica al indexador los datos que se han movido. Cuando envía la notificación al indexador, incluye la dirección antigua, la nueva dirección y la dirección lógica.

## <a name="syntax"></a>Sintaxis


```C++
void OnDataMove (Deprecated)(
  [in] long eChangeAdviseSemantics,
  [in] BSTR bstrOldAddress,
  [in] BSTR bstrNewAddress,
  [in] BSTR bstrLogicalAddress
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*eChangeAdviseSemantics* \[ En\]
</dt> <dd>

Tipo: **long**

Parámetro enumerado que describe el tipo de movimiento que se ha producido.

</dd> <dt>

*bstrOldAddress* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Dirección antigua del elemento que se movió. Para los archivos normales,*eChangeAdviseSematics* es **NULL.** Para una carpeta o directorio, establezca *eChangeAdviseSematics en* GTHR \_ CA \_ SEMANTICS \_ DIRECTORY.

</dd> <dt>

*bstrNewAddress* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Nueva dirección del elemento que se ha movido.

</dd> <dt>

*bstrLogicalAddress* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Dirección lógica del elemento que se ha movido.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

 

 
