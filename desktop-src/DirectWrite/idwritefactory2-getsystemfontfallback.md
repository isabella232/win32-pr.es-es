---
title: IDWriteFactory2 GetSystemFontFallback, método
description: Crea un objeto de reserva de fuente a partir de la lista de reserva del sistema.
ms.assetid: 7F2BDB39-2CB4-4DB7-BBBA-74B0C07E7420
keywords:
- Método GetSystemFontFallback de escritura directa
- Método GetSystemFontFallback de escritura directa, interfaz IDWriteFactory2
- Interfaz IDWriteFactory2 Direct Write, método GetSystemFontFallback
topic_type:
- apiref
api_name:
- IDWriteFactory2.GetSystemFontFallback
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3f0eb73ee80dc3e6195267d25f6043225b8613ed
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421161"
---
# <a name="idwritefactory2getsystemfontfallback-method"></a>IDWriteFactory2:: GetSystemFontFallback (método)

Crea un objeto de reserva de fuente a partir de la lista de reserva del sistema.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSystemFontFallback(
  [out] IDWriteFontFallback **fontFallback
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fontFallback* \[ enuncia\]
</dt> <dd>

Tipo: **[ **IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)\*\***

Contiene una dirección de un puntero al objeto de reserva de fuente recién creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteFactory2**](idwritefactory2.md)
</dt> </dl>

 

 