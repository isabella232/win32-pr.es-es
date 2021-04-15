---
description: Inicializa un IWICColorTransform con IWICBitmapSource y lo transforma de un IWICColorContext a otro.
ms.assetid: 68C8EF36-DFFF-4FF3-BD9A-583508F9C2B1
title: IWICColorTransform_Initialize_Proxy función)
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
ms.openlocfilehash: 29d29bfd925d979897b22711c748083b94673142
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708787"
---
# <a name="iwiccolortransform_initialize_proxy-function"></a>IWICColorTransform \_ inicializar \_ función de proxy

Inicializa un [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) con [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) y lo transforma de un [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) a otro.

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

*pIColorTransform* \[ de\]
</dt> <dd>

Tipo: **[ **IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)\***

Transformación de color que se va a inicializar.

</dd> <dt>

*pIBitmapSource* \[ de\]
</dt> <dd>

Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

Origen de mapa de bits utilizado para inicializar la transformación de color.

</dd> <dt>

*pIContextSource* \[ de\]
</dt> <dd>

Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***

Origen del contexto de color.

</dd> <dt>

*pIContextDest* \[ de\]
</dt> <dd>

Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***

El destino del contexto de color.

</dd> <dt>

*pixelFmtDest* \[ de\]
</dt> <dd>

Tipo: **REFWICPixelFormatGUID**

GUID del formato de píxel deseado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si esta función se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-------------------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>WindowsCodecsExt.dll</dt> </dl> |



 

 




