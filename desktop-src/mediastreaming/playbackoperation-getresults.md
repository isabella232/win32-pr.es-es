---
title: Método PlaybackOperation.GetResults
description: Devuelve los resultados de una operación asincrónica iniciada por uno de los métodos de reproducción de MediaRenderer.
ms.assetid: EAA5B342-51EF-449A-A7E2-FFBDBE07757C
keywords:
- Método GetResults de Media Streaming API
- Método GetResults de Media Streaming API, interfaz PlaybackOperation
- Interfaz PlaybackOperation de Media Streaming API, método GetResults
topic_type:
- apiref
api_name:
- PlaybackOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9bd3c79164a78e7993eb8a58d0d89a64c7ceb31a0c33eaff2e9c1bc352144088
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235788"
---
# <a name="playbackoperationgetresults-method"></a>Método PlaybackOperation.GetResults

Devuelve los resultados de una operación asincrónica iniciada por uno de los métodos [**de reproducción de MediaRenderer.**](mediarenderer.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out, retval\]
</dt> <dd>

Resultado de la operación. Un valor de 0 indica que se completó la operación. Otros valores están reservados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Comentarios

Normalmente, se llama al método **GetResults** desde el controlador de eventos que se registró estableciendo la [**propiedad Completed.**](playbackoperation-completed.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[**PlaybackOperation**](playbackoperation.md)
</dt> </dl>

 

 





