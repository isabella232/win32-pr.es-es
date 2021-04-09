---
description: Crea un objeto de fuente para un dispositivo y fuente.
ms.assetid: 3e65dfdc-9608-420c-9672-c38289d13ab1
title: Función D3DXCreateFont (D3dx9core. h)
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
ms.openlocfilehash: 488a400928ecc270612a307fbede971e02b43b25
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821279"
---
# <a name="d3dxcreatefont-function"></a>D3DXCreateFont función)

Crea un objeto de fuente para un dispositivo y fuente.

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

*pDevice* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , el dispositivo que se va a asociar al objeto de fuente.

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

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Juego de caracteres de la fuente.

</dd> <dt>

*OutputPrecision* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica el modo en que Windows debe intentar hacer coincidir los tamaños de fuente y las características deseadas con las fuentes reales. Use \_ solo TT \_ \_ PRECIS por ejemplo para asegurarse de que siempre obtiene una fuente TrueType.

</dd> <dt>

*Calidad* \[ de de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica el modo en que Windows debe coincidir con la fuente deseada con una fuente real. Solo se aplica a las fuentes de trama y no debe afectar a las fuentes TrueType.

</dd> <dt>

*PitchAndFamily* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Índice de paso y familia.

</dd> <dt>

*pFacename* \[ de\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Cadena que contiene el nombre del tipo de letra. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR. Vea la sección Comentarios.

</dd> <dt>

*ppFont* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXFONT**](id3dxfont.md)\***

Devuelve un puntero a una interfaz [**ID3DXFont**](id3dxfont.md) que representa el objeto de fuente creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

La creación de un objeto ID3DXFont requiere que el dispositivo admita el color de 32 bits.

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada de función se resuelve como D3DXCreateFontW. De lo contrario, la llamada de función se resuelve como D3DXCreateFontA porque se usan cadenas ANSI.

Si desea obtener más información sobre los parámetros de fuente, consulte [la fuente lógica](../gdi/creating-a-logical-font.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de De uso general](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
