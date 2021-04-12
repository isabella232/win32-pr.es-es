---
description: Este método devuelve un dispositivo asociado a los datos de vídeo.
ms.assetid: 9A61159B-C383-4770-AD8F-9F69F720E3E2
title: 'IVideoFrameNative:: GetDevice (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVideoFrameNative.GetDevice
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: d012ae79b1cb2c83e916dc74113cc3d0560da4c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423784"
---
# <a name="ivideoframenativegetdevice-method"></a>IVideoFrameNative:: GetDevice (método)

Este método devuelve un dispositivo asociado a los datos de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDevice(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*riid* \[ de\]
</dt> <dd>

IID del dispositivo que se va a recuperar.

</dd> <dt>

*PPV* \[ enuncia\]
</dt> <dd>

Cuando este método se devuelve correctamente, contiene el puntero de dispositivo solicitado en el parámetro *riid* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto al finalizar correctamente.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVideoFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



