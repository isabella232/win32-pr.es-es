---
description: Recupera información acerca de una imagen determinada en un recurso.
ms.assetid: 1f811b1e-f0bd-4f64-a4c9-caf899470940
title: Función D3DXGetImageInfoFromResource (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6875719123fe0b4dca4405570703b2587492975b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821079"
---
# <a name="d3dxgetimageinfofromresource-function"></a>D3DXGetImageInfoFromResource función)

Recupera información acerca de una imagen determinada en un recurso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXGetImageInfoFromResource(
  _In_ HMODULE        hSrcModule,
  _In_ LPCTSTR        pSrcFile,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSrcModule* \[ de\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Módulo en el que se carga el recurso. Establezca este parámetro en **null** para especificar el módulo asociado a la imagen que el sistema operativo usó para crear el proceso actual.

</dd> <dt>

*pSrcFile* \[ de\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntero a una cadena que especifica el nombre de archivo. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR. Vea la sección Comentarios.

</dd> <dt>

*pSrcInfo* \[ de\]
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***

Puntero a una estructura de [**\_ información D3DXIMAGE**](d3dximage-info.md) que se va a rellenar con la descripción de los datos del archivo de código fuente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Observaciones

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada de función se resuelve como D3DXGetImageInfoFromResourceW. De lo contrario, la llamada de función se resuelve como D3DXGetImageInfoFromResourceA porque se usan cadenas ANSI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXGetImageInfoFromFile**](d3dxgetimageinfofromfile.md)
</dt> <dt>

[**D3DXGetImageInfoFromFileInMemory**](d3dxgetimageinfofromfileinmemory.md)
</dt> </dl>

 

 
