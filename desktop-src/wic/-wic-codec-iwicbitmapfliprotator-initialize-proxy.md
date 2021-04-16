---
description: Función de proxy para el método Initialize.
ms.assetid: 860e8092-054d-489e-8ca1-fec43a039eca
title: IWICBitmapFlipRotator_Initialize_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFlipRotator_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 82a1aa5648edd47d0b635a407adc001c25183b50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705535"
---
# <a name="iwicbitmapfliprotator_initialize_proxy-function"></a>IWICBitmapFlipRotator \_ inicializar \_ función de proxy

Función de proxy para el método [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICBitmapFlipRotator_Initialize_Proxy(
  _In_ IWICBitmapFlipRotator     *THIS_PTR,
  _In_ IWICBitmapSource          *pISource,
  _In_ WICBitmapTransformOptions options
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Este \_ PTR* \[ en\]
</dt> <dd>

Tipo: **[**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) \** _

Puntero a este objeto [_ *IWICBitmapFlipRotator* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) .

</dd> <dt>

*pISource* \[ de\]
</dt> <dd>

Tipo: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _

Origen del mapa de bits de entrada.

</dd> <dt>

_options * \[ en\]
</dt> <dd>

Tipo: **[ **WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**

[**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) que se va a voltear o girar la imagen.

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



 

 




