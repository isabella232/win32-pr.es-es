---
description: Función de proxy para el método CreateBitmapFromSource.
ms.assetid: 7d000377-1855-4971-b782-4c0bf7968c5f
title: IWICImagingFactory_CreateBitmapFromSource_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromSource_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a7f7be9ca9eaa8aa14dcaf3617face2dff2f52f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003156"
---
# <a name="iwicimagingfactory_createbitmapfromsource_proxy-function"></a>IWICImagingFactory \_ CreateBitmapFromSource \_ función proxy

Función de proxy para el método [**CreateBitmapFromSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromsource) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICImagingFactory_CreateBitmapFromSource_Proxy(
  _In_  IWICImagingFactory         *pFactory,
  _In_  IWICBitmapSource           *pIBitmapSource,
  _In_  WICBitmapCreateCacheOption option,
  _Out_ IWICBitmap                 **ppIBitmap
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFactory* \[ de\]
</dt> <dd>

Tipo: **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _

</dd> <dt>

_pIBitmapSource * \[ en\]
</dt> <dd>

Tipo: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _

[_ *IWICBitmapSource* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) del que se va a crear el mapa de bits.

</dd> <dt>

*opción* \[ de de\]
</dt> <dd>

Tipo: **[ **WICBitmapCreateCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**

Opciones de caché del nuevo mapa de bits.

</dd> <dt>

*ppIBitmap* \[ enuncia\]
</dt> <dd>

Tipo: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***

Puntero que recibe un puntero al nuevo mapa de bits.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si esta función se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]<br/>                                                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                                                                             |
| Archivo DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




