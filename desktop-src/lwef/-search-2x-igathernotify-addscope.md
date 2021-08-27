---
title: Método IGatherNotify AddScope (en desuso)
description: Este Windows interfaz de búsqueda de escritorio está en desuso y se reemplaza por la API ISearchPersistentItemsChangedSink de Windows Search en el SDK Windows. | Método IGatherNotify AddScope (en desuso)
ms.assetid: 3b250818-1876-40b2-9a85-91f2bf6f52ec
keywords:
- Método AddScope (en desuso) Heredado Windows environment
- Método AddScope (en desuso) Heredado Windows Environment Features , interfaz IGatherNotify
- IGatherNotify interface Legacy Windows Environment Features , AddScope (Deprecated) method
topic_type:
- apiref
api_name:
- IGatherNotify.AddScope (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a49c0cf652b0cfde59167fa98498a978d3c2c41d3a886ee092b8f4a28d35f61b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118755596"
---
# <a name="igathernotifyaddscope-deprecated-method"></a>Método IGatherNotify::AddScope (en desuso)

\[**AddScope** puede modificarse o no estar disponible en versiones posteriores del sistema operativo o del producto.\]

Este Windows interfaz de Búsqueda de escritorio está en desuso y se reemplaza por la API [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) de Windows Search en Windows SDK.

Agrega la página de inicio o la dirección URL que está supervisando. Esto inicia un rastreo incremental al conectarse y, a continuación, da por supuesto que todos los cambios de dirección URL adicionales se realizarán mediante notificación.

## <a name="syntax"></a>Sintaxis


```C++
void AddScope (Deprecated)(
  [in] BSTR bstrScope
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrScope* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Cadena que especifica la página de inicio o la DIRECCIÓN URL que está supervisando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Al llamar a este método, se inicia un rastreo incremental cuando se conecta al almacén. A partir de entonces, se supone que todos los cambios de dirección URL se realizarán mediante notificación después de la actualización inicial.

 

 
