---
title: IGatherNotify OnDataChange (deprecated) (método)
description: Este tema de la interfaz de búsqueda en el escritorio de Windows está en desuso y se ha sustituido por la API ISearchPersistentItemsChangedSink de Windows Search en el Windows SDK. | IGatherNotify OnDataChange (deprecated) (método)
ms.assetid: 0cbfa6b7-44f0-41f0-93a3-d5941b5822de
keywords:
- OnDataChange (obsoleto) características de entorno de Windows heredado
- OnDataChange (obsoleto) características de entorno heredado de Windows, interfaz IGatherNotify
- Interfaz IGatherNotify características del entorno heredado de Windows, OnDataChange (en desuso) (método)
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataChange (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d41edeaa591a7f3cbc9494064906af1815597737
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698114"
---
# <a name="igathernotifyondatachange-deprecated-method"></a>IGatherNotify:: OnDataChange (deprecated) (método)

\[**OnDataChange** puede modificarse o no estar disponible en versiones posteriores del sistema operativo o del producto.\]

Este tema de la interfaz de búsqueda en el escritorio de Windows está en desuso y se ha sustituido por la API [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) de Windows Search en el Windows SDK.

Este método notifica al indizador de los datos que han cambiado. Cuando envía la notificación al indexador, incluye el tipo de cambio, la dirección física y la dirección lógica.

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

*eChangeAdvise* \[ de\]
</dt> <dd>

Tipo: **Long**

Valor enumerado que especifica el tipo de cambio.

</dd> <dt>

*bstrPhysicalAddress* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Dirección física del elemento que ha cambiado.

</dd> <dt>

*bstrLogicalAddress* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Dirección lógica del elemento que ha cambiado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

 

 
