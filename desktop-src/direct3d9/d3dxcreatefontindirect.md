---
description: Crea un objeto de fuente indirectamente para un dispositivo y una fuente.
ms.assetid: 480f3012-8495-47ca-a649-11ce53cee06c
title: Función D3DXCreateFontIndirect (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateFontIndirect
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 086f9cb4cff7666fc3977551e2c9fd4a61150d46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362691"
---
# <a name="d3dxcreatefontindirect-function"></a>D3DXCreateFontIndirect función)

Crea un objeto de fuente indirectamente para un dispositivo y una fuente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateFontIndirect(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_  const D3DXFONT_DESC     *pDesc,
  _Out_       LPD3DXFONT        *ppFont
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , el dispositivo que se va a asociar al objeto de fuente.

</dd> <dt>

*pDesc* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXFONT \_ DESC**](d3dxfont-desc.md) \***

Puntero a una [**estructura \_ DESC de D3DXFONT**](d3dxfont-desc.md) , que describe los atributos del objeto de fuente que se va a crear. Si la configuración del compilador requiere Unicode, el tipo de datos D3DXFONT \_ desc se resuelve como D3DXFONT \_ DESCW; de lo contrario, el tipo de datos se resuelve como D3DXFONT \_ Desca. Vea la sección Comentarios.

</dd> <dt>

*ppFont* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXFONT**](id3dxfont.md)\***

Devuelve un puntero a una interfaz [**ID3DXFont**](id3dxfont.md) que representa el objeto de fuente creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada de función se resuelve como D3DXCreateFontIndirectW. De lo contrario, la llamada de función se resuelve como D3DXCreateFontIndirectA porque se usan cadenas ANSI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de De uso general](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
