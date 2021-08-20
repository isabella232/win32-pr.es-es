---
description: Función de proxy para el método CreateComponentInfo.
ms.assetid: 7d3b791a-d65e-4b90-8050-373a949e6d9c
title: IWICImagingFactory_CreateComponentInfo_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateComponentInfo_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8391b7ce90e99d03e53951afa64a53de87f464e88a906444e0b379545c37fc31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118033648"
---
# <a name="iwicimagingfactory_createcomponentinfo_proxy-function"></a>Función IWICImagingFactory \_ CreateComponentInfo \_ Proxy

Función de proxy para [**el método CreateComponentInfo.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICImagingFactory_CreateComponentInfo_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _In_  REFCLSID           clsidComponent,
  _Out_ IWICComponentInfo  **ppIInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFactory* \[ En\]
</dt> <dd>

Tipo: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\***

</dd> <dt>

*clsidComponent* \[ En\]
</dt> <dd>

Tipo: **REFCLSID**

CLSID para el componente deseado.

</dd> <dt>

*ppIInfo* \[ out\]
</dt> <dd>

Tipo: **[ **IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\*\***

Puntero que recibe un puntero a un [**nuevo IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo).

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



 

 




