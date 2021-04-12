---
title: IGatherNotify parámetro addscope (deprecated) (método)
description: Este tema de la interfaz de búsqueda en el escritorio de Windows está en desuso y se ha sustituido por la API ISearchPersistentItemsChangedSink de Windows Search en el Windows SDK. | IGatherNotify parámetro addscope (deprecated) (método)
ms.assetid: 3b250818-1876-40b2-9a85-91f2bf6f52ec
keywords:
- Parámetro addscope (obsoleto) características de entorno de Windows heredado
- Parámetro addscope (obsoleto) características de entorno heredado de Windows, interfaz IGatherNotify
- Interfaz IGatherNotify características del entorno heredado de Windows, parámetro addscope (en desuso) (método)
topic_type:
- apiref
api_name:
- IGatherNotify.AddScope (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 967dc4f30acee2f8d8adbcfec04f0508e53bba15
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362201"
---
# <a name="igathernotifyaddscope-deprecated-method"></a>IGatherNotify:: parámetro addscope (deprecated) (método)

\[**Parámetro addscope** puede modificarse o no estar disponible en versiones posteriores del sistema operativo o del producto.\]

Este tema de la interfaz de búsqueda en el escritorio de Windows está en desuso y se ha sustituido por la API [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) de Windows Search en el Windows SDK.

Agrega la página de inicio o la dirección URL que está supervisando. Esto inicia un rastreo incremental al conectarse y, a continuación, asume que todos los cambios de dirección URL adicionales son por notificación.

## <a name="syntax"></a>Sintaxis


```C++
void AddScope (Deprecated)(
  [in] BSTR bstrScope
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrScope* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Una cadena que especifica la página de inicio o el URLthat que está supervisando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La llamada a este método inicia un rastreo incremental cuando se conecta al almacén. A partir de ese momento, se supone que todos los cambios de dirección URL son por notificación después de la actualización inicial.

 

 
