---
title: IMediaRendererActionInformation IsMuteAvailable, método
description: Recupera un valor que indica si el DMR es capaz de silenciar el audio.
ms.assetid: F744C2D7-5518-4A9F-A71E-60CF0B312177
keywords:
- Método IsMuteAvailable API de streaming de multimedia
- Método IsMuteAvailable API de streaming de multimedia, interfaz IMediaRendererActionInformation
- Interfaz IMediaRendererActionInformation API de streaming de multimedia, método IsMuteAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsMuteAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96751a7f2f1aedcd9e29be981ffadf6c43bf4008
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077639"
---
# <a name="imediarendereractioninformationismuteavailable-method"></a>IMediaRendererActionInformation:: IsMuteAvailable (método)

Recupera un valor que indica si el DMR es capaz de silenciar el audio.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsMuteAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*valor* \[ de enuncia\]
</dt> <dd>

Valor booleano que es **true** si el DMR es capaz de silenciar el audio y **false** si no lo es.

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

 

