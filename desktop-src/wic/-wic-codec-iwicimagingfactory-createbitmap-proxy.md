---
description: Función de proxy para el método CreateBitmap.
ms.assetid: 5647521b-231d-4819-97ab-4dfb5f796211
title: IWICImagingFactory_CreateBitmap_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmap_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 978946b5c22d8e4cb3427dbf27e5bb745efde259b48811a2b2a82e3721108184
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965204"
---
# <a name="iwicimagingfactory_createbitmap_proxy-function"></a>Función IWICImagingFactory \_ CreateBitmap \_ Proxy

Función de proxy para el [**método CreateBitmap.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmap)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICImagingFactory_CreateBitmap_Proxy(
  _In_  IWICImagingFactory         *pFactory,
  _In_  UINT                       uiWidth,
  _In_  UINT                       uiHeight,
  _In_  REFWICPixelFormatGUID      pixelFormat,
  _In_  WICBitmapCreateCacheOption option,
  _Out_ IWICBitmap                 **ppIBitmap
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFactory* \[ En\]
</dt> <dd>

Tipo: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\***

</dd> <dt>

*uiWidth* \[ En\]
</dt> <dd>

Tipo: **UINT**

Ancho del nuevo mapa de bits.

</dd> <dt>

*uiHeight* \[ En\]
</dt> <dd>

Tipo: **UINT**

Alto del nuevo mapa de bits.

</dd> <dt>

*pixelFormat* \[ En\]
</dt> <dd>

Tipo: **REFWICPixelFormatGUID**

Formato de píxel del nuevo mapa de bits.

</dd> <dt>

*opción* \[ En\]
</dt> <dd>

Tipo: **[ **WICBitmapCreateCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**

Opciones de creación de caché del nuevo mapa de bits.

</dd> <dt>

*ppIBitmap* \[ out\]
</dt> <dd>

Tipo: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***

Puntero que recibe un puntero al nuevo mapa de bits.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP con SP2, solo Windows aplicaciones \[ de escritorio de Vista\]<br/>                                                                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                                                                             |
| Archivo DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




