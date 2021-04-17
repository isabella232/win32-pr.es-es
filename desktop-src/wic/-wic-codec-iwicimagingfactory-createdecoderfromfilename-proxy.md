---
description: Función de proxy para el método CreateDecoderFromFilename.
ms.assetid: 12c60899-0fe0-47d0-9026-48c74df328ef
title: IWICImagingFactory_CreateDecoderFromFilename_Proxy función)
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
ms.openlocfilehash: 3497d71475198d035a496909e65c47df6c5f8b8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697812"
---
# <a name="iwicimagingfactory_createdecoderfromfilename_proxy-function"></a>IWICImagingFactory \_ CreateDecoderFromFilename \_ función proxy

Función de proxy para el método [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) .

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

*pFactory* \[ de\]
</dt> <dd>

Tipo: **IWICImagingFactory \** _

</dd> <dt>

_wzFilename * \[ en\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntero a una cadena terminada en null que especifica el nombre de un objeto que se va a crear o abrir.

</dd> <dt>

*pguidVendor* \[ de\]
</dt> <dd>

Tipo: **const GUID \** _

GUID del proveedor para el descodificador.

</dd> <dt>

_dwDesiredAccess * \[ en\]
</dt> <dd>

Tipo: **DWORD**

El acceso al objeto, que puede ser de lectura, escritura o ambos.

Para obtener más información, consulte [File Security and Access \[ Rights \] files](../fileio/file-security-and-access-rights.md).

</dd> <dt>

*metadataOptions* \[ de\]
</dt> <dd>

Tipo: **[ **WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**

[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) que se va a usar al crear el descodificador.

</dd> <dt>

*ppIDecoder* \[ enuncia\]
</dt> <dd>

Tipo: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***

Puntero que recibe un puntero al nuevo [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).

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



 

