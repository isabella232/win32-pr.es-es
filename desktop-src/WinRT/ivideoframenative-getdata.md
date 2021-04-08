---
description: Este método devuelve una interfaz que proporciona acceso a los datos de vídeo.
ms.assetid: 084F020F-A6F5-4982-BA4B-A8F8D6182868
title: 'IVideoFrameNative:: GetData (método)'
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
ms.openlocfilehash: c612d2d34e23b393921f83f7dbe9e189aa366b30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001147"
---
# <a name="ivideoframenativegetdata-method"></a>IVideoFrameNative:: GetData (método)

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

*riid* \[ de\]
</dt> <dd>

IID de la interfaz que se va a recuperar.

</dd> <dt>

*PPV* \[ enuncia\]
</dt> <dd>

Cuando este método se devuelve correctamente, contiene el puntero de interfaz solicitado en el parámetro *riid* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto al finalizar correctamente. Devuelve E \_ nointerface si no se encuentra la interfaz solicitada.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVideoFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



