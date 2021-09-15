---
description: Función de proxy para crear IWICImagingFactory.
ms.assetid: e4f575b0-878f-461e-92e7-9494e505ea6f
title: WICCreateImagingFactory_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateImagingFactory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Windowscodecs.lib
ms.openlocfilehash: 6717764d0c25d64f99ab5d864bd0e77a63b88330
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359619"
---
# <a name="wiccreateimagingfactory_proxy-function"></a>Función de proxy WICCreateImagingFactory \_

Función de proxy para crear [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT WICCreateImagingFactory_Proxy(
  _In_  UINT               SDKVersion,
  _Out_ IWICImagingFactory **ppIImagingFactory
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*SDKVersion* \[ En\]
</dt> <dd>

Tipo: **UINT**

</dd> <dt>

*ppIImagingFactory* \[ out\]
</dt> <dd>

Tipo: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\*\***

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Esta función es un asistente para crear un generador de WIC para la vinculación explícita de DLL, que era necesaria para Windows XP. En el uso normal, usaría [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) en su lugar (consulte generadores de clases de LA API de [WIC),](./-wic-api.md#class-factories)ya que siempre se incluye en todas las versiones más recientes de Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP con SP2, solo Windows \[ aplicaciones de escritorio de Vista\]<br/>                                                                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                                                                             |
| Archivo DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>windowscodecs.lib</dt> </dl> |



 

