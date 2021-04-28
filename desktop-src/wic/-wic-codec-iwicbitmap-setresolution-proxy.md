---
description: 'IWICBitmap_SetResolution_Proxy función: función proxy para el método SetResolution.'
ms.assetid: c4e3927c-6f9d-401d-acd7-711674cdbb53
title: IWICBitmap_SetResolution_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_SetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: f11189307ad14dde6ea1e1373583a8ab4b08b9be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086383"
---
# <a name="iwicbitmap_setresolution_proxy-function"></a>Función IWICBitmap \_ SetResolution \_ Proxy

Función de proxy para el [**método SetResolution.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setresolution)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICBitmap_SetResolution_Proxy(
  _In_ IWICBitmap *THIS_PTR,
  _In_ double     dpiX,
  _In_ double     dpiY
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*THIS \_ PTR* \[ en\]
</dt> <dd>

Tipo: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***

Puntero a este [**objeto IWICBitmap.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)

</dd> <dt>

*pppX* \[ En\]
</dt> <dd>

Tipo: **double**

Resolución horizontal.

</dd> <dt>

*pppY* \[ En\]
</dt> <dd>

Tipo: **double**

Resolución vertical.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP con SP2, solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                                                                             |
| Archivo DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




