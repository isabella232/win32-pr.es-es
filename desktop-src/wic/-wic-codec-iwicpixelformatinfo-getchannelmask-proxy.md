---
description: Función de proxy para el método GetChannelMask.
ms.assetid: c96e6078-4648-4333-8a25-bcb03a2cd50b
title: IWICPixelFormatInfo_GetChannelMask_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetChannelMask_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ee200dddf0b2cd736ca2ad435b63e774076465ad3d1f6215f1c558f1abb6c194
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056605"
---
# <a name="iwicpixelformatinfo_getchannelmask_proxy-function"></a>IWICPixelFormatInfo \_ GetChannelMask \_ Proxy function

Función de proxy para [**el método GetChannelMask.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelmask)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICPixelFormatInfo_GetChannelMask_Proxy(
  _In_    IWICPixelFormatInfo *THIS_PTR,
  _In_    UINT                uiChannelIndex,
  _In_    UINT                cbMaskBuffer,
  _Inout_ BYTE                *pbMaskBuffer,
  _Out_   UINT                *pcbActual
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*THIS \_ PTR* \[ en\]
</dt> <dd>

Tipo: **[ **IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)\***

Puntero a este [**objeto IWICPixelFormatInfo.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)

</dd> <dt>

*uiChannelIndex* \[ En\]
</dt> <dd>

Tipo: **UINT**

Índice de la máscara de canal que se recuperará.

</dd> <dt>

*cbMaskBuffer* \[ En\]
</dt> <dd>

Tipo: **UINT**

Tamaño del búfer *pbMaskBuffer.*

</dd> <dt>

*pbMaskBuffer* \[ in, out\]
</dt> <dd>

Tipo: **\* BYTE**

Puntero al búfer de máscara.

</dd> <dt>

*actual* \[ out\]
</dt> <dd>

Tipo: **UINT \***

Tamaño de búfer real necesario para obtener la máscara de canal.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP con SP2, solo Windows \[ aplicaciones de escritorio de Vista\]<br/>                                                                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                                                                             |
| Archivo DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




