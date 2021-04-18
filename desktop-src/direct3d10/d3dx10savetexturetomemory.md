---
description: Guardar una textura en la memoria.
ms.assetid: be541b99-6d07-480e-8f28-b7fc44566e7d
title: Función D3DX10SaveTextureToMemory (D3DX10Tex. h)
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
ms.openlocfilehash: f20278f9fc590e72f93051d5fdd4cfbd918098df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698270"
---
# <a name="d3dx10savetexturetomemory-function"></a>D3DX10SaveTextureToMemory función)

Guardar una textura en la memoria.

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

*pSrcTexture* \[ de\]
</dt> <dd>

Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

Puntero a la textura que se va a guardar. Consulte la [**interfaz ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).

</dd> <dt>

*DestFormat* \[ de\]
</dt> <dd>

Tipo: **[ **\_ formato de \_ archivo \_ de imagen D3DX10**](d3dx10-image-file-format.md)**

Formato en el que se guardará la textura. Consulte [**\_ formato de \_ archivo \_ de imagen D3DX10**](d3dx10-image-file-format.md).

</dd> <dt>

*ppDestBuf* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***

Dirección de un puntero a la memoria que contiene la textura guardada. Consulte la [**interfaz ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob).

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Opcional.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).

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

 

 
