---
description: Crea una textura de volumen vacía, ajustando los parámetros de llamada según sea necesario.
ms.assetid: 8fc515cd-2fb3-40c7-8192-a41d93ac1e99
title: Función D3DXCreateVolumeTexture (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fa3e7b701649b07a9a6da9c0faeed6e0594d1c0e145126c533f87e06249fb8c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119285"
---
# <a name="d3dxcreatevolumetexture-function"></a>Función D3DXCreateVolumeTexture

Crea una textura de volumen vacía, ajustando los parámetros de llamada según sea necesario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateVolumeTexture(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  UINT                     Width,
  _In_  UINT                     Height,
  _In_  UINT                     Depth,
  _In_  UINT                     MipLevels,
  _In_  DWORD                    Usage,
  _In_  D3DFORMAT                Format,
  _In_  D3DPOOL                  Pool,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a una [**interfaz IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura del volumen.

</dd> <dt>

*Ancho* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Ancho en píxeles. Este valor debe ser distinto de cero. La dimensión máxima que admite un controlador (para el ancho, el alto y la profundidad) se puede encontrar en MaxVolumeExtent en [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

</dd> <dt>

*Alto* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Alto en píxeles. Este valor debe ser distinto de cero. La dimensión máxima que admite un controlador (para el ancho, el alto y la profundidad) se puede encontrar en MaxVolumeExtent en [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

</dd> <dt>

*Profundidad* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Profundidad en píxeles. Este valor debe ser distinto de cero. La dimensión máxima que admite un controlador (para el ancho, el alto y la profundidad) se puede encontrar en MaxVolumeExtent en [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

</dd> <dt>

*MipLevels* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de niveles de mip solicitados. Si este valor es cero o D3DX DEFAULT, se crea una \_ cadena de asignación mip completa.

</dd> <dt>

*Uso* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

0 o D3DUSAGE \_ DYNAMIC. Para obtener más información sobre el uso de texturas dinámicas, vea [Usar texturas dinámicas.](performance-optimizations.md)

</dd> <dt>

*Formato* \[ En\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Miembro del tipo [enumerado D3DFORMAT,](d3dformat.md) que describe el formato de píxel solicitado para la textura del volumen. La textura del volumen devuelta puede tener un formato diferente del especificado por Format. Las aplicaciones deben comprobar el formato de la textura del volumen devuelta.

</dd> <dt>

*Grupo* \[ En\]
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

Miembro del tipo [**enumerado D3DPOOL,**](./d3dpool.md) que describe la clase de memoria en la que se debe colocar la textura del volumen.

</dd> <dt>

*ppVolumeTexture* \[ out\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***

Dirección de un puntero a una [**interfaz IDirect3DVolumeTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) que representa el objeto de textura de volumen creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY .

## <a name="remarks"></a>Comentarios

Internamente, D3DXCreateVolumeTexture usa [**D3DXCheckVolumeTextureRequirements**](d3dxcheckvolumetexturerequirements.md) para ajustar los parámetros de llamada. Por lo tanto, las llamadas a D3DXCreateVolumeTexture a menudo se realizará correctamente, donde se producirá un error en las llamadas a [**CreateVolumeTexture.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
