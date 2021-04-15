---
description: Crea un objeto de fuente para un dispositivo y fuente. Tenga en cuenta que, en lugar de usar esta función, se recomienda usar DirectWrite y la biblioteca DirectXTK, SpriteFont Class.
ms.assetid: a0dd02f1-c512-46d3-9e83-a785ac3ad7ee
title: Función D3DX10CreateFont (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateFont
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d6e5966e50c9c997085d35854868a2a7dd0455c7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707944"
---
# <a name="d3dx10createfont-function"></a>D3DX10CreateFont función)

Crea un objeto de fuente para un dispositivo y fuente.

> [!Note]  
> En lugar de usar esta función, se recomienda usar [DirectWrite](../directwrite/direct-write-portal.md) y la biblioteca [DirectXTK](https://github.com/Microsoft/DirectXTK) , **SpriteFont** Class.

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10CreateFont(
  _In_  ID3D10Device *pDevice,
  _In_  INT          Height,
  _In_  UINT         Width,
  _In_  UINT         Weight,
  _In_  UINT         MipLevels,
  _In_  BOOL         Italic,
  _In_  UINT         CharSet,
  _In_  UINT         OutputPrecision,
  _In_  UINT         Quality,
  _In_  UINT         PitchAndFamily,
  _In_  LPCTSTR      pFaceName,
  _Out_ LPD3DX10FONT *ppFont
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ de\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Puntero a una interfaz ID3D10Device, el dispositivo que se va a asociar al objeto de fuente.

</dd> <dt>

*Alto* \[ de de\]
</dt> <dd>

Tipo: **[ **int**](../winprog/windows-data-types.md)**

Alto de los caracteres en unidades lógicas.

</dd> <dt>

*Ancho* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ancho de los caracteres de las unidades lógicas.

</dd> <dt>

*Peso* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Peso del tipo de letra. Un ejemplo está en negrita.

</dd> <dt>

*MipLevels* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de niveles de mipmap.

</dd> <dt>

*Cursiva* \[ de\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

True para la fuente cursiva; de lo contrario, false.

</dd> <dt>

*Juego de caracteres* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Juego de caracteres de la fuente.

</dd> <dt>

*OutputPrecision* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Especifica el modo en que Windows debe intentar hacer coincidir los tamaños de fuente y las características deseadas con las fuentes reales. Use \_ solo TT \_ \_ PRECIS por ejemplo para asegurarse de que siempre obtiene una fuente TrueType.

</dd> <dt>

*Calidad* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Especifica el modo en que Windows debe coincidir con la fuente deseada con una fuente real. Solo se aplica a las fuentes de trama y no debe afectar a las fuentes TrueType.

</dd> <dt>

*PitchAndFamily* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice de paso y familia.

</dd> <dt>

*pFaceName* \[ de\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Cadena que contiene el nombre del tipo de letra. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos se resuelve como LPCSTR. Vea la sección Comentarios.

</dd> <dt>

*ppFont* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DX10FONT**](id3dx10font.md)\***

Devuelve un puntero a una interfaz ID3DX10Font que representa el objeto de fuente creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada de función se resuelve como D3DXCreateFontW. De lo contrario, la llamada de función se resuelve como D3DXCreateFontA porque se usan cadenas ANSI.

Si desea obtener más información sobre los parámetros de fuente, consulte [la fuente lógica](/previous-versions//ms533985(v=vs.85)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de De uso general](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
