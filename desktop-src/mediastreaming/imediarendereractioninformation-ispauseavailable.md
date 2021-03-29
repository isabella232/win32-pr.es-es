---
title: IMediaRendererActionInformation IsPauseAvailable, método
description: Recupera un valor que indica si el DMR está aceptando actualmente el método PauseAsync.
ms.assetid: 095A664F-D974-410D-8741-87A171EDD071
keywords:
- Método IsPauseAvailable API de streaming de multimedia
- Método IsPauseAvailable API de streaming de multimedia, interfaz IMediaRendererActionInformation
- Interfaz IMediaRendererActionInformation API de streaming de multimedia, método IsPauseAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsPauseAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9eb0b750f5a04528aef830d87376c276bdaf6674
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904577"
---
# <a name="imediarendereractioninformationispauseavailable-method"></a>IMediaRendererActionInformation:: IsPauseAvailable (método)

Recupera un valor que indica si el DMR está aceptando actualmente el método [**PauseAsync**](imediarenderer-pauseasync.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsPauseAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*valor* \[ de enuncia\]
</dt> <dd>

Valor booleano que es **true** si el DMR está aceptando actualmente el método [**PauseAsync**](imediarenderer-pauseasync.md) y **false** si no lo está.

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

 

