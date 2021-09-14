---
title: Función D3DX11SaveTextureToMemory (D3DX11tex.h)
description: Nota La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store. Nota En lugar de usar esta función, se recomienda usar la biblioteca DirectXTex, CaptureTexture y SaveToXXXMemory (donde XXX es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admite TGA como un formato de origen de arte común para juegos). Guarde una textura en la memoria.
ms.assetid: 3b54d8e1-6474-48fd-8348-a3baac406101
keywords:
- Función D3DX11SaveTextureToMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SaveTextureToMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4718f32f8d8288f83b30e3d742ebbe619421dc48
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060846"
---
# <a name="d3dx11savetexturetomemory-function"></a>Función D3DX11SaveTextureToMemory

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.

 

> [!Note]  
> En lugar de usar esta función, se recomienda usar la biblioteca [DirectXTex,](https://github.com/Microsoft/DirectXTex) **CaptureTexture** y **SaveToXXXMemory** (donde XXX es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admite TGA como un formato de origen de arte común para juegos).

 

Guarde una textura en la memoria.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX11SaveTextureToMemory(
        ID3D11DeviceContext      *pContext,
  _In_  ID3D11Resource           *pSrcTexture,
  _In_  D3DX11_IMAGE_FILE_FORMAT DestFormat,
  _Out_ LPD3D10BLOB              *ppDestBuf,
  _In_  UINT                     Flags
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

Formato con el que se guardará la textura. Vea FORMATO DE ARCHIVO DE [**\_ IMAGEN \_ \_ D3DX11.**](d3dx11-image-file-format.md)

</dd> <dt>

*ppDestBuf* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3D10BLOB**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\***

Dirección de un puntero a la memoria que contiene la textura guardada.

</dd> <dt>

*Marcas* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Opcional.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno [de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX11tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11.lib</dt> </dl>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

