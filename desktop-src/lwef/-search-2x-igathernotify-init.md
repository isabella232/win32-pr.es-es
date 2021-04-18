---
title: IGatherNotify init (deprecated) (método)
description: Este tema de la interfaz de búsqueda en el escritorio de Windows está en desuso y se ha sustituido por la API ISearchPersistentItemsChangedSink de Windows Search en el Windows SDK. | IGatherNotify init (deprecated) (método)
ms.assetid: 6a5f89eb-10f4-4262-89bf-b47e345f12eb
keywords:
- Init (obsoleto) características del entorno de Windows heredado
- Init (obsoleto) características del entorno heredado de Windows, interfaz IGatherNotify
- Interfaz IGatherNotify características del entorno heredado de Windows, método init (obsoleto)
topic_type:
- apiref
api_name:
- IGatherNotify.Init (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81379bb4a9a7c6099912bfc9ebca170141d76cd2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698115"
---
# <a name="igathernotifyinit-deprecated-method"></a>IGatherNotify:: init (deprecated) (método)

\[**Init** puede modificarse o no estar disponible en versiones posteriores del sistema operativo o del producto.\]

Este tema de la interfaz de búsqueda en el escritorio de Windows está en desuso y se ha sustituido por la API [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) de Windows Search en el Windows SDK.

Inicializa la interfaz del recopilador. También especifica el índice al que se va a notificar y el almacén de aplicaciones que se va a supervisar.

## <a name="syntax"></a>Sintaxis


```C++
void Init (Deprecated)(
  [in] BSTR    bstrApplication,
  [in] BSTR    bstrProject,
  [in] variant varScopesBstrArray
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrApplication* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Cadena que especifica la aplicación de destino.

</dd> <dt>

*bstrProject* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Cadena que especifica el nombre del indizador al que se va a pasar la información del recopilador.

</dd> <dt>

*varScopesBstrArray* \[ de\]
</dt> <dd>

Tipo: **variante**

Parámetro opcional, que permite pasar una matriz de ámbitos que se van a inicializar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Inicialice con Application = "RSApp", Project = "alindex".

 

 
