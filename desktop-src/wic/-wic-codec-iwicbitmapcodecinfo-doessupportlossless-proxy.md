---
description: Función de proxy para el método DoesSupportLossless.
ms.assetid: c88d7971-cc93-458c-a31e-19a8b8350d09
title: IWICBitmapCodecInfo_DoesSupportLossless_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_DoesSupportLossless_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: f102a487e76667cc3a1cfb9c3bf0c2153d661199b36cbef86fec3f7f111d2f46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090065"
---
# <a name="iwicbitmapcodecinfo_doessupportlossless_proxy-function"></a>IWICBitmapCodecInfo \_ DoesSupportLossless \_ Proxy function

Función de proxy para [**el método DoesSupportLossless.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportlossless)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICBitmapCodecInfo_DoesSupportLossless_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ BOOL                *pfSupportLossless
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*THIS \_ PTR* \[ en\]
</dt> <dd>

Tipo: **[ **IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\***

Puntero a este [**objeto IWICBitmapCodecInfo.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)

</dd> <dt>

*pfSupportLossless* \[ out\]
</dt> <dd>

Tipo: **BOOL \***

Puntero que recibe **TRUE si** el códec admite formatos sin pérdida de datos; de lo contrario, **FALSE**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP con SP2, solo Windows \[ aplicaciones de escritorio de Vista\]<br/>                                                                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                                                                             |
| Archivo DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




