---
title: IGatherNotify OnDataMove (deprecated) (método)
description: Este tema de la interfaz de búsqueda en el escritorio de Windows está en desuso y se ha sustituido por la API ISearchPersistentItemsChangedSink de Windows Search en el Windows SDK. | IGatherNotify OnDataMove (deprecated) (método)
ms.assetid: cc223d0f-6508-4e38-b365-c60660db5324
keywords:
- OnDataMove (obsoleto) características de entorno de Windows heredado
- OnDataMove (obsoleto) características de entorno heredado de Windows, interfaz IGatherNotify
- Interfaz IGatherNotify características del entorno heredado de Windows, OnDataMove (en desuso) (método)
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataMove (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9fe38cd11e9072981334e5b724445ea3393d4361
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362200"
---
# <a name="igathernotifyondatamove-deprecated-method"></a>IGatherNotify:: OnDataMove (deprecated) (método)

\[**OnDataMove** puede modificarse o no estar disponible en versiones posteriores del sistema operativo o del producto.\]

Este tema de la interfaz de búsqueda en el escritorio de Windows está en desuso y se ha sustituido por la API [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) de Windows Search en el Windows SDK.

Este método notifica al indizador de los datos que se han despasado. Cuando envía la notificación al indexador, incluye la dirección anterior, la nueva dirección y la dirección lógica.

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

*eChangeAdviseSemantics* \[ de\]
</dt> <dd>

Tipo: **Long**

Parámetro enumerado que describe el tipo de movimiento que se ha producido.

</dd> <dt>

*bstrOldAddress* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Dirección antigua del elemento que se ha desplace. En el caso de los archivos normales,*eChangeAdviseSematics* es **null**. En el caso de una carpeta o directorio, establezca *eChangeAdviseSematics* en el \_ directorio GTHR CA \_ Semantics \_ .

</dd> <dt>

*bstrNewAddress* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Nueva dirección del elemento que se ha despasado.

</dd> <dt>

*bstrLogicalAddress* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Dirección lógica del elemento que se ha despasado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

 

 
