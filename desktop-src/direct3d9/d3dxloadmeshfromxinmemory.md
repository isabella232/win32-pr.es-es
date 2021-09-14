---
description: Carga una malla desde la memoria.
ms.assetid: bbaecc00-97ab-433c-b0c7-ac7837bfc3be
title: Función D3DXLoadMeshFromXInMemory (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 66b07a88a938b09217a2fee2b9eed272233edc75
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974345"
---
# <a name="d3dxloadmeshfromxinmemory-function"></a>Función D3DXLoadMeshFromXInMemory

Carga una malla desde la memoria.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXLoadMeshFromXInMemory(
  _In_  LPCVOID           Memory,
  _In_  DWORD             SizeOfMemory,
  _Out_ DWORD             Options,
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

*Memoria* \[ En\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntero al búfer de memoria que contiene los datos de malla.

</dd> <dt>

*SizeOfMemory* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Tamaño del archivo en memoria, en bytes.

</dd> <dt>

*Opciones* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de una o varias marcas de la [**enumeración D3DXMESH,**](./d3dxmesh.md) especificando opciones de creación para la malla.

</dd> <dt>

*pD3DDevice* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a una [**interfaz IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) el objeto de dispositivo asociado a la malla.

</dd> <dt>

*ppAdjacency* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Dirección de un puntero a una [**interfaz ID3DXBuffer.**](id3dxbuffer.md) Cuando el método devuelve un resultado, este parámetro se rellena con una matriz de tres DWORD por cara que especifican los tres vecinos para cada cara de la malla.

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

## <a name="remarks"></a>Observaciones

Todas las mallas del archivo se contraerán en una malla de salida. Si el archivo contiene una jerarquía de fotogramas, todas las transformaciones se aplicarán a la malla.

En el caso de los archivos de malla que no contienen información de instancia de efecto, las instancias de efecto predeterminadas se generarán a partir de la información de material del archivo .x. Una instancia de efecto predeterminada tendrá valores predeterminados que corresponden a los miembros de la [**estructura D3DMATERIAL9.**](d3dmaterial9.md)

El nombre de textura predeterminado también se rellena, pero se controla de forma diferente. El nombre será , que corresponde a una variable de efecto por el nombre Texture0@Name de "Texture0" con una anotación denominada "Name". Contendrá el nombre del archivo de cadena para la textura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md)
</dt> <dt>

[**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)
</dt> </dl>

 

 
