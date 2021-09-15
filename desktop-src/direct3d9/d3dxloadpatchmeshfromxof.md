---
description: Carga una malla de revisión desde un objeto ID3DXFileData.
ms.assetid: 8054e33e-6bf8-4a56-9f66-30600732c84f
title: Función D3DXLoadPatchMeshFromXof (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPatchMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aa2e75e34927d0bb3c68445b994ee0911adb08f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465437"
---
# <a name="d3dxloadpatchmeshfromxof-function"></a>Función D3DXLoadPatchMeshFromXof

Carga una malla de revisión desde [**un objeto ID3DXFileData.**](id3dxfiledata.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXLoadPatchMeshFromXof(
  _In_  LPD3DXFILEDATA    pxofMesh,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ PDWORD            pNumMaterials,
  _Out_ LPD3DXPATCHMESH   *ppMesh
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pxofMesh* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**

Puntero a una [**interfaz ID3DXFileData,**](id3dxfiledata.md) que representa el objeto de datos de archivo que se cargará.

</dd> <dt>

*Opciones* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de una o varias [**marcas D3DXMESH,**](./d3dxmesh.md) especificando las opciones de creación para la malla.

</dd> <dt>

*pD3DDevice* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero al dispositivo desde el que se crea la malla.

</dd> <dt>

*ppMaterials* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Matriz de materiales contenidos en la malla. Cada material se indexa mediante una [**interfaz ID3DXBuffer.**](id3dxbuffer.md)

</dd> <dt>

*ppEffectInstances* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntero a un búfer que contiene una matriz de instancias de efecto, una por grupo de atributos en la malla devuelta. Una instancia de efecto es una instancia determinada de información de estado que se usa para inicializar un efecto. Vea [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md). Para obtener más información sobre el acceso al búfer, [**vea ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*pNumMaterials* \[ out\]
</dt> <dd>

Tipo: **PDWORD**

Puntero que contiene el número de materiales de la malla.

</dd> <dt>

*ppMesh* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***

Dirección de un puntero a una [**interfaz ID3DXPatchMesh,**](id3dxpatchmesh.md) que representa la malla cargada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Para los archivos de malla que no contienen información de instancia de efecto, las instancias de efecto predeterminadas se generarán a partir de la información de material del archivo .x. Una instancia de efecto predeterminada tendrá valores predeterminados que corresponden a los miembros de la [**estructura D3DMATERIAL9.**](d3dmaterial9.md)

El nombre de textura predeterminado también se rellena, pero se controla de forma diferente. El nombre será , que corresponde a una variable de efecto por el nombre Texture0@Name de "Texture0" con una anotación denominada "Name". Contendrá el nombre de archivo de cadena para la textura.

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

 

 
