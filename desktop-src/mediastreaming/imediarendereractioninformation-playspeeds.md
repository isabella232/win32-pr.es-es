---
title: IMediaRendererActionInformation PlaySpeeds, método
description: Recupera la lista completa de valores de PlaySpeed que acepta el DMR.
ms.assetid: 0AB63E39-6A26-4199-9978-A10866A7C805
keywords:
- Método PlaySpeeds API de streaming de multimedia
- Método PlaySpeeds API de streaming de multimedia, interfaz IMediaRendererActionInformation
- Interfaz IMediaRendererActionInformation API de streaming de multimedia, método PlaySpeeds
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.PlaySpeeds
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31089dd7616c035ebde4079c51988b94d1c27562
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358924"
---
# <a name="imediarendereractioninformationplayspeeds-method"></a>IMediaRendererActionInformation::P método laySpeeds

Recupera la lista completa de valores de [**PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) que acepta el DMR.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PlaySpeeds(
  [out] IVector< PlaySpeed > **value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*valor* \[ de enuncia\]
</dt> <dd>

Recibe un vector de estructuras [**PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) que especifica la lista completa de valores **PlaySpeed** aceptados por el DMR.

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

 

