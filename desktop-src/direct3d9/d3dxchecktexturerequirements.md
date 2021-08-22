---
description: Comprueba los parámetros de creación de texturas.
ms.assetid: f8e788f3-02a9-4ee7-b74d-9e781a2fb39f
title: Función D3DXCheckTextureRequirements (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4c7166f981c0351054a2a6c359127a4ce1959b45a6e71c44db9e2546825bc5f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496105"
---
# <a name="d3dxchecktexturerequirements-function"></a>Función D3DXCheckTextureRequirements

Comprueba los parámetros de creación de texturas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCheckTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pWidth,
  _Inout_ UINT              *pHeight,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a una [**interfaz IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura.

</dd> <dt>

*pWidth* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Puntero al ancho solicitado en píxeles o **NULL.** Devuelve el tamaño corregido.

</dd> <dt>

*pHeight* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Puntero al alto solicitado en píxeles o **NULL.** Devuelve el tamaño corregido.

</dd> <dt>

*pNumMipLevels* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Puntero al número de niveles de asignación mip solicitados o **NULL.** Devuelve el número corregido de niveles de mapa mip.

</dd> <dt>

*Uso* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

0 o [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md). Establecer esta marca en D3DUSAGE RENDERTARGET indica que la superficie se \_ va a usar como destino de representación. A continuación, el recurso se puede pasar al parámetro pNewRenderTarget del [**método SetRenderTarget.**](/windows/desktop/api) Si **se especifica D3DUSAGE \_ RENDERTARGET,** la aplicación debe comprobar que el dispositivo admite esta operación llamando a [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).

</dd> <dt>

*pFormat* \[ in, out\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)\***

Puntero a un miembro del [tipo enumerado D3DFORMAT.](d3dformat.md) Especifica el formato de píxel deseado o **NULL.** Devuelve el formato corregido.

</dd> <dt>

*Grupo* \[ En\]
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

Miembro del [**tipo enumerado D3DPOOL,**](./d3dpool.md) que describe la clase de memoria en la que se debe colocar la textura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE.

## <a name="remarks"></a>Comentarios

Si los parámetros de esta función no son válidos, esta función devuelve los parámetros corregidos.

Esta función usa la heurística siguiente al comparar los requisitos solicitados con los formatos disponibles:

-   No elija un formato que tenga menos canales.
-   Evite [los formatos FOURCC](d3dformat.md) y de 24 bits a menos que se soliciten explícitamente.
-   Intente no agregar nuevos canales.
-   Intente no cambiar el número de bits por canal.
-   Intente evitar la conversión entre tipos de formatos. Por ejemplo, evite convertir un formato ARGB a un formato de profundidad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
