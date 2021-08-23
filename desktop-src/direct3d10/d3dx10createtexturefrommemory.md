---
description: Cree un recurso de textura a partir de un archivo que resida en la memoria del sistema.
ms.assetid: 63eac44b-0540-457f-96c0-d151fbd44df0
title: Función D3DX10CreateTextureFromMemory (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateTextureFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7b64c3c429ef356fa4ab8c206682c3b1711a14fe29ee6b2024b92b8113951062
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753355"
---
# <a name="d3dx10createtexturefrommemory-function"></a>Función D3DX10CreateTextureFromMemory

Cree un recurso de textura a partir de un archivo que resida en la memoria del sistema.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10CreateTextureFromMemory(
  _In_  ID3D10Device           *pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  SIZE_T                 SrcDataSize,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX10ThreadPump      *pPump,
  _Out_ ID3D10Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Puntero al dispositivo (consulte [**ID3D10Device Interface)**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)que usará el recurso.

</dd> <dt>

*pSrcData* \[ En\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntero al recurso en la memoria del sistema.

</dd> <dt>

*SrcDataSize* \[ En\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

Tamaño del recurso en la memoria del sistema.

</dd> <dt>

*pLoadInfo* \[ En\]
</dt> <dd>

Tipo: **[ **D3DX10 \_ IMAGE \_ LOAD \_ INFO**](d3dx10-image-load-info.md)\***

Opcional. Identifica las características de una textura (vea [**D3DX10 \_ IMAGE \_ LOAD \_ INFO**](d3dx10-image-load-info.md)) cuando se crea el procesador de datos; esta opción se establece en **NULL** para leer las características de una textura cuando se carga la textura.

</dd> <dt>

*pPump* \[ En\]
</dt> <dd>

Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Puntero a una interfaz de bombeo de subprocesos (vea [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)). Si se especifica **NULL,** esta función se comportará sincrónicamente y no volverá hasta que finalice.

</dd> <dt>

*ppTexture* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***

Dirección de un puntero al recurso creado. Vea [**ID3D10Resource (Interfaz).**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntero al valor devuelto. Puede ser **NULL.** Si *pPump* no es **NULL,** *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios

Para obtener una lista de los formatos de imagen admitidos, [**vea D3DX10 \_ IMAGE FILE \_ \_ FORMAT**](d3dx10-image-file-format.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de textura en D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[De uso general functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
