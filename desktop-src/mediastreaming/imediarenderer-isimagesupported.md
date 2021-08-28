---
title: Método IsImageSupported de IMediaRenderer
description: Recupera un valor que indica si la DMR es capaz de mostrar imágenes.
ms.assetid: 3941789B-0FFF-4F00-B63C-2586B39B6546
keywords:
- Método IsImageSupported de Media Streaming API
- Método IsImageSupported de Media Streaming API, interfaz IMediaRenderer
- IMediaRenderer interface Media Streaming API , Método IsImageSupported
topic_type:
- apiref
api_name:
- IMediaRenderer.IsImageSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1fae20b6b5486586e305723a1d6a29a885bf0db8b8741ab9e6881fb292f35d6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461645"
---
# <a name="imediarendererisimagesupported-method"></a>IMediaRenderer::IsImageSupported (método)

Recupera un valor que indica si la DMR es capaz de mostrar imágenes.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsImageSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Valor booleano que es **True si** la DMR es capaz de mostrar imágenes y **False** si no lo es.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMediaRenderer**](imediarenderer.md)
</dt> </dl>

 

 





