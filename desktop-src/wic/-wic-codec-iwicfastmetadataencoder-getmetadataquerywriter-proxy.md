---
description: 'IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy función: función proxy para el método GetMetadataQueryWriter.'
ms.assetid: 64d2c6d8-f1dd-4397-8487-4d23c69aea82
title: IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b06bc6fbcdc65c9d1163ccb4a862d6046b455c9a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097173"
---
# <a name="iwicfastmetadataencoder_getmetadataquerywriter_proxy-function"></a>Función IWICFastMetadataEncoder \_ GetMetadataQueryWriter \_ Proxy

Función de proxy para [**el método GetMetadataQueryWriter.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-getmetadataquerywriter)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapFrameDecode   *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*THIS \_ PTR* \[ en\]
</dt> <dd>

Tipo: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***

Puntero a este [**objeto IWICBitmapFrameDecode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)

</dd> <dt>

*ppIMetadataQueryWriter* \[ out\]
</dt> <dd>

Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***

Puntero que recibe un puntero al escritor de consultas de metadatos del codificador.

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



 

 




