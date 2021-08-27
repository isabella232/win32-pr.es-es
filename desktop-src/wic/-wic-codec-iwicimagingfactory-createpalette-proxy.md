---
description: Función de proxy para el método CreatePalette.
ms.assetid: c83b4239-ce6b-4a4c-ab70-df31dfcdd26c
title: IWICImagingFactory_CreatePalette_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreatePalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 23f970acdd6166547322714cdcf5cd5cd8c4d0875616f5bbe692a02d06f8a8fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056615"
---
# <a name="iwicimagingfactory_createpalette_proxy-function"></a>Función \_ CreatePalette Proxy de IWICImagingFactory \_

Función de proxy para [**el método CreatePalette.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createpalette)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICImagingFactory_CreatePalette_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICPalette        **ppIPalette
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFactory* \[ En\]
</dt> <dd>

Tipo: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\***

</dd> <dt>

*ppIPalette* \[ out\]
</dt> <dd>

Tipo: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\*\***

Puntero que recibe un puntero a una [**nueva IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP con SP2, solo Windows aplicaciones \[ de escritorio de Vista\]<br/>                                                                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                                                                             |
| Archivo DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




