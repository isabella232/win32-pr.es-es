---
title: IDWriteTextLayout DetermineMinWidth, método
description: Determina el ancho mínimo posible con el que se puede establecer el diseño sin interrumpir la emergencia entre los caracteres de palabras completas que se están produciendo.
ms.assetid: 8efa1471-1b74-46d4-ac6d-fb1839ce2e74
keywords:
- Método DetermineMinWidth de escritura directa
- Método DetermineMinWidth de escritura directa, interfaz IDWriteTextLayout
- Interfaz IDWriteTextLayout Direct Write, método DetermineMinWidth
topic_type:
- apiref
api_name:
- IDWriteTextLayout.DetermineMinWidth
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2525f770030b80f0e9c0d6df9e5ec88becbb394b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690602"
---
# <a name="idwritetextlayoutdetermineminwidth-method"></a>IDWriteTextLayout::D método etermineMinWidth

Determina el ancho mínimo posible con el que se puede establecer el diseño sin interrumpir la emergencia entre los caracteres de palabras completas que se están produciendo.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT DetermineMinWidth(
  [out] FLOAT *minWidth
) = 0;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*minWidth* \[ enuncia\]
</dt> <dd>

Tipo: **float \***

Ancho mínimo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Dwrite. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

