---
title: Método IdWriteTextLayout DetermineMinWidth
description: Determina el ancho mínimo posible en el que se puede establecer el diseño sin que se produzca una separación de emergencia entre los caracteres de palabras enteras.
ms.assetid: 8efa1471-1b74-46d4-ac6d-fb1839ce2e74
keywords:
- Escritura directa del método DetermineMinWidth
- Método DetermineMinWidth Direct Write , interfaz IDWriteTextLayout
- Método Direct Write de la interfaz IDWriteTextLayout , DetermineMinWidth
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
ms.openlocfilehash: 41123f2a5d584341c344248d0af936f34fc04e49c9aabc1cb73ecea0eacc84ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075535"
---
# <a name="idwritetextlayoutdetermineminwidth-method"></a>Método IDWriteTextLayout::D etermineMinWidth

Determina el ancho mínimo posible en el que se puede establecer el diseño sin que se produzca una separación de emergencia entre los caracteres de palabras enteras.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT DetermineMinWidth(
  [out] FLOAT *minWidth
) = 0;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*minWidth* \[ out\]
</dt> <dd>

Tipo: **\* FLOAT**

Ancho mínimo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

