---
description: Inicializa un IWICColorTransform con un IWICBitmapSource y lo transforma de un IWICColorContext a otro.
ms.assetid: 68C8EF36-DFFF-4FF3-BD9A-583508F9C2B1
title: IWICColorTransform_Initialize_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICColorTransform_Initialize_Proxy
api_type:
- DllExport
api_location:
- WindowsCodecsExt.dll
ms.openlocfilehash: fcfe124d03e9ad41edb49554613bc18b2cd15818b3f52db7ca368e27f5c4fcc9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119841375"
---
# <a name="iwiccolortransform_initialize_proxy-function"></a>Función IWICColorTransform \_ Initialize \_ Proxy

Inicializa un [**IWICColorTransform con**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) [**un IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) y lo transforma de [**un IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) a otro.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICColorTransform_Initialize_Proxy(
  _In_ IWICColorTransform    *pIColorTransform,
  _In_ IWICBitmapSource      *pIBitmapSource,
  _In_ IWICColorContext      *pIContextSource,
  _In_ IWICColorContext      *pIContextDest,
  _In_ REFWICPixelFormatGUID pixelFmtDest
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pIColorTransform* \[ En\]
</dt> <dd>

Tipo: **[ **IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)\***

Transformación de color que se inicializará.

</dd> <dt>

*pIBitmapSource* \[ En\]
</dt> <dd>

Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

Origen de mapa de bits utilizado para inicializar la transformación de color.

</dd> <dt>

*pIContextSource* \[ En\]
</dt> <dd>

Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***

Origen del contexto de color.

</dd> <dt>

*pIContextDest* \[ En\]
</dt> <dd>

Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***

Destino del contexto de color.

</dd> <dt>

*pixelFmtDest* \[ En\]
</dt> <dd>

Tipo: **REFWICPixelFormatGUID**

GUID del formato de píxel deseado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-------------------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>WindowsCodecsExt.dll</dt> </dl> |



 

 




