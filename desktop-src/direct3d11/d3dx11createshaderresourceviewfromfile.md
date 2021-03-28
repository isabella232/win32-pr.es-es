---
title: Función D3DX11CreateShaderResourceViewFromFile (D3DX11tex. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Tenga en cuenta que, en lugar de usar esta función, se recomienda usar esta biblioteca DirectXTK (Runtime), CreateXXXTextureFromFile (donde XXX es DDS o WIC) DirectXTex Library (Tools), LoadFromXXXFile (donde XXX es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de código fuente común para juegos) y CreateShaderResourceView crear una vista de recursos de sombreador a partir de un archivo.
ms.assetid: c6a23503-f511-49dc-a0dc-19932cf8f313
keywords:
- Función D3DX11CreateShaderResourceViewFromFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateShaderResourceViewFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05e7d710b0b379f3027591c2ff9e52c2fdd0d7a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362669"
---
# <a name="d3dx11createshaderresourceviewfromfile-function"></a>D3DX11CreateShaderResourceViewFromFile función)

> [!Note]  
> La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.

 

> [!Note]  
> En lugar de usar esta función, se recomienda usar estas:
>
> -   Biblioteca [DirectXTK](https://github.com/Microsoft/DirectXTK) (Runtime), **CREATEXXXTEXTUREFROMFILE** (donde xxx es DDS o WIC)
> -   Biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) (herramientas), **LOADFROMXXXFILE** (donde xxx es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de fuente de arte común para juegos) y luego **CreateShaderResourceView**

 

Cree una vista de recursos del sombreador a partir de un archivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX11CreateShaderResourceViewFromFile(
  _In_  ID3D11Device             *pDevice,
  _In_  LPCTSTR                  pSrcFile,
  _In_  D3DX11_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX11ThreadPump        *pPump,
  _Out_ ID3D11ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ de\]
</dt> <dd>

Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***

Un puntero al dispositivo (vea [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) que usará el recurso.

</dd> <dt>

*pSrcFile* \[ de\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Nombre del archivo que contiene la vista de recursos del sombreador. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos se resuelve como LPCSTR.

</dd> <dt>

*pLoadInfo* \[ de\]
</dt> <dd>

Tipo: **[ **\_ información de \_ carga \_ de imagen de D3DX11**](d3dx11-image-load-info.md)\***

Opcional. Identifica las características de una textura (consulte [**\_ información de \_ carga \_ de imagen de D3DX11**](d3dx11-image-load-info.md)) cuando se crea el procesador de datos; establezca este valor en **null** para leer las características de una textura cuando se carga la textura.

</dd> <dt>

*pPump* \[ de\]
</dt> <dd>

Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Puntero a una interfaz de bombeo de subprocesos (consulte la [**interfaz ID3DX11ThreadPump**](id3dx11threadpump.md)). Si se especifica **null** , esta función se comportará de forma sincrónica y no volverá hasta que finalice.

</dd> <dt>

*ppShaderResourceView* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***

Dirección de un puntero a la vista de recursos del sombreador (vea [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)).

</dd> <dt>

*pHResult* \[ enuncia\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntero al valor devuelto. Puede ser **null**. Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

Para obtener una lista de formatos de imagen compatibles, consulte [**\_ formato de \_ archivo \_ de imagen D3DX11**](d3dx11-image-file-format.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

