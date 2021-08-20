---
title: Función D3DX11SaveTextureToFile (D3DX11tex.h)
description: Nota La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store. Nota En lugar de usar esta función, se recomienda usar la biblioteca DirectXTex, CaptureTexture y SaveToXXXFile (donde XXX es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admite TGA como un formato de origen de arte común para juegos). Para el escenario simplificado de creación de una captura de pantalla a partir de una textura de destino de representación, se recomienda usar la biblioteca DirectXTK, SaveDDSTextureToFile o SaveWICTextureToFile. Guarde una textura en un archivo.
ms.assetid: da161268-fb68-42dd-ba31-b090a993f369
keywords:
- Función D3DX11SaveTextureToFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SaveTextureToFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e74f73eaad167c7c813a8effe93b65ea7558514ae78ecc00926b420014f4a37a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118099267"
---
# <a name="d3dx11savetexturetofile-function"></a>Función D3DX11SaveTextureToFile

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.

 

> [!Note]  
> En lugar de usar esta función, se recomienda usar la biblioteca [DirectXTex,](https://github.com/Microsoft/DirectXTex) **CaptureTexture** y **SaveToXXXFile** (donde XXX es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admite TGA como un formato de origen de arte común para juegos). Para el escenario simplificado de creación de una captura de pantalla a partir de una textura de destino de representación, se recomienda usar la biblioteca [DirectXTK,](https://github.com/Microsoft/DirectXTK) **SaveDDSTextureToFile** o **SaveWICTextureToFile**.

 

Guarde una textura en un archivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX11SaveTextureToFile(
       ID3D11DeviceContext      *pContext,
  _In_ ID3D11Resource           *pSrcTexture,
  _In_ D3DX11_IMAGE_FILE_FORMAT DestFormat,
  _In_ LPCTSTR                  pDestFile
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pContext* 
</dt> <dd>

Tipo: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Puntero a un [**objeto ID3D11DeviceContext.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)

</dd> <dt>

*pSrcTexture* \[ En\]
</dt> <dd>

Tipo: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***

Puntero a la textura que se va a guardar. Vea [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).

</dd> <dt>

*DestFormat* \[ En\]
</dt> <dd>

Tipo: FORMATO DE ARCHIVO DE **[ **\_ IMAGEN \_ \_ D3DX11**](d3dx11-image-file-format.md)**

El formato de la textura se guardará como (vea [**D3DX11 \_ IMAGE \_ FILE \_ FORMAT**](d3dx11-image-file-format.md)). D3DX11 IFF DDS es el formato preferido, ya que es la única opción que admite todos los formatos \_ \_ en [**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

</dd> <dt>

*pDestFile* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Nombre del archivo de salida de destino donde se guardará la textura. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos se resuelve como LPCSTR.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 11](d3d11-graphics-reference-returnvalues.md); use el valor devuelto para ver si se *admite DestFormat.*

## <a name="remarks"></a>Comentarios

**D3DX11SaveTextureToFile** escribe la estructura [**\_ \_ DDS HEADER DXT10**](/windows/desktop/direct3ddds/dds-header-dxt10) adicional para la textura de entrada solo si es necesario (por ejemplo, porque la textura de entrada está en formato RGB estándar (sRGB). Si **D3DX11SaveTextureToFile** escribe la estructura **\_ \_ DXT10 de DDS HEADER,** establece el miembro **dwFourCC** de la estructura [**\_ PIXELFORMAT de DDS**](/windows/desktop/direct3ddds/dds-pixelformat) para la textura en **DX10** para indicar el prescense del encabezado extendido **\_ \_ DDS HEADER DXT10.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX11tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11.lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

