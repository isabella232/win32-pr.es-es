---
description: Crea una malla que contiene el texto especificado, utilizando la fuente asociada al contexto del dispositivo.
ms.assetid: 1c8b0dc6-51b8-45bf-b4c0-b67e3d128097
title: Función D3DXCreateText (D3dx9shape.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateText
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9db7cc6fa89f8f102cabccdebd14852a50f60576b6135ae52e4cc9fada494812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117732299"
---
# <a name="d3dxcreatetext-function"></a>Función D3DXCreateText

Crea una malla que contiene el texto especificado, utilizando la fuente asociada al contexto del dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateText(
  _In_  LPDIRECT3DDEVICE9   pDevice,
  _In_  HDC                 hDC,
  _In_  LPCTSTR             pText,
  _In_  FLOAT               Deviation,
  _In_  FLOAT               Extrusion,
  _Out_ LPD3DXMESH          *ppMesh,
  _Out_ LPD3DXBUFFER        *ppAdjacency,
  _Out_ LPGLYPHMETRICSFLOAT pGlyphMetrics
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero al dispositivo que creó la malla.

</dd> <dt>

*hDC* \[ En\]
</dt> <dd>

Tipo: **HDC**

Contexto del dispositivo, que contiene la fuente para la salida. La fuente seleccionada por el contexto del dispositivo debe ser una fuente TrueType.

</dd> <dt>

*pText* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntero a una cadena que especifica el texto que se generará. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve en LPCWSTR. De lo contrario, el tipo de datos de cadena se resuelve en LPCSTR. Vea la sección Comentarios.

</dd> <dt>

*Desviación* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Desviación máxima de los esquemas de fuente TrueType.

</dd> <dt>

*Extrusión* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Cantidad para extruir texto en la dirección Z negativa.

</dd> <dt>

*ppMesh* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Puntero a la malla devuelta.

</dd> <dt>

*ppAdjacency* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntero a un búfer que contiene información de adyacencia. Puede ser **NULL.**

</dd> <dt>

*pGlyphMetrics* \[ out\]
</dt> <dd>

Tipo: **[ **LPGLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat)**

Puntero a una matriz de [**estructuras GLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat) que contienen los datos de métricas del glifo. Cada elemento contiene información sobre la posición y la orientación del glifo correspondiente en la cadena. El número de elementos de la matriz debe ser igual al número de caracteres de la cadena. Tenga en cuenta que el origen de cada estructura no es relativo a toda la cadena, sino que es relativo a esa celda de caracteres. Para calcular todo el cuadro de límite, agregue el incremento de cada glifo mientras recorre la cadena. Si no le preocupa el tamaño del glifo, establezca este parámetro en **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada de función se resuelve en D3DXCreateTextW. De lo contrario, la llamada de función se resuelve en D3DXCreateTextA porque se usan cadenas ANSI.

Esta función crea una malla con la opción de creación D3DXMESH MANAGED y el formato flexible de vértice \_ flexible (FVF) [D3DFVF \_ XYZ \| D3DFVF \_ NORMAL.](d3dfvf.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9shape.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de dibujo de formas](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
