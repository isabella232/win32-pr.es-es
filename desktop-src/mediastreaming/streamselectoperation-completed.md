---
title: Propiedad StreamSelectOperation.Completed
description: Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por SelectBestStreamAsync.
ms.assetid: 693CC002-2D91-4656-954D-8A556480155C
keywords:
- Propiedad completada Media Streaming API
- Propiedad completada Media Streaming API, interfaz StreamSelectOperation
- Interfaz StreamSelectOperation Media Streaming API, propiedad Completed
topic_type:
- apiref
api_name:
- StreamSelectOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 554874c19054f4b2ee46fbfe29fb4dfb8149e476ff96d040ffdbdd9b39de4612
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847585"
---
# <a name="streamselectoperationcompleted-property"></a>Propiedad StreamSelectOperation.Completed

Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por [**SelectBestStreamAsync.**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85))

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Completed(
  [in]  IStreamSelectCompletedHandler *value
);

HRESULT get_Completed(
  [out] IStreamSelectCompletedHandler **value
);
```



## <a name="property-value"></a>Valor de propiedad

Controlador de eventos.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**StreamSelectOperation**](streamselectoperation.md)
</dt> </dl>

 

 