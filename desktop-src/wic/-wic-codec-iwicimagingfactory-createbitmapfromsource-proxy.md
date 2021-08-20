---
description: Función de proxy para el método CreateBitmapFromSource.
ms.assetid: 7d000377-1855-4971-b782-4c0bf7968c5f
title: IWICImagingFactory_CreateBitmapFromSource_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromSource_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: f9904e96bd19e0b0453e8827f92e842a3424e30d6ba5b7cf72842112483c9587
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118033743"
---
# <a name="iwicimagingfactory_createbitmapfromsource_proxy-function"></a>Función IWICImagingFactory \_ CreateBitmapFromSource \_ Proxy

Función de proxy para [**el método CreateBitmapFromSource.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromsource)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICImagingFactory_CreateBitmapFromSource_Proxy(
  _In_  IWICImagingFactory         *pFactory,
  _In_  IWICBitmapSource           *pIBitmapSource,
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

*pIBitmapSource* \[ En\]
</dt> <dd>

Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

[**IWICBitmapSource desde**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) el que se crea el mapa de bits.

</dd> <dt>

*opción* \[ En\]
</dt> <dd>

Tipo: **[ **WICBitmapCreateCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**

Opciones de caché del nuevo mapa de bits.

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



 

 




