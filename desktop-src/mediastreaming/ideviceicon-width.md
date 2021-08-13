---
title: Método IDeviceIcon Width
description: Recupera el ancho del icono en píxeles.
ms.assetid: 28ADA921-6808-43B8-966E-BA42B1B52931
keywords:
- Media Streaming API de método de ancho
- Método de ancho Media Streaming API, interfaz IDeviceIcon
- IDeviceIcon interface Media Streaming API , método Width
topic_type:
- apiref
api_name:
- IDeviceIcon.Width
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cc76fcd7915c350e04cbacfe756e424d31b0d27d5ced38b0ccf8664805fc9bb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118473467"
---
# <a name="ideviceiconwidth-method"></a>IDeviceIcon::Width (Método)

Recupera el ancho del icono en píxeles.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Width(
  [out] UINT32 *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Recibe un puntero al ancho del icono en píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

