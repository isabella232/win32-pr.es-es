---
description: Recupera las características de fuente que se identifican en una estructura TEXTMETRIC. Este método admite la configuración del compilador ANSI y Unicode.
ms.assetid: 37788281-5bb0-45bb-b6d4-bdc4d811e3af
title: Método ID3DXFont::GetTextMetrics (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetTextMetrics
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ce6064804d2aac2846cbea6971f145fc07759f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060606"
---
# <a name="id3dxfontgettextmetrics-method"></a>Método ID3DXFont::GetTextMetrics

Recupera las características de fuente que se identifican en una [**estructura TEXTMETRIC.**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) Este método admite la configuración del compilador ANSI y Unicode.

## <a name="syntax"></a>Sintaxis


```C++
BOOL GetTextMetrics(
  [out] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTextMetrics* \[ out\]
</dt> <dd>

Tipo: **[ **TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)\***

Puntero a una [**estructura TEXTMETRIC,**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) que contiene propiedades de fuente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Es distinto de cero si la función se realiza correctamente; de lo contrario, es 0.

## <a name="remarks"></a>Observaciones

La configuración del compilador también determina el tipo de estructura. Si se define Unicode, la función devuelve una estructura TEXTMETRICW. De lo contrario, la llamada a la función devuelve una estructura TEXTMETRICA.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
