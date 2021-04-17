---
description: Función de proxy para el método SetPalette.
ms.assetid: d8e2c36e-6886-4959-b2a2-469bebfe1cdc
title: IWICBitmapEncoder_SetPalette_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_SetPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 128953cd56c3bea17ec9761a2acf2b8bc89cacfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541262"
---
# <a name="iwicbitmapencoder_setpalette_proxy-function"></a>IWICBitmapEncoder \_ SetPalette \_ función proxy

Función de proxy para el método [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICBitmapEncoder_SetPalette_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR,
  _In_ IWICPalette       *pIPalette
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Este \_ PTR* \[ en\]
</dt> <dd>

Tipo: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _

Puntero a este objeto [_ *IWICBitmapEncoder* *](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .

</dd> <dt>

*pIPalette* \[ de\]
</dt> <dd>

Tipo: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _

[_ *IWICPalette* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) que se va a usar como paleta global.

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



 

 




