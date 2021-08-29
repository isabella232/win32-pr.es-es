---
description: Carga una malla desde un recurso.
ms.assetid: 3cf253dc-4f3f-4949-ab24-8225667f95f2
title: Función D3DXLoadMeshFromXResource (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 903add3ab87e23f904e609b2d0fe076cef4e7990f62424f365307ba87e014e0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857005"
---
# <a name="d3dxloadmeshfromxresource-function"></a>Función D3DXLoadMeshFromXResource

Carga una malla desde un recurso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXLoadMeshFromXResource(
  _In_  HMODULE           Module,
  _In_  LPCSTR            Name,
  _In_  LPCSTR            Type,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pNumMaterials,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Módulo* \[ En\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Controle el módulo donde se encuentra el recurso o **NULL** para el módulo asociado a la imagen que el sistema operativo usó para crear el proceso actual. Vea Notas.

</dd> <dt>

*Nombre* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntero a una cadena que especifica el recurso desde el que se crea la malla. Vea Notas.

</dd> <dt>

*Tipo* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntero a una cadena que especifica el tipo de recurso. Vea Notas.

</dd> <dt>

*Opciones* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de una o varias marcas de la [**enumeración D3DXMESH**](./d3dxmesh.md) que especifican opciones de creación para la malla.

</dd> <dt>

*pD3DDevice* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a una [**interfaz IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) el objeto de dispositivo asociado a la malla.

</dd> <dt>

*ppAdjacency* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Dirección de un puntero a una [**interfaz ID3DXBuffer.**](id3dxbuffer.md) Cuando el método devuelve un resultado, este parámetro se rellena con una matriz de tres DWORD por cara que especifican los tres vecinos de cada cara de la malla.

</dd> <dt>

*ppMaterials* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Dirección de un puntero a una [**interfaz ID3DXBuffer.**](id3dxbuffer.md) Cuando este método devuelve un resultado, este parámetro se rellena con una matriz de estructuras [**D3DXMATERIAL,**](d3dxmaterial.md) que contiene información guardada en el archivo DirectX.

</dd> <dt>

*ppEffectInstances* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntero a un búfer que contiene una matriz de instancias de efecto, una por grupo de atributos en la malla devuelta. Una instancia de efecto es una instancia determinada de información de estado que se usa para inicializar un efecto. Vea [**D3DXEFFECTINSTANCE.**](d3dxeffectinstance.md) Para obtener más información sobre el acceso al búfer, [**vea ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*pNumMaterials* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero al número de estructuras [**D3DXMATERIAL**](d3dxmaterial.md) en la matriz *ppMaterials,* cuando se devuelve el método .

</dd> <dt>

*ppMesh* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Dirección de un puntero a una [**interfaz ID3DXMesh,**](id3dxmesh.md) que representa la malla cargada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

Consulte [**FindResource para**](/windows/win32/api/winbase/nf-winbase-findresourcea) obtener más información sobre los parámetros Module, Name y Type.

Todas las mallas del archivo se contraerán en una malla de salida. Si el archivo contiene una jerarquía de fotogramas, todas las transformaciones se aplicarán a la malla.

En el caso de los archivos de malla que no contienen información de instancia de efecto, las instancias de efecto predeterminadas se generarán a partir de la información de material del archivo .x. Una instancia de efecto predeterminada tendrá valores predeterminados que corresponden a los miembros de la [**estructura D3DMATERIAL9.**](d3dmaterial9.md)

El nombre de textura predeterminado también se rellena, pero se controla de forma diferente. El nombre será , que corresponde a una variable de efecto por el nombre Texture0@Name de "Texture0" con una anotación denominada "Name". Contendrá el nombre del archivo de cadena para la textura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md)
</dt> <dt>

[**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)
</dt> </dl>

 

 
