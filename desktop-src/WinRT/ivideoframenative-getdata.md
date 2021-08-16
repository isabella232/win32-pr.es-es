---
description: Este método devuelve una interfaz que proporciona acceso a los datos de vídeo.
ms.assetid: 084F020F-A6F5-4982-BA4B-A8F8D6182868
title: IVideoFrameNative::GetData (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVideoFrameNative.GetData
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: 832b2e300887699b926362ce9cbfc6f334c181805bacb3546532920c684251d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993775"
---
# <a name="ivideoframenativegetdata-method"></a>IVideoFrameNative::GetData (método)

Este método devuelve una interfaz que proporciona acceso a los datos de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetData(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*riid* \[ En\]
</dt> <dd>

El IID de la interfaz que se recuperará.

</dd> <dt>

*ppv* \[ out\]
</dt> <dd>

Cuando este método se devuelve correctamente, contiene el puntero de interfaz solicitado en *el parámetro riid.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK cuando se completa correctamente. Devuelve E NOINTERFACE si no se encuentra \_ la interfaz solicitada.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVideoFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



