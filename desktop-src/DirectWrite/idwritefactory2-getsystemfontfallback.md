---
title: Método IDWriteFactory2 GetSystemFontFallback
description: Crea un objeto de reserva de fuentes a partir de la lista de reserva de fuentes del sistema.
ms.assetid: 7F2BDB39-2CB4-4DB7-BBBA-74B0C07E7420
keywords:
- GetSystemFontFallback method Direct Write
- Método GetSystemFontFallback Direct Write , interfaz IDWriteFactory2
- Método Direct Write de la interfaz IDWriteFactory2, GetSystemFontFallback
topic_type:
- apiref
api_name:
- IDWriteFactory2.GetSystemFontFallback
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4513c8ee7fb4e7a3796ec442d4d36bb663a0c8803bb6276a584edcfda306d588
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329455"
---
# <a name="idwritefactory2getsystemfontfallback-method"></a>Método IDWriteFactory2::GetSystemFontFallback

Crea un objeto de reserva de fuentes a partir de la lista de reserva de fuentes del sistema.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSystemFontFallback(
  [out] IDWriteFontFallback **fontFallback
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fontFallback* \[ out\]
</dt> <dd>

Tipo: **[ **IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)\*\***

Contiene una dirección de un puntero al objeto de reserva de fuente recién creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IDWriteFactory2**](idwritefactory2.md)
</dt> </dl>

 

 