---
description: Función de proxy para el método GetFileExtensions.
ms.assetid: 1c9232c5-54f3-4186-a1c8-4531e8357d06
title: IWICBitmapCodecInfo_GetFileExtensions_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetFileExtensions_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 7dc44622bb7d576bfe4dc8a70e69779a72c1c07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360245"
---
# <a name="iwicbitmapcodecinfo_getfileextensions_proxy-function"></a>IWICBitmapCodecInfo \_ GetFileExtensions \_ función proxy

Función de proxy para el método [**GetFileExtensions**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getfileextensions) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICBitmapCodecInfo_GetFileExtensions_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchFileExtensions,
  _Inout_ WCHAR               *wzFileExtensions,
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

*cchFileExtensions* \[ de\]
</dt> <dd>

Tipo: **uint**

Tamaño del búfer de extensión de nombre de archivo.

</dd> <dt>

*wzFileExtensions* \[ in, out\]
</dt> <dd>

Tipo: **WCHAR \** _

Puntero que recibe las extensiones de nombre de archivo asociadas al códec.

</dd> <dt>

_pcchActual * \[ in, out\]
</dt> <dd>

Tipo: **uint \** _

El tamaño de búfer real necesario para recuperar todas las extensiones de nombre de archivo asociadas al códec.

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



 

 




