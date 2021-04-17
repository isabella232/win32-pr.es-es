---
title: MediaRenderer. PauseAsync, método
description: Indica al DMR de forma asincrónica que PAUSE la reproducción del contenido actual. | MediaRenderer. PauseAsync, método
ms.assetid: 1bd36349-0551-44e8-9550-3fd80900de9a
keywords:
- Método PauseAsync API de streaming de multimedia
- Método PauseAsync API de streaming de multimedia, interfaz MediaRenderer
- Interfaz MediaRenderer API de streaming de multimedia, método PauseAsync
topic_type:
- apiref
api_name:
- MediaRenderer.PauseAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2bbbc55931c7cc7fc5e2e5ec39ba63fe7a064478
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105717523"
---
# <a name="mediarendererpauseasync-method"></a>MediaRenderer. PauseAsync, método

Indica al DMR de forma asincrónica que PAUSE la reproducción del contenido actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PauseAsync(
  [out] PlaybackOperation **value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*valor* \[ de enuncia\]
</dt> <dd>

Recibe una referencia a un objeto [**PlaybackOperation**](playbackoperation.md) que se usa para obtener los resultados de la operación asincrónica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**MediaRenderer**](mediarenderer.md)
</dt> </dl>

 

 





