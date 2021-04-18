---
description: Función de proxy para el método GetDeviceManufacturer.
ms.assetid: f4dbf67a-eb67-4138-a77a-7386567b95e6
title: IWICBitmapCodecInfo_GetDeviceManufacturer_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetDeviceManufacturer_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3dc10df32325fd0ffc5bb24d1a4c7927b1adc7e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715066"
---
# <a name="iwicbitmapcodecinfo_getdevicemanufacturer_proxy-function"></a>IWICBitmapCodecInfo \_ GetDeviceManufacturer \_ función proxy

Función de proxy para el método [**GetDeviceManufacturer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemanufacturer) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICBitmapCodecInfo_GetDeviceManufacturer_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchDeviceManufacturer,
  _Inout_ WCHAR               *wzDeviceManufacturer,
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

*cchDeviceManufacturer* \[ de\]
</dt> <dd>

Tipo: **uint**

Tamaño del nombre del fabricante del dispositivo.

</dd> <dt>

*wzDeviceManufacturer* \[ in, out\]
</dt> <dd>

Tipo: **WCHAR \** _

Puntero que recibe el nombre del fabricante del dispositivo.

</dd> <dt>

_pcchActual * \[ in, out\]
</dt> <dd>

Tipo: **uint \** _

Tamaño de búfer real necesario para recuperar el nombre del fabricante del dispositivo.

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



 

 




