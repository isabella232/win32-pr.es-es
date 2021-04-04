---
title: IMediaRendererFactory CreateMediaRendererAsync, método
description: Crea de forma asincrónica una nueva instancia de un objeto que implementa la interfaz IMediaRenderer con el nombre de dispositivo único especificado (UDN).
ms.assetid: FD1242F8-4C2E-4027-B1DE-5FD69557684C
keywords:
- Método CreateMediaRendererAsync API de streaming de multimedia
- Método CreateMediaRendererAsync API de streaming de multimedia, interfaz IMediaRendererFactory
- Interfaz IMediaRendererFactory API de streaming de multimedia, método CreateMediaRendererAsync
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b152e5889ad83440a48e178be0b89a97d2a9f664
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790563"
---
# <a name="imediarendererfactorycreatemediarendererasync-method"></a>IMediaRendererFactory:: CreateMediaRendererAsync (método)

Crea de forma asincrónica una nueva instancia de un objeto que implementa la interfaz [**IMediaRenderer**](imediarenderer.md) con el nombre de dispositivo único especificado (UDN).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateMediaRendererAsync(
  [in]          HSTRING                      deviceIdentifier,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*deviceIdentifier* \[ de\]
</dt> <dd>

Un HSTRING que contiene un UDN que identifica el dispositivo DMR de DLNA para el que se creará una instancia de [**IMediaRenderer**](imediarenderer.md) .

</dd> <dt>

*valor* \[ de out, retval\]
</dt> <dd>

Recibe una referencia a un objeto [**CreateMediaRendererOperation**](createmediarendereroperation.md) que se usa para obtener los resultados de la operación asincrónica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMediaRendererFactory**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

