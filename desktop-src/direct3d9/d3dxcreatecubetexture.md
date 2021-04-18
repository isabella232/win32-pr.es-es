---
description: Crea una textura de cubo vacía, ajustando los parámetros de llamada según sea necesario.
ms.assetid: 96cf3fc1-9efc-4b97-a082-2956386145c7
title: Función D3DXCreateCubeTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8fa31945cea5e65cdf00eae512059308090bcbab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721540"
---
# <a name="d3dxcreatecubetexture-function"></a>D3DXCreateCubeTexture función)

Crea una textura de cubo vacía, ajustando los parámetros de llamada según sea necesario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateCubeTexture(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  UINT                   Size,
  _In_  UINT                   MipLevels,
  _In_  DWORD                  Usage,
  _In_  D3DFORMAT              Format,
  _In_  D3DPOOL                Pool,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura.

</dd> <dt>

*Tamaño* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ancho y alto de la textura del cubo, en píxeles. Por ejemplo, si la textura del cubo es un cubo de 8 píxeles por 8 píxeles, el valor de este parámetro debe ser 8.

</dd> <dt>

*MipLevels* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de niveles de MIP solicitados. Si este valor es cero o el valor predeterminado de D3DX \_ , se crea una cadena de mipmap completa.

</dd> <dt>

*Uso* \[ de de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

0, D3DUSAGE \_ RENDERTARGET o D3DUSAGE \_ Dynamic. Al establecer esta marca en D3DUSAGE \_ RENDERTARGET, se indica que la superficie se va a usar como destino de representación. Después, el recurso se puede pasar al parámetro *pNewRenderTarget* del método [**SetRenderTarget**](/windows/desktop/api) . Si \_ se especifica D3DUSAGE RENDERTARGET, la aplicación debe comprobar que el dispositivo admite esta operación llamando a [**CheckDeviceFormat**](/windows/desktop/api). Para obtener más información sobre el uso de texturas dinámicas, vea [usar texturas dinámicas](performance-optimizations.md).

</dd> <dt>

*Formato* \[ de\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) , que describe el formato de píxel solicitado para la textura del cubo. La textura del cubo devuelto puede tener un formato diferente al especificado por *Format*. Las aplicaciones deben comprobar el formato de la textura del cubo devuelta.

</dd> <dt>

*Grupo* \[ de de\]
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

Miembro del tipo enumerado [**D3DPOOL**](./d3dpool.md) , que describe la clase de memoria en la que se debe colocar la textura del cubo.

</dd> <dt>

*ppCubeTexture* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***

Dirección de un puntero a una interfaz [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) que representa el objeto de textura del cubo creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Las texturas del cubo se diferencian de otras superficies en que son colecciones de superficies.

Internamente, D3DXCreateCubeTexture usa [**D3DXCheckCubeTextureRequirements**](d3dxcheckcubetexturerequirements.md) para ajustar los parámetros de llamada. Por lo tanto, las llamadas a D3DXCreateCubeTexture se realizarán con frecuencia cuando se produzca un error en las llamadas a [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
