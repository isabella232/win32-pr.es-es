---
description: Guardar una textura en un archivo.
ms.assetid: c1718903-039a-4132-b128-82e03078ef62
title: Función D3DX10SaveTextureToFile (D3DX10Tex. h)
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
ms.openlocfilehash: c760876160d8ce1cbc0423639a59218c79716481
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698450"
---
# <a name="d3dx10savetexturetofile-function"></a>D3DX10SaveTextureToFile función)

Guardar una textura en un archivo.

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

*pSrcTexture* \[ de\]
</dt> <dd>

Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

Puntero a la textura que se va a guardar. Consulte la [**interfaz ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).

</dd> <dt>

*DestFormat* \[ de\]
</dt> <dd>

Tipo: **[ **\_ formato de \_ archivo \_ de imagen D3DX10**](d3dx10-image-file-format.md)**

El formato con el que se guardará la textura (consulte [**\_ formato de \_ archivo \_ de imagen D3DX10**](d3dx10-image-file-format.md)). D3DX10 \_ IFF \_ es el formato preferido, ya que es la única opción que admite todos los formatos en [**el \_ formato de DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).

</dd> <dt>

*pDestFile* \[ de\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Nombre del archivo de salida de destino en el que se guardará la textura. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos se resuelve como LPCSTR.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md). Use el valor devuelto para ver si se admite *DestFormat* .

## <a name="remarks"></a>Observaciones

**D3DX10SaveTextureToFile** escribe la estructura del [**encabezado DDS adicional \_ \_ DXT10**](../direct3ddds/dds-header-dxt10.md) para la textura de entrada solo si es necesario (por ejemplo, porque la textura de entrada está en formato RGB estándar (sRGB)). Si **D3DX10SaveTextureToFile** escribe la estructura **del \_ encabezado \_ DDS DXT10** , establece el miembro **DwFourCC** de la estructura [**de \_ PIXELFORMAT de DDS**](../direct3ddds/dds-pixelformat.md) para la textura en **contenido DX10** para indicar el prescense del **encabezado \_ DDS \_ DXT10** encabezado extendido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de textura en D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[Funciones de De uso general](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
