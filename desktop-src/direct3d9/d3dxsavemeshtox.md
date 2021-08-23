---
description: Guarda una malla en un archivo .x.
ms.assetid: 6d9cbca8-3847-4e15-95d4-9df3f8269665
title: Función D3DXSaveMeshToX (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveMeshToX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 668131237def6078d775d0002f624b035ad29e21b9a49399b673933dc63e5b5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988445"
---
# <a name="d3dxsavemeshtox-function"></a>Función D3DXSaveMeshToX

Guarda una malla en un archivo .x.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXSaveMeshToX(
  _In_       LPCTSTR            pFilename,
  _In_       LPD3DXMESH         pMesh,
  _In_ const DWORD              *pAdjacency,
  _In_ const D3DXMATERIAL       *pMaterials,
  _In_ const D3DXEFFECTINSTANCE *pEffectInstances,
  _In_       DWORD              NumMaterials,
  _In_       DWORD              Format
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFilename* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntero a una cadena que especifica el nombre de archivo. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve en LPCWSTR. De lo contrario, el tipo de datos de cadena se resuelve en LPCSTR. Vea la sección Comentarios.

</dd> <dt>

*pMesh* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero a una [**interfaz ID3DXMesh,**](id3dxmesh.md) que representa la malla que se guardará en un archivo .x.

</dd> <dt>

*pAdjacency* \[ En\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntero a una matriz de tres DWORD por cara que especifican los tres vecinos de cada cara de la malla. Este parámetro puede ser **NULL.**

</dd> <dt>

*pMaterials* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATERIAL**](d3dxmaterial.md) \***

Puntero a una matriz de [**estructuras D3DXMATERIAL,**](d3dxmaterial.md) que contiene información de material que se va a guardar en el archivo .x.

</dd> <dt>

*pEffectInstances* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md) \***

Puntero a una matriz de instancias de efecto, una por grupo de atributos en la malla. Este parámetro puede ser **NULL.** Una instancia de efecto es una instancia determinada de información de estado que se usa para inicializar un efecto. Para obtener más información, [**vea D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).

</dd> <dt>

*NumMaterials* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de [**estructuras D3DXMATERIAL**](d3dxmaterial.md) en la *matriz pMaterials.*

</dd> <dt>

*Formato* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de formato de archivo y opciones de guardado al guardar un archivo .x. Vea [D3DX X File Constants (Constantes de archivo D3DX X).](dx9-graphics-reference-d3dx-x-file-constants.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada a la función se resuelve en D3DXSaveMeshToXW. De lo contrario, la llamada de función se resuelve en D3DXSaveMeshToXA porque se usan cadenas ANSI.

El formato de archivo predeterminado es binario; sin embargo, si se especifica un archivo como un archivo binario y un archivo de texto, se guardará como un archivo de texto. Independientemente del formato de archivo, también puede usar el formato comprimido para reducir el tamaño del archivo.

A continuación se muestra un ejemplo de código típico de cómo usar esta función.


```
ID3DXMesh*    m_pMesh;           // Mesh object to be saved to a .x file
D3DXMATERIAL* m_pMaterials;      // Array of material structs in the mesh
DWORD         m_dwNumMaterials;  // Number of material structs in the mesh
    
DWORD dwFormat = D3DXF_FILEFORMAT_BINARY;  // Binary-format .x file (default)
// DWORD dwFormat = D3DXF_FILEFORMAT_TEXT; // Text-format .x file
    
// Load mesh into m_pMesh and determine values of m_pMaterials and 
// m_dwNumMaterials with calls to D3DXLoadMeshxxx or other D3DX functions
    
// ...
        
D3DXSaveMeshToX(
    L"outputxfilename.x",
    m_pMesh,
    NULL,
    m_pMaterials,
    NULL,
    m_dwNumMaterials,
    dwFormat );
```



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

 

 
