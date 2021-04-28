---
description: 'IWICBitmapEncoder_Commit_Proxy función: función de proxy para el método Commit.'
ms.assetid: f7f1be43-fe44-47eb-a5ba-3446c0db22a6
title: IWICBitmapEncoder_Commit_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_Commit_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 934b2e21097a671c2b52ea77ab07caf25ab521a3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091193"
---
# <a name="iwicbitmapencoder_commit_proxy-function"></a>Función IWICBitmapEncoder \_ Commit \_ Proxy

Función de proxy para el [**método Commit.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICBitmapEncoder_Commit_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*THIS \_ PTR* \[ en\]
</dt> <dd>

Tipo: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***

Puntero a este [**objeto IWICBitmapEncoder.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)

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



 

 




