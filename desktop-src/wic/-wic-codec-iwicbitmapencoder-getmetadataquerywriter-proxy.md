---
description: 'IWICBitmapEncoder_GetMetadataQueryWriter_Proxy función: función proxy para el método GetMetadataQueryWriter.'
ms.assetid: 3186d473-f8a7-405a-8429-3f50104bee4a
title: IWICBitmapEncoder_GetMetadataQueryWriter_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 798a9b5bafb2f5011e42e603b8b2c98b0ba79b37
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091173"
---
# <a name="iwicbitmapencoder_getmetadataquerywriter_proxy-function"></a>Función IWICBitmapEncoder \_ GetMetadataQueryWriter \_ Proxy

Función de proxy para [**el método GetMetadataQueryWriter.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICBitmapEncoder_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapEncoder       *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*THIS \_ PTR* \[ en\]
</dt> <dd>

Tipo: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***

Puntero a este [**objeto IWICBitmapEncoder.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)

</dd> <dt>

*ppIMetadataQueryWriter* \[ out\]
</dt> <dd>

Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***

Puntero que recibe un puntero a [**un objeto IWICMetadataQueryWriter.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)

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



 

 




