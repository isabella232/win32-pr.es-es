---
description: Este método devuelve un dispositivo asociado a los datos de vídeo.
ms.assetid: 9A61159B-C383-4770-AD8F-9F69F720E3E2
title: IVideoFrameNative::GetDevice (método)
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
ms.openlocfilehash: 7f204cc0d44690a2b80c8642d590ef38510cebedbc00332720ec51529fe34ad2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323114"
---
# <a name="ivideoframenativegetdevice-method"></a>IVideoFrameNative::GetDevice (método)

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

*riid* \[ En\]
</dt> <dd>

El IID del dispositivo que se recuperará.

</dd> <dt>

*ppv* \[ out\]
</dt> <dd>

Cuando este método se devuelve correctamente, contiene el puntero de dispositivo solicitado en *el parámetro riid.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK cuando se completa correctamente.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVideoFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



