---
description: Crea una textura vacía, ajustando los parámetros de llamada según sea necesario.
ms.assetid: ea028aa9-4f37-4625-9e07-9072ec1a61d0
title: Función D3DXCreateTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ecbd5cbb94355af9c1e51e6c7e8fc31a862b03be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547915"
---
# <a name="d3dxcreatetexture-function"></a>D3DXCreateTexture función)

Crea una textura vacía, ajustando los parámetros de llamada según sea necesario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateTexture(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  UINT               Width,
  _In_  UINT               Height,
  _In_  UINT               MipLevels,
  _In_  DWORD              Usage,
  _In_  D3DFORMAT          Format,
  _In_  D3DPOOL            Pool,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura.

</dd> <dt>

*Ancho* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ancho en píxeles. Si este valor es 0, se utiliza un valor de 1. Vea la sección Comentarios.

</dd> <dt>

*Alto* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Alto en píxeles. Si este valor es 0, se utiliza un valor de 1. Vea la sección Comentarios.

</dd> <dt>

*MipLevels* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de niveles de MIP solicitados. Si este valor es cero o el valor predeterminado de D3DX \_ , se crea una cadena de mipmap completa.

</dd> <dt>

*Uso* \[ de de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

0, [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md)o **D3DUSAGE \_ Dynamic**. Al establecer esta marca en **D3DUSAGE \_ RENDERTARGET** , se indica que la superficie se va a usar como destino de representación llamando al método [**SetRenderTarget**](/windows/desktop/api) . Si se especifica **D3DUSAGE \_ RENDERTARGET** o **D3DUSAGE \_ Dynamic** , la aplicación debe comprobar que el dispositivo admite esta operación mediante una llamada a [**CheckDeviceFormat**](/windows/desktop/api). Para obtener más información sobre el uso de texturas dinámicas, vea [usar texturas dinámicas](performance-optimizations.md).

</dd> <dt>

*Formato* \[ de\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) , que describe el formato de píxel solicitado para la textura. La textura devuelta puede tener un formato diferente al especificado, si el dispositivo no admite el formato solicitado. Las aplicaciones deben comprobar el formato de la textura devuelta para ver si coincide con el formato solicitado.

</dd> <dt>

*Grupo* \[ de de\]
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

Miembro del tipo enumerado [**D3DPOOL**](./d3dpool.md) , que describe la clase de memoria en la que se debe colocar la textura.

</dd> <dt>

*ppTexture* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Dirección de un puntero a una interfaz [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa el objeto de textura creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Internamente, D3DXCreateTexture usa [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) para ajustar los parámetros de llamada. Por lo tanto, las llamadas a D3DXCreateTexture se realizarán con frecuencia cuando se produzca un error en las llamadas a [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) .

Si el alto y el ancho se establecen en el valor [ \_ predeterminado de D3DX](other-d3dx-constants.md), se usa un valor de 256 para ambos parámetros. Si el alto o el ancho se establece en \_ el valor predeterminado de D3DX y el otro parámetro se establece en un valor numérico, la textura será cuadrada con el alto y el ancho equivalentes al valor numérico.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
