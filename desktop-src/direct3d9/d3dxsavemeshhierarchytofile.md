---
description: Crea un archivo. x y guarda la jerarquía de malla y sus animaciones correspondientes.
ms.assetid: 803926fe-8cb7-422a-9920-56f7d0b0d0ea
title: Función D3DXSaveMeshHierarchyToFile (D3dx9anim. h)
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
ms.openlocfilehash: f2de65f9bc2f9e40a5bc07c6f0b4d00112f0df21
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698230"
---
# <a name="d3dxsavemeshhierarchytofile-function"></a>D3DXSaveMeshHierarchyToFile función)

Crea un archivo. x y guarda la jerarquía de malla y sus animaciones correspondientes.

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

*pFilename* \[ de\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntero a una cadena que especifica el nombre del archivo. x que identifica la malla guardada. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR. Vea la sección Comentarios.

</dd> <dt>

*XFormat* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Formato del archivo. x (texto o binario, comprimido o no). Consulte D3DXF \_ FILEFORMAT. D3DXF \_ fileformat \_ Compressed se puede combinar (mediante un OR lógico) con las \_ marcas de texto D3DXF FILEFORMAT \_ binary o D3DXF \_ fileformat \_ para reducir el tamaño del archivo de salida.

</dd> <dt>

*pFrameRoot* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***

Nodo raíz de la jerarquía que se va a guardar. Vea [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*pAnimController* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**

Controlador de animación que tiene conjuntos de animaciones que se van a almacenar. Vea [**ID3DXAnimationController**](id3dxanimationcontroller.md).

</dd> <dt>

*pUserDataSaver* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXSAVEUSERDATA**](id3dxsaveuserdata.md)**

Interfaz proporcionada por la aplicación que permite guardar datos de usuario. Vea [**ID3DXSaveUserData**](id3dxsaveuserdata.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada de función se resuelve como D3DXSaveMeshHierarchyToFileW. De lo contrario, la llamada de función se resuelve como D3DXSaveMeshHierarchyToFileA.

Esta función no guarda los conjuntos de animaciones comprimidos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de animación](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> <dt>

[Referencia de archivo X](dx9-graphics-reference-d3dx-x-file.md)
</dt> </dl>

 

 
