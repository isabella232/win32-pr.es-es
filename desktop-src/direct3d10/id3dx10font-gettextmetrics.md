---
description: Recupera las características de fuente.
ms.assetid: ef7e0d18-492b-476b-945a-bfc0232a939a
title: Método ID3DX10Font::GetTextMetrics (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetTextMetrics
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 97cbddc59dd84d0a5b83610212fe94e87a49757da0430d64cb420280c815d9cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047053"
---
# <a name="id3dx10fontgettextmetrics-method"></a>Método ID3DX10Font::GetTextMetrics

Recupera las características de fuente.

## <a name="syntax"></a>Sintaxis


```C++
BOOL GetTextMetrics(
  [in] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTextMetrics* \[ En\]
</dt> <dd>

Tipo: **TEXTMETRIC \***

Puntero a una [estructura TEXTMETRIC,](/previous-versions//ms534202(v=vs.85)) que contiene propiedades de fuente. Si se define Unicode, la función devuelve una estructura TEXTMETRICW. De lo contrario, la función devuelve una estructura TEXTMETRICA.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Es distinto de cero si la función se realiza correctamente; de lo contrario, es 0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
