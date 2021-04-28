---
description: 'IWICBitmapCodecInfo_GetContainerFormat_Proxy función: función proxy para el método GetContainerFormat.'
ms.assetid: d8a2387a-fb75-4812-b046-51359071281d
title: IWICBitmapCodecInfo_GetContainerFormat_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetContainerFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 729b4e2fe0f21fd1e96082e53194fd49bbc39ae1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086373"
---
# <a name="iwicbitmapcodecinfo_getcontainerformat_proxy-function"></a>Función IWICBitmapCodecInfo \_ GetContainerFormat \_ Proxy

Función de proxy para [**el método GetContainerFormat.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICBitmapCodecInfo_GetContainerFormat_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ GUID                *pguidContainerFormat
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*THIS \_ PTR* \[ en\]
</dt> <dd>

Tipo: **[ **IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\***

Puntero a este [**objeto IWICBitmapCodecInfo.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)

</dd> <dt>

*pguidContainerFormat* \[ out\]
</dt> <dd>

Tipo: **\* GUID**

Puntero que recibe el GUID del contenedor.

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



 

 




