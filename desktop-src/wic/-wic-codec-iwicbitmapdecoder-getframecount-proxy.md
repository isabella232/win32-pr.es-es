---
description: Función de proxy para el método GetFrameCount.
ms.assetid: 2103af73-60a2-4c1c-8db2-7dfd474440eb
title: IWICBitmapDecoder_GetFrameCount_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetFrameCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: de2fd241a9a5d805bcbd0114836183aec2212394f2823e2484ea77fe66a32ee9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117668604"
---
# <a name="iwicbitmapdecoder_getframecount_proxy-function"></a>Función de proxy GetFrameCount de IWICBitmapDecoder \_ \_

Función de proxy para el [**método GetFrameCount.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICBitmapDecoder_GetFrameCount_Proxy(
  _In_  IWICBitmapDecoder *THIS_PTR,
  _Out_ UINT              *pCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*THIS \_ PTR* \[ en\]
</dt> <dd>

Tipo: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***

Puntero a este [**objeto IWICBitmapDecoder.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)

</dd> <dt>

*pCount* \[ out\]
</dt> <dd>

Tipo: **UINT \***

Puntero que recibe el número total de fotogramas de la imagen.

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



 

 




