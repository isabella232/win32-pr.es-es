---
description: Función de proxy para el método HasAlpha.
ms.assetid: 8af9f588-ac22-40c4-8973-9636951cc9e6
title: IWICPalette_HasAlpha_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_HasAlpha_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6f9398b2d570efb41048d88ddeeeb76d62f4ca37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002387"
---
# <a name="iwicpalette_hasalpha_proxy-function"></a>IWICPalette \_ HasAlpha \_ función proxy

Función de proxy para el método [**HasAlpha**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-hasalpha) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICPalette_HasAlpha_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _Out_ BOOL        *pfHasAlpha
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Este \_ PTR* \[ en\]
</dt> <dd>

Tipo: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _

Puntero a este objeto [_ *IWICPalette* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .

</dd> <dt>

*pfHasAlpha* \[ enuncia\]
</dt> <dd>

Tipo: **bool \** _

Puntero que recibe `TRUE` si la paleta contiene un color transparente; de lo contrario, `FALSE` .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: _ *HRESULT**

Si esta función se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]<br/>                                                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                                                                             |
| Archivo DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




