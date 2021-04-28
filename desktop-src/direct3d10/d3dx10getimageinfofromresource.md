---
description: 'Función D3DX10GetImageInfoFromResource: recupera información sobre una imagen determinada en un recurso.'
ms.assetid: d413d887-77e0-43cc-a30e-67c3c40772f0
title: Función D3DX10GetImageInfoFromResource (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetImageInfoFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 650d05f379be634bfdd9dfb0908153260f795b00
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098373"
---
# <a name="d3dx10getimageinfofromresource-function"></a>Función D3DX10GetImageInfoFromResource

Recupera información sobre una imagen determinada en un recurso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10GetImageInfoFromResource(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSrcModule* \[ En\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Módulo donde se carga el recurso. Establezca este parámetro en **NULL** para especificar el módulo asociado a la imagen que el sistema operativo usó para crear el proceso actual.

</dd> <dt>

*pSrcResource* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntero a una cadena que especifica el nombre de archivo. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos se resuelve como LPCSTR. Vea la sección Comentarios.

</dd> <dt>

*pPump* \[ En\]
</dt> <dd>

Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Bombeo de subprocesos opcional que se puede usar para cargar la información de forma asincrónica. Puede ser **NULL.** Vea [**ID3DX10ThreadPump.**](id3dx10threadpump.md)

</dd> <dt>

*pSrcInfo* \[ En\]
</dt> <dd>

Tipo: **[ **D3DX10 \_ IMAGE \_ INFO**](d3dx10-image-info.md)\***

Puntero a una estructura DE INFORMACIÓN DE IMAGEN D3DX10 que se va a rellenar con la descripción de \_ los datos del archivo de \_ origen.

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntero al valor devuelto. Puede ser **NULL.** Si *pPump* no es **NULL,** *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Comentarios

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada de función se resuelve en D3DX10GetImageInfoFromResourceW. De lo contrario, la llamada de función se resuelve en D3DX10GetImageInfoFromResourceA porque se usan cadenas ANSI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de textura en D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
