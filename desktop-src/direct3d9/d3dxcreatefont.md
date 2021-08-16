---
description: Crea un objeto de fuente para un dispositivo y una fuente.
ms.assetid: 3e65dfdc-9608-420c-9672-c38289d13ab1
title: Función D3DXCreateFont (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateFont
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d9bac71e89657f4df176a1ee15e2dca0cda6e4a25b8c47560adc5cf26c982383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118526159"
---
# <a name="d3dxcreatefont-function"></a>Función D3DXCreateFont

Crea un objeto de fuente para un dispositivo y una fuente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateFont(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  INT               Height,
  _In_  UINT              Width,
  _In_  UINT              Weight,
  _In_  UINT              MipLevels,
  _In_  BOOL              Italic,
  _In_  DWORD             CharSet,
  _In_  DWORD             OutputPrecision,
  _In_  DWORD             Quality,
  _In_  DWORD             PitchAndFamily,
  _In_  LPCTSTR           pFacename,
  _Out_ LPD3DXFONT        *ppFont
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a una [**interfaz IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) el dispositivo que se va a asociar al objeto de fuente.

</dd> <dt>

*Alto* \[ En\]
</dt> <dd>

Tipo: **[ **INT**](../winprog/windows-data-types.md)**

Alto de los caracteres en unidades lógicas.

</dd> <dt>

*Ancho* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Ancho de los caracteres de las unidades lógicas.

</dd> <dt>

*Peso* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Grosor del tipo de letra. Un ejemplo es negrita.

</dd> <dt>

*MipLevels* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de niveles de mapa mip.

</dd> <dt>

*Cursiva* \[ En\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

True para la fuente cursiva; en caso contrario, false.

</dd> <dt>

*CharSet* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Juego de caracteres de la fuente.

</dd> <dt>

*OutputPrecision* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica cómo Windows debe intentar hacer coincidir los tamaños de fuente y las características deseados con las fuentes reales. Use OUT \_ TT ONLY PRECIS por ejemplo, para asegurarse de que \_ siempre obtiene una fuente \_ TrueType.

</dd> <dt>

*Calidad* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica cómo debe Windows la fuente deseada con una fuente real. Solo se aplica a las fuentes de trama y no debe afectar a las fuentes TrueType.

</dd> <dt>

*PitchAndFamily* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Índice de inclinación y familia.

</dd> <dt>

*pFacename* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Cadena que contiene el nombre del tipo de letra. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos de cadena se resuelve en LPCSTR. Vea la sección Comentarios.

</dd> <dt>

*ppFont* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXFONT**](id3dxfont.md)\***

Devuelve un puntero a una [**interfaz ID3DXFont,**](id3dxfont.md) que representa el objeto de fuente creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

La creación de un objeto ID3DXFont requiere que el dispositivo admita un color de 32 bits.

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada a la función se resuelve en D3DXCreateFontW. De lo contrario, la llamada de función se resuelve en D3DXCreateFontA porque se usan cadenas ANSI.

Si desea obtener más información sobre los parámetros de fuente, vea [Fuente lógica](../gdi/creating-a-logical-font.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[De uso general functions](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
