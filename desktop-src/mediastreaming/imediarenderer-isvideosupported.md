---
title: IMediaRenderer IsVideoSupported, método
description: Recupera un valor que indica si el DMR es capaz de reproducir contenido de vídeo.
ms.assetid: AE9A14D0-A7A2-4A71-9454-06A05C7D85F9
keywords:
- Método IsVideoSupported API de streaming de multimedia
- Método IsVideoSupported API de streaming de multimedia, interfaz IMediaRenderer
- Interfaz IMediaRenderer API de streaming de multimedia, método IsVideoSupported
topic_type:
- apiref
api_name:
- IMediaRenderer.IsVideoSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9808841bf60a384d6a4566e75f53248b0f86338c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358260"
---
# <a name="imediarendererisvideosupported-method"></a>IMediaRenderer:: IsVideoSupported (método)

Recupera un valor que indica si el DMR es capaz de reproducir contenido de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsVideoSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*valor* \[ de enuncia\]
</dt> <dd>

Valor booleano que es **true** si el DMR es capaz de reproducir contenido de vídeo y **false** en caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMediaRenderer**](imediarenderer.md)
</dt> </dl>

 

 





