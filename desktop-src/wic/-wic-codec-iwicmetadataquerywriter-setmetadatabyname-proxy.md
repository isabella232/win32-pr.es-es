---
description: Función de proxy para el método SetMetadataByName.
ms.assetid: 467d7735-152a-4e7c-93b1-fd031cc57c19
title: IWICMetadataQueryWriter_SetMetadataByName_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryWriter_SetMetadataByName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 5ec3d018856b087762de70d6e2aea3e1f473db96b7ad989a62b3dfc2b5d3e691
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206390"
---
# <a name="iwicmetadataquerywriter_setmetadatabyname_proxy-function"></a>Función IWICMetadataQueryWriter \_ SetMetadataByName \_ Proxy

Función de proxy para [**el método SetMetadataByName.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-setmetadatabyname)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICMetadataQueryWriter_SetMetadataByName_Proxy(
  _In_       IWICMetadataQueryWriter *THIS_PTR,
  _In_       LPCWSTR                 wzName,
  _In_ const PROPVARIANT             *pvarValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*THIS \_ PTR* \[ en\]
</dt> <dd>

Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\***

Puntero a este [**objeto IWICMetadataQueryWriter.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)

</dd> <dt>

*wzName* \[ En\]
</dt> <dd>

Tipo: **LPCWSTR**

Nombre del elemento de metadatos.

</dd> <dt>

*pvarValue* \[ En\]
</dt> <dd>

Tipo: **const [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \***

Metadatos que se establecerán.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP con SP2, solo Windows de \[ escritorio de Vista\]<br/>                                                                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                                                                             |
| Archivo DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

