---
title: Propiedad StreamSelectOperation. Completed
description: Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por SelectBestStreamAsync.
ms.assetid: 693CC002-2D91-4656-954D-8A556480155C
keywords:
- Propiedad completada API de streaming de multimedia
- Propiedad completada API de streaming multimedia, interfaz StreamSelectOperation
- Interfaz StreamSelectOperation API de streaming de multimedia, propiedad Completed
topic_type:
- apiref
api_name:
- StreamSelectOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74cfdf1a3db4f6843a5f12522b688e889e156f33
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105714364"
---
# <a name="streamselectoperationcompleted-property"></a>Propiedad StreamSelectOperation. Completed

Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) .

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Completed(
  [in]  IStreamSelectCompletedHandler *value
);

HRESULT get_Completed(
  [out] IStreamSelectCompletedHandler **value
);
```



## <a name="property-value"></a>Valor de propiedad

Controlador de eventos.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**StreamSelectOperation**](streamselectoperation.md)
</dt> </dl>

 

 