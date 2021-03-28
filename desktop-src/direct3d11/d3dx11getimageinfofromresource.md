---
title: Función D3DX11GetImageInfoFromResource (D3DX11tex. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Tenga en cuenta que, en lugar de usar esta función, se recomienda usar funciones de recursos y, a continuación, usar la biblioteca DirectXTex (herramientas), LoadFromXXXMemory (donde XXX es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de fuente de arte común para juegos. Recupera información acerca de una imagen determinada en un recurso.
ms.assetid: e4752eb3-38d5-4922-b3c8-5fdcd0cc0610
keywords:
- Función D3DX11GetImageInfoFromResource Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 967a7b2c2ff03faefc12a48be18a4756e4ed3962
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987001"
---
# <a name="d3dx11getimageinfofromresource-function"></a>D3DX11GetImageInfoFromResource función)

> [!Note]  
> La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.

 

> [!Note]  
> En lugar de usar esta función, se recomienda usar funciones de [recursos](/windows/desktop/menurc/resources-functions)y, a continuación, usar la biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) (herramientas), **LOADFROMXXXMEMORY** (donde xxx es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de fuente de arte común para juegos.

 

Recupera información acerca de una imagen determinada en un recurso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX11GetImageInfoFromResource(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSrcModule* \[ de\]
</dt> <dd>

Tipo: **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**

Módulo en el que se carga el recurso. Establezca este parámetro en **null** para especificar el módulo asociado a la imagen que el sistema operativo usó para crear el proceso actual.

</dd> <dt>

*pSrcResource* \[ de\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Puntero a una cadena que especifica el nombre de archivo. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos se resuelve como LPCSTR. Vea la sección Comentarios.

</dd> <dt>

*pPump* \[ de\]
</dt> <dd>

Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Bombeo de subprocesos opcional que se puede usar para cargar la información de forma asincrónica. Puede ser **null**. Consulte la [**interfaz ID3DX11ThreadPump**](id3dx11threadpump.md).

</dd> <dt>

*pSrcInfo* \[ de\]
</dt> <dd>

Tipo: **[ **\_ \_ información de imagen de D3DX11**](d3dx11-image-info.md)\***

Puntero a una \_ estructura de \_ información de imagen D3DX11 que se va a rellenar con la descripción de los datos del archivo de código fuente.

</dd> <dt>

*pHResult* \[ enuncia\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntero al valor devuelto. Puede ser **null**. Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Observaciones

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada de función se resuelve como **D3DX11GetImageInfoFromResourceW**. De lo contrario, la llamada de función se resuelve como **D3DX11GetImageInfoFromResourceA** porque se usan cadenas ANSI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

