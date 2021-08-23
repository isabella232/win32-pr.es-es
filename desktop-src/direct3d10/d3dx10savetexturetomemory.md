---
description: Guarde una textura en la memoria.
ms.assetid: be541b99-6d07-480e-8f28-b7fc44566e7d
title: Función D3DX10SaveTextureToMemory (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SaveTextureToMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3736b2de21df3e77f5b06d34f2b0b64a7592f2212a71ffd4a37b70454667427a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047063"
---
# <a name="d3dx10savetexturetomemory-function"></a>Función D3DX10SaveTextureToMemory

Guarde una textura en la memoria.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10SaveTextureToMemory(
  _In_  ID3D10Resource           *pSrcTexture,
  _In_  D3DX10_IMAGE_FILE_FORMAT DestFormat,
  _Out_ LPD3D10BLOB              *ppDestBuf,
  _In_  UINT                     Flags
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

Formato con el que se guardará la textura. Vea [**FORMATO DE ARCHIVO DE IMAGEN \_ \_ \_ D3DX10.**](d3dx10-image-file-format.md)

</dd> <dt>

*ppDestBuf* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***

Dirección de un puntero a la memoria que contiene la textura guardada. Vea [**ID3D10Blob (Interfaz).**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)

</dd> <dt>

*Marcas* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Opcional.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de textura en D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[De uso general Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
