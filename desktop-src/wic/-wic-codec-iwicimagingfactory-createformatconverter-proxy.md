---
description: Función de proxy para el método CreateFormatConverter.
ms.assetid: 1013720a-d00e-4381-af5d-747806546692
title: IWICImagingFactory_CreateFormatConverter_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateFormatConverter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 91e0d87a57326e413e725e056bd5f44aff152934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278470"
---
# <a name="iwicimagingfactory_createformatconverter_proxy-function"></a>IWICImagingFactory \_ CreateFormatConverter \_ función proxy

Función de proxy para el método [**CreateFormatConverter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICImagingFactory_CreateFormatConverter_Proxy(
  _In_  IWICImagingFactory  *pFactory,
  _Out_ IWICFormatConverter **ppIFormatConverter
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFactory* \[ de\]
</dt> <dd>

Tipo: **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _

</dd> <dt>

_ppIFormatConverter * \[ out\]
</dt> <dd>

Tipo: **[ **IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\*\***

Puntero que recibe un puntero a un nuevo [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter).

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



 

 




