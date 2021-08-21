---
description: Función de proxy para negociar el formato de píxeles y la paleta del codificador.
ms.assetid: 01179598-ba40-4aed-a7c4-888cb4e851f4
title: WICSetEncoderFormat_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICSetEncoderFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3343e6f80193a4cb37dba98ffa3320bd8d56ee8bb9f14159adbf2474c767ed03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812065"
---
# <a name="wicsetencoderformat_proxy-function"></a>Función de proxy WICSetEncoderFormat \_

Función de proxy para negociar el formato de píxeles y la paleta del codificador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WICSetEncoderFormat_Proxy(
  _In_  IWICBitmapSource      *pSourceIn,
  _In_  IWICPalette           *pIPalette,
  _In_  IWICBitmapFrameEncode *pIFrameEncode,
  _Out_ IWICBitmapSource      **ppSourceOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSourceIn* \[ En\]
</dt> <dd>

Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

Puntero al mapa de bits de origen.

</dd> <dt>

*pIPalette* \[ En\]
</dt> <dd>

Tipo: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***

Puntero a la paleta que se usará para la codificación.

</dd> <dt>

*pIFrameEncode* \[ En\]
</dt> <dd>

Tipo: **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***

Puntero al objeto de codificación de marco.

</dd> <dt>

*ppSourceOut* \[ out\]
</dt> <dd>

Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***

Puntero que recibe un puntero al origen de salida.

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



 

 




