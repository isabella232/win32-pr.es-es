---
title: MediaRenderer. StopAsync, método
description: Indica al DMR de forma asincrónica que detenga la reproducción del contenido actual. | MediaRenderer. StopAsync, método
ms.assetid: 04cf6d5a-8aa5-4821-8117-f250bfaf7ebd
keywords:
- Método StopAsync API de streaming de multimedia
- Método StopAsync API de streaming de multimedia, interfaz MediaRenderer
- Interfaz MediaRenderer API de streaming de multimedia, método StopAsync
topic_type:
- apiref
api_name:
- MediaRenderer.StopAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 205c69a83572539974c1b8ad2cf45159c45335cb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104157108"
---
# <a name="mediarendererstopasync-method"></a>MediaRenderer. StopAsync, método

Indica al DMR de forma asincrónica que detenga la reproducción del contenido actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT StopAsync(
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

 

 





