---
description: Función de proxy para el método GetSize.
ms.assetid: a9b7d01c-78d9-47b8-a373-a7c49f7bccfd
title: IWICBitmapSource_GetSize_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetSize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 1a0892fea469180a0d06eded30e4459667513acbf66d56161d81788c1a17820f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711656"
---
# <a name="iwicbitmapsource_getsize_proxy-function"></a>Función de proxy GetSize de IWICBitmapSource \_ \_

Función de proxy para el [**método GetSize.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICBitmapSource_GetSize_Proxy(
  _In_  IWICBitmapSource *THIS_PTR,
  _Out_ UINT             *puiWidth,
  _Out_ UINT             *puiHeight
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*THIS \_ PTR* \[ en\]
</dt> <dd>

Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

Puntero a este [**objeto IWICBitmapSource.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)

</dd> <dt>

*puiWidth* \[ out\]
</dt> <dd>

Tipo: **UINT \***

Puntero que recibe el ancho de píxel del mapa de bits.

</dd> <dt>

*puiHeight* \[ out\]
</dt> <dd>

Tipo: **UINT \***

Puntero que recibe el alto de píxeles del mapa de bits

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP con SP2, solo Windows \[ aplicaciones de escritorio de Vista\]<br/>                                                                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                                                                             |
| Archivo DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




