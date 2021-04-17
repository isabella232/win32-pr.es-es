---
description: Función de proxy para el método GetBitsPerPixel.
ms.assetid: bb98daeb-3886-473b-9c8e-5c606602249a
title: IWICPixelFormatInfo_GetBitsPerPixel_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetBitsPerPixel_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: f8d3469ca7c1eacf1f6755cbf5b6243527639d30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716711"
---
# <a name="iwicpixelformatinfo_getbitsperpixel_proxy-function"></a>IWICPixelFormatInfo \_ GetBitsPerPixel \_ función proxy

Función de proxy para el método [**GetBitsPerPixel**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getbitsperpixel) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICPixelFormatInfo_GetBitsPerPixel_Proxy(
  _In_  IWICPixelFormatInfo *THIS_PTR,
  _Out_ UINT                *puiBitsPerPixel
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Este \_ PTR* \[ en\]
</dt> <dd>

Tipo: **[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) \** _

Puntero a este objeto [_ *IWICPixelFormatInfo* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) .

</dd> <dt>

*puiBitsPerPixel* \[ enuncia\]
</dt> <dd>

Tipo: **uint \** _

Puntero que recibe el BPP del formato de píxel.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: _ *HRESULT**

Si esta función se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]<br/>                                                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                                                                             |
| Archivo DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




