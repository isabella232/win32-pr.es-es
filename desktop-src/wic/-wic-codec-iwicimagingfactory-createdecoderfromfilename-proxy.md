---
description: Función de proxy para el método CreateDecoderFromFilename.
ms.assetid: 12c60899-0fe0-47d0-9026-48c74df328ef
title: IWICImagingFactory_CreateDecoderFromFilename_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromFilename_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: dabc24d17fdac881537d45e47a8cc6808a1cf805ac14025d7fdfcfa50eea8500
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056635"
---
# <a name="iwicimagingfactory_createdecoderfromfilename_proxy-function"></a>Función IWICImagingFactory \_ CreateDecoderFromFilename \_ Proxy

Función de proxy para [**el método CreateDecoderFromFilename.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICImagingFactory_CreateDecoderFromFilename_Proxy(
  _In_        IWICImagingFactory  *pFactory,
  _In_        LPCWSTR             wzFilename,
  _In_  const GUID                *pguidVendor,
  _In_        DWORD               dwDesiredAccess,
  _In_        WICDecodeOptions    metadataOptions,
  _Out_       IWICBitmapDecoder   **ppIDecoder
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFactory* \[ En\]
</dt> <dd>

Tipo: **IWICImagingFactory \***

</dd> <dt>

*wzFilename* \[ En\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntero a una cadena terminada en NULL que especifica el nombre de un objeto que se debe crear o abrir.

</dd> <dt>

*pguidVendor* \[ En\]
</dt> <dd>

Tipo: **\* GUID const**

GUID del proveedor para el descodificador.

</dd> <dt>

*dwDesiredAccess* \[ En\]
</dt> <dd>

Tipo: **DWORD**

Acceso al objeto , que se puede leer, escribir o ambos.

Para obtener más información, vea [Archivos de derechos de acceso y seguridad de \[ archivos. \] ](../fileio/file-security-and-access-rights.md)

</dd> <dt>

*metadataOptions* \[ En\]
</dt> <dd>

Tipo: **[ **WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**

[**WICDecodeOptions que**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) se usará al crear el descodificador.

</dd> <dt>

*ppIDecoder* \[ out\]
</dt> <dd>

Tipo: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***

Puntero que recibe un puntero al nuevo [**IWICBitmapDecoder.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)

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



 

