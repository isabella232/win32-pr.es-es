---
description: Función de proxy para el método CreateBitmapFromMemory.
ms.assetid: 5aa455d5-23e3-4738-b028-b84da0fb0c50
title: IWICImagingFactory_CreateBitmapFromMemory_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e7f5567f2ead2b68440e448a9a03f36fdedceb5d31ecfc579f7df956988dfc01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118033918"
---
# <a name="iwicimagingfactory_createbitmapfrommemory_proxy-function"></a>Función IWICImagingFactory \_ CreateBitmapFromMemory \_ Proxy

Función de proxy para [**el método CreateBitmapFromMemory.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfrommemory)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICImagingFactory_CreateBitmapFromMemory_Proxy(
  _In_  IWICImagingFactory    *pFactory,
  _In_  UINT                  uiWidth,
  _In_  UINT                  uiHeight,
  _In_  REFWICPixelFormatGUID pixelFormat,
  _In_  UINT                  cbStride,
  _In_  UINT                  cbBufferSize,
  _In_  BYTE                  *pbBuffer,
  _Out_ IWICBitmap            **ppIBitmap
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

*cbStride* \[ En\]
</dt> <dd>

Tipo: **UINT**

El [*paso de*](/windows) los datos de píxeles dados.

</dd> <dt>

*cbBufferSize* \[ En\]
</dt> <dd>

Tipo: **UINT**

Tamaño de *pbBuffer.*

</dd> <dt>

*pbBuffer* \[ En\]
</dt> <dd>

Tipo: **\* BYTE**

Búfer utilizado para crear el mapa de bits.

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
| Cliente mínimo compatible<br/> | Windows XP con SP2, solo Windows de \[ escritorio de Vista\]<br/>                                                                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                                                                             |
| Archivo DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

