---
description: Este método devuelve una interfaz que proporciona acceso a los datos de audio.
ms.assetid: 4FA7CC9D-D379-4C08-8D4F-5301ECCDF372
title: IAudioFrameNative::GetData (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAudioFrameNative.GetData
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: 3d845cef0a4a9f6ee9d19b35705b20bd7e6bf2862a84ce4118acb92a5c66f37d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642125"
---
# <a name="iaudioframenativegetdata-method"></a>IAudioFrameNative::GetData (método)

Este método devuelve una interfaz que proporciona acceso a los datos de audio.

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

Tipo: **REFIID**

El IID de la interfaz que se recuperará.

</dd> <dt>

*ppv* \[ out\]
</dt> <dd>

Tipo: **LPVOID \***

Cuando este método se devuelve correctamente, contiene el puntero de interfaz solicitado en *el parámetro riid.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve S \_ OK cuando se completa correctamente. Devuelve E \_ NOINTERFACE si no se encuentra la interfaz solicitada.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAudioFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative)
</dt> </dl>

 

 



