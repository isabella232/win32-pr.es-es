---
description: Función de proxy para el método GetDeviceModels.
ms.assetid: de8f91f7-fef7-48bc-94fc-34c43175248b
title: IWICBitmapCodecInfo_GetDeviceModels_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetDeviceModels_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b8fa6d6df6984569aa3fe49fc734f7699aa504d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715065"
---
# <a name="iwicbitmapcodecinfo_getdevicemodels_proxy-function"></a>IWICBitmapCodecInfo \_ GetDeviceModels \_ función proxy

Función de proxy para el método [**GetDeviceModels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemodels) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICBitmapCodecInfo_GetDeviceModels_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchDeviceModels,
  _Inout_ WCHAR               *wzDeviceModels,
  _Inout_ UINT                *pcchActual
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Este \_ PTR* \[ en\]
</dt> <dd>

Tipo: **[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _

Puntero a este objeto [_ *IWICBitmapCodecInfo* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .

</dd> <dt>

*cchDeviceModels* \[ de\]
</dt> <dd>

Tipo: **uint**

Tamaño del búfer de modelos de dispositivo.

</dd> <dt>

*wzDeviceModels* \[ in, out\]
</dt> <dd>

Tipo: **WCHAR \** _

Un puntero que recibe una lista delimitada por comas de nombres de modelo de dispositivo asociados al códec.

</dd> <dt>

_pcchActual * \[ in, out\]
</dt> <dd>

Tipo: **uint \** _

Tamaño de búfer real necesario para recuperar todos los nombres de modelo de dispositivo.

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



 

 




