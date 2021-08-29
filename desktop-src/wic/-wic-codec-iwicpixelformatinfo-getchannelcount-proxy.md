---
description: Función de proxy para el método GetChannelCount.
ms.assetid: f74916d9-d4b5-4b1b-adba-489d46c8d81c
title: IWICPixelFormatInfo_GetChannelCount_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetChannelCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: eaaf0abc2c32e7a5a4469a3959875e28bb29d840f9da43f9bbbcc88fe56df788
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812125"
---
# <a name="iwicpixelformatinfo_getchannelcount_proxy-function"></a>Función de proxy IWICPixelFormatInfo \_ GetChannelCount \_

Función de proxy para el [**método GetChannelCount.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelcount)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICPixelFormatInfo_GetChannelCount_Proxy(
  _In_  IWICPixelFormatInfo *THIS_PTR,
  _Out_ UINT                *puiChannelCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*THIS \_ PTR* \[ en\]
</dt> <dd>

Tipo: **[ **IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)\***

Puntero a este [**objeto IWICPixelFormatInfo.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)

</dd> <dt>

*puiChannelCount* \[ out\]
</dt> <dd>

Tipo: **UINT \***

Puntero que recibe el recuento de canales.

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



 

 




