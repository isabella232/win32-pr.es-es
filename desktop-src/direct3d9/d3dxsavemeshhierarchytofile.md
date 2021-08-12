---
description: Crea un archivo .x y guarda en él la jerarquía de malla y las animaciones correspondientes.
ms.assetid: 803926fe-8cb7-422a-9920-56f7d0b0d0ea
title: Función D3DXSaveMeshHierarchyToFile (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveMeshHierarchyToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 892d27e305badc2cf1b21de41a1f9d37da13f36c1521135a79a65619e31903f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298533"
---
# <a name="d3dxsavemeshhierarchytofile-function"></a>Función D3DXSaveMeshHierarchyToFile

Crea un archivo .x y guarda en él la jerarquía de malla y las animaciones correspondientes.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXSaveMeshHierarchyToFile(
  _In_       LPCSTR                    pFilename,
  _In_       DWORD                     XFormat,
  _In_ const D3DXFRAME                 *pFrameRoot,
  _In_       LPD3DXANIMATIONCONTROLLER pAnimController,
  _In_       LPD3DXSAVEUSERDATA        pUserDataSaver
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFilename* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntero a una cadena que especifica el nombre del archivo .x que identifica la malla guardada. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve en LPCWSTR. De lo contrario, el tipo de datos de cadena se resuelve en LPCSTR. Vea la sección Comentarios.

</dd> <dt>

*XFormat* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Formato del archivo .x (texto o binario, comprimido o no). Consulte \_ FILEFORMAT D3DXF. D3DXF FILEFORMAT COMPRESSED se puede combinar (mediante un OR lógico) con las marcas FILEFORMAT BINARY o \_ \_ \_ \_ D3DXF FILEFORMAT TEXT de D3DXF \_ para reducir el tamaño del archivo de \_ salida.

</dd> <dt>

*pFrameRoot* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***

Nodo raíz de la jerarquía que se va a guardar. Vea [**D3DXFRAME.**](d3dxframe.md)

</dd> <dt>

*pAnimController* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**

Controlador de animación que tiene conjuntos de animaciones que se almacenarán. Vea [**ID3DXAnimationController.**](id3dxanimationcontroller.md)

</dd> <dt>

*pUserDataSaver* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXSAVEUSERDATA**](id3dxsaveuserdata.md)**

Interfaz proporcionada por la aplicación que permite guardar datos de usuario. Vea [**ID3DXSaveUserData**](id3dxsaveuserdata.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada de función se resuelve en D3DXSaveMeshHierarchyToFileW. De lo contrario, la llamada de función se resuelve en D3DXSaveMeshHierarchyToFileA.

Esta función no guarda conjuntos de animación comprimidos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de animación](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> <dt>

[Referencia de archivo X](dx9-graphics-reference-d3dx-x-file.md)
</dt> </dl>

 

 
