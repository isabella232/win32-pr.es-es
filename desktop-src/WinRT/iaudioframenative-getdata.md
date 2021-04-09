---
description: Este método devuelve una interfaz que proporciona acceso a los datos de audio.
ms.assetid: 4FA7CC9D-D379-4C08-8D4F-5301ECCDF372
title: 'IAudioFrameNative:: GetData (método)'
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
ms.openlocfilehash: eb61bce5132c2029b6f53fdd1159ca50984ba936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154306"
---
# <a name="iaudioframenativegetdata-method"></a>IAudioFrameNative:: GetData (método)

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

*riid* \[ de\]
</dt> <dd>

Tipo: **REFIID**

IID de la interfaz que se va a recuperar.

</dd> <dt>

*PPV* \[ enuncia\]
</dt> <dd>

Tipo: **LPVOID \** _

Cuando este método se devuelve correctamente, contiene el puntero de interfaz solicitado en _riid parámetro *.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve S \_ correcto al finalizar correctamente. Devuelve E \_ nointerface si no se encuentra la interfaz solicitada.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAudioFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative)
</dt> </dl>

 

 



