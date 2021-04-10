---
title: IMediaRendererActionInformation IsStopAvailable, método
description: Recupera un valor que indica si el DMR está aceptando actualmente el método StopAsync.
ms.assetid: 6EE8F56D-2A5A-49B0-A9B2-0A7EE57D03FD
keywords:
- Método IsStopAvailable API de streaming de multimedia
- Método IsStopAvailable API de streaming de multimedia, interfaz IMediaRendererActionInformation
- Interfaz IMediaRendererActionInformation API de streaming de multimedia, método IsStopAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsStopAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e0a031bafc9a755dfec2498f4e2a52cdd9ef5b1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149244"
---
# <a name="imediarendereractioninformationisstopavailable-method"></a>IMediaRendererActionInformation:: IsStopAvailable (método)

Recupera un valor que indica si el DMR está aceptando actualmente el método [**StopAsync**](imediarenderer-stopasync.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsStopAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*valor* \[ de enuncia\]
</dt> <dd>

Valor booleano que es **true** si el DMR está aceptando actualmente el método [**StopAsync**](imediarenderer-stopasync.md) y **false** si no lo está.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

