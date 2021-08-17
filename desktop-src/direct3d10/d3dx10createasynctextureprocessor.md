---
description: 'Función D3DX10CreateAsyncTextureProcessor: cree un procesador de datos que se usará con una bomba de subprocesos.'
ms.assetid: c96b0ebb-7b9c-47d0-ad4f-fa62ddb74fa1
title: Función D3DX10CreateAsyncTextureProcessor (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncTextureProcessor
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d245a96181e194479b0c5e115b3b3aea89096da8176713047578a93264e470da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852365"
---
# <a name="d3dx10createasynctextureprocessor-function"></a>Función D3DX10CreateAsyncTextureProcessor

Cree un procesador de datos que se usará con una bomba [**de subprocesos**](id3dx10threadpump.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10CreateAsyncTextureProcessor(
  _In_  ID3D10Device           *pDevice,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Puntero a la interfaz devive [**(vea ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)).

</dd> <dt>

*pLoadInfo* \[ En\]
</dt> <dd>

Tipo: **[ **D3DX10 \_ IMAGE \_ LOAD \_ INFO**](d3dx10-image-load-info.md)\***

Opcional. Identifica las características de una textura (vea [**D3DX10 \_ IMAGE \_ LOAD \_ INFO**](d3dx10-image-load-info.md)) cuando se crea el procesador de datos; esta opción se establece en **NULL** para leer las características de una textura cuando se carga la textura.

</dd> <dt>

*ppDataProcessor* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***

Dirección de un puntero a un búfer que contiene el procesador de datos creado (vea [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios

Esta API crea una interfaz de procesador de datos y carga la textura; [**D3DX10CreateAsyncTextureInfoProcessor crea**](d3dx10createasynctextureinfoprocessor.md) la interfaz del procesador de datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de textura en D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




