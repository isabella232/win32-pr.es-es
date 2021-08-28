---
description: Guarde una textura en un archivo.
ms.assetid: c1718903-039a-4132-b128-82e03078ef62
title: Función D3DX10SaveTextureToFile (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SaveTextureToFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4d1adb4a490b047329277c4092a68563ffc4bf5d4bb1dbfd866bb849d9f561a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634565"
---
# <a name="d3dx10savetexturetofile-function"></a>Función D3DX10SaveTextureToFile

Guarde una textura en un archivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10SaveTextureToFile(
  _In_ ID3D10Resource           *pSrcTexture,
  _In_ D3DX10_IMAGE_FILE_FORMAT DestFormat,
  _In_ LPCTSTR                  pDestFile
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSrcTexture* \[ En\]
</dt> <dd>

Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

Puntero a la textura que se va a guardar. Vea [**ID3D10Resource (Interfaz).**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)

</dd> <dt>

*DestFormat* \[ En\]
</dt> <dd>

Tipo: FORMATO DE ARCHIVO DE **[ **\_ IMAGEN \_ \_ D3DX10**](d3dx10-image-file-format.md)**

El formato de la textura se guardará como (vea [**D3DX10 \_ IMAGE \_ FILE \_ FORMAT**](d3dx10-image-file-format.md)). D3DX10 IFF DDS es el formato preferido, ya que es la única opción que admite todos los formatos \_ \_ en [**DXGI \_ FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).

</dd> <dt>

*pDestFile* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Nombre del archivo de salida de destino donde se guardará la textura. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos se resuelve como LPCSTR.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10](d3d10-graphics-reference-returnvalues.md); use el valor devuelto para ver si se *admite DestFormat.*

## <a name="remarks"></a>Comentarios

**D3DX10SaveTextureToFile** escribe la estructura [**\_ \_ DDS HEADER DXT10**](../direct3ddds/dds-header-dxt10.md) adicional para la textura de entrada solo si es necesario (por ejemplo, porque la textura de entrada está en formato RGB estándar (sRGB). Si **D3DX10SaveTextureToFile** escribe la estructura **\_ \_ DXT10 de DDS HEADER,** establece el miembro **dwFourCC** de la estructura [**\_ PIXELFORMAT de DDS**](../direct3ddds/dds-pixelformat.md) para la textura en **DX10** para indicar la prescense del encabezado extendido **DDS \_ HEADER \_ DXT10.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de textura en D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[De uso general functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
