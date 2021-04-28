---
description: 'IWICBitmapEncoder_Initialize_Proxy función: función de proxy para el método Initialize.'
ms.assetid: 0db79eb4-dcb2-491a-9bea-a0dec418f80f
title: IWICBitmapEncoder_Initialize_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d346d1379ae92f19a530c65daff07cb98b2e0e50
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100623"
---
# <a name="iwicbitmapencoder_initialize_proxy-function"></a>IWICBitmapEncoder \_ Initialize \_ Proxy function

Función de proxy para el [**método Initialize.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICBitmapEncoder_Initialize_Proxy(
  _In_ IWICBitmapEncoder           *THIS_PTR,
  _In_ IStream                     *pIStream,
  _In_ WICBitmapEncoderCacheOption cacheOption
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*THIS \_ PTR* \[ en\]
</dt> <dd>

Tipo: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***

Puntero a este [**objeto IWICBitmapEncoder.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)

</dd> <dt>

*pIStream* \[ En\]
</dt> <dd>

Tipo: **[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\***

Secuencia de salida.

</dd> <dt>

*cacheOption* \[ En\]
</dt> <dd>

Tipo: **[ **WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption)**

[**WICBitmapEncoderCacheOption usado**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) en la inicialización.

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



 

