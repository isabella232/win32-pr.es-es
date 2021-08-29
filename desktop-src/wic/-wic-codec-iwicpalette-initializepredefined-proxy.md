---
description: Función de proxy para el método InitializePredefined.
ms.assetid: 78137d43-c32f-4d60-b289-2e2154cf4d1e
title: IWICPalette_InitializePredefined_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializePredefined_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4ae1113dfba184490347bb8e255a0751884fd36c81cb8bbe337af771cd01d2ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812195"
---
# <a name="iwicpalette_initializepredefined_proxy-function"></a>Función IWICPalette \_ InitializePredefined \_ Proxy

Función de proxy para el [**método InitializePredefined.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializepredefined)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICPalette_InitializePredefined_Proxy(
  _In_ IWICPalette          *THIS_PTR,
  _In_ WICBitmapPaletteType ePaletteType,
  _In_ BOOL                 fAddTransparentColor
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*THIS \_ PTR* \[ en\]
</dt> <dd>

Tipo: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***

Puntero a este [**objeto IWICPalette.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)

</dd> <dt>

*ePaletteType* \[ En\]
</dt> <dd>

Tipo: **[ **WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**

Tipo de paleta predefinido deseado.

</dd> <dt>

*fAddTransparentColor* \[ En\]
</dt> <dd>

Tipo: **BOOL**

Color tranparent opcional que se agregará a la paleta. Si no se necesita ningún color transparente, use 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP con SP2, solo Windows aplicaciones \[ de escritorio de Vista\]<br/>                                                                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                                                                             |
| Archivo DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




