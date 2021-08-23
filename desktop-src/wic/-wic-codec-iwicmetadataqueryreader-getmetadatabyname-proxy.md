---
description: Función de proxy para el método GetMetadataByName.
ms.assetid: 5685e282-637e-4db0-8654-fee12ae25112
title: IWICMetadataQueryReader_GetMetadataByName_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetMetadataByName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c84d8d6e93c3f5edf223811844937fd1d223a1a3df991e9d62dd24c2fa445ce9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088237"
---
# <a name="iwicmetadataqueryreader_getmetadatabyname_proxy-function"></a>Función IWICMetadataQueryReader \_ GetMetadataByName \_ Proxy

Función de proxy para [**el método GetMetadataByName.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getmetadatabyname)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICMetadataQueryReader_GetMetadataByName_Proxy(
  _In_    IWICMetadataQueryReader *THIS_PTR,
  _In_    LPCWSTR                 wzName,
  _Inout_ PROPVARIANT             *pvarValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*THIS \_ PTR* \[ en\]
</dt> <dd>

Tipo: **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\***

Puntero a este [**objeto IWICMetadataQueryReader.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)

</dd> <dt>

*wzName* \[ En\]
</dt> <dd>

Tipo: **LPCWSTR**

Nombre del elemento de metadatos solicitado.

</dd> <dt>

*pvarValue* \[ in, out\]
</dt> <dd>

Tipo: **[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\***

Puntero que recibe la propiedad de metadatos.

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



 

