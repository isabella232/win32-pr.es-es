---
description: Recupera las características de la fuente.
ms.assetid: ef7e0d18-492b-476b-945a-bfc0232a939a
title: 'ID3DX10Font:: GetTextMetrics (método) (D3DX10. h)'
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
ms.openlocfilehash: 72decdcf0a9573f7ad8ba0f4e363df6df3599477
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547942"
---
# <a name="id3dx10fontgettextmetrics-method"></a>ID3DX10Font:: GetTextMetrics (método)

Recupera las características de la fuente.

## <a name="syntax"></a>Sintaxis


```C++
BOOL GetTextMetrics(
  [in] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTextMetrics* \[ de\]
</dt> <dd>

Tipo: **TEXTMETRIC \***

Puntero a una estructura [TEXTMETRIC](/previous-versions//ms534202(v=vs.85)) , que contiene las propiedades de fuente. Si se define Unicode, la función devuelve una estructura TEXTMETRICW. De lo contrario, la función devuelve una estructura TEXTMETRICA.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Es distinto de cero si la función se realiza correctamente; de lo contrario, es 0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[Interfaces de D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
