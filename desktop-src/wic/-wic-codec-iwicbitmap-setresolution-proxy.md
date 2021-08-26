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
ms.openlocfilehash: a32fa4e0d830d5307bc2927a1d5b6cb0a40e5b21f86517dc4421a0ce246a2ab8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056705"
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



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP con SP2, solo Windows aplicaciones \[ de escritorio de Vista\]<br/>                                                                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                                                                             |
| Archivo DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




