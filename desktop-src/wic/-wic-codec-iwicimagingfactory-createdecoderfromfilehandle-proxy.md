---
description: Función de proxy para el método CreateDecoderFromFileHandle.
ms.assetid: bc7f8a07-6d82-4d95-88ef-979d571758f4
title: IWICImagingFactory_CreateDecoderFromFileHandle_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromFileHandle_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 15c515bb17641e2e7b70b79552fe3bacf1f1c3fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002158"
---
# <a name="iwicimagingfactory_createdecoderfromfilehandle_proxy-function"></a>IWICImagingFactory \_ CreateDecoderFromFileHandle \_ función proxy

Función de proxy para el método [**CreateDecoderFromFileHandle**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICImagingFactory_CreateDecoderFromFileHandle_Proxy(
  _In_        IWICImagingFactory *pFactory,
  _In_        ULONG_PTR          hFile,
  _In_  const GUID               *pguidVendor,
  _In_        WICDecodeOptions   metadataOptions,
  _Out_       IWICBitmapDecoder  **ppIDecoder
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFactory* \[ de\]
</dt> <dd>

Tipo: **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _

</dd> <dt>

_hFile * \[ en\]
</dt> <dd>

Tipo: **ULong \_ ptr**

Identificador de archivo del que se va a crear el descodificador.

</dd> <dt>

*pguidVendor* \[ de\]
</dt> <dd>

Tipo: **const GUID \** _

GUID del proveedor para el descodificador.

</dd> <dt>

_metadataOptions * \[ en\]
</dt> <dd>

Tipo: **[ **WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**

[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) que se va a usar al crear el descodificador.

</dd> <dt>

*ppIDecoder* \[ enuncia\]
</dt> <dd>

Tipo: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***

Puntero que recibe un puntero a un nuevo [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).

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



 

 




