---
title: Función D3DX11SaveTextureToFile (D3DX11tex. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Tenga en cuenta que, en lugar de usar esta función, se recomienda usar la biblioteca DirectXTex, CaptureTexture then SaveToXXXFile (donde XXX es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de fuente de arte común para juegos. Para el escenario simplificado de creación de una captura de pantalla a partir de una textura de destino de representación, se recomienda usar la biblioteca DirectXTK, SaveDDSTextureToFile o SaveWICTextureToFile. Guardar una textura en un archivo.
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
ms.openlocfilehash: 1d87188c3e58a8bea36b1cffb675c229aed71677
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986989"
---
# <a name="d3dx11savetexturetofile-function"></a>D3DX11SaveTextureToFile función)

> [!Note]  
> La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.

 

> [!Note]  
> En lugar de usar esta función, se recomienda usar la biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) , **CaptureTexture** then **SAVETOXXXFILE** (donde xxx es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de fuente de arte común para juegos. Para el escenario simplificado de creación de una captura de pantalla a partir de una textura de destino de representación, se recomienda usar la biblioteca [DirectXTK](https://github.com/Microsoft/DirectXTK) , **SaveDDSTextureToFile** o **SaveWICTextureToFile**.

 

Guardar una textura en un archivo.

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

Un puntero a un objeto [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .

</dd> <dt>

*pSrcTexture* \[ de\]
</dt> <dd>

Tipo: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***

Puntero a la textura que se va a guardar. Vea [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).

</dd> <dt>

*DestFormat* \[ de\]
</dt> <dd>

Tipo: **[ **\_ formato de \_ archivo \_ de imagen D3DX11**](d3dx11-image-file-format.md)**

El formato con el que se guardará la textura (consulte [**\_ formato de \_ archivo \_ de imagen D3DX11**](d3dx11-image-file-format.md)). D3DX11 \_ IFF \_ es el formato preferido, ya que es la única opción que admite todos los formatos en [**el \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

</dd> <dt>

*pDestFile* \[ de\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Nombre del archivo de salida de destino en el que se guardará la textura. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos se resuelve como LPCSTR.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md); Use el valor devuelto para ver si se admite *DestFormat* .

## <a name="remarks"></a>Observaciones

**D3DX11SaveTextureToFile** escribe la estructura del [**encabezado DDS adicional \_ \_ DXT10**](/windows/desktop/direct3ddds/dds-header-dxt10) para la textura de entrada solo si es necesario (por ejemplo, porque la textura de entrada está en formato RGB estándar (sRGB)). Si **D3DX11SaveTextureToFile** escribe la estructura **del \_ encabezado \_ DDS DXT10** , establece el miembro **DwFourCC** de la estructura [**de \_ PIXELFORMAT de DDS**](/windows/desktop/direct3ddds/dds-pixelformat) para la textura en **contenido DX10** para indicar el prescense del **encabezado \_ DDS \_ DXT10** encabezado extendido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

