---
title: Función D3DX11CreateAsyncTextureInfoProcessor (D3DX11tex.h)
description: Nota La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store. Vea la sección Comentarios. Cree un procesador de datos que se usará con una bomba de subprocesos. | Función D3DX11CreateAsyncTextureInfoProcessor (D3DX11tex.h)
ms.assetid: 87de73a5-21f7-4abd-b83a-65c6761681c3
keywords:
- Función D3DX11CreateAsyncTextureInfoProcessor Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncTextureInfoProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aac60b1d496e0f1d4ecb604b18a8ef71cac8b5d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566280"
---
# <a name="d3dx11createasynctextureinfoprocessor-function"></a>Función D3DX11CreateAsyncTextureInfoProcessor

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store. Vea la sección Comentarios.

 

Cree un procesador de datos que se usará con una bomba [**de subprocesos**](id3dx11threadpump.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX11CreateAsyncTextureInfoProcessor(
  _In_  D3DX11_IMAGE_INFO    *pImageInfo,
  _Out_ ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pImageInfo* \[ En\]
</dt> <dd>

Tipo: **[ **D3DX11 \_ IMAGE \_ INFO**](d3dx11-image-info.md)\***

Opcional. Identifica las características de una textura (vea [**D3DX11 \_ IMAGE \_ INFO**](d3dx11-image-info.md)) cuando se crea el procesador de datos; esta opción se establece en **NULL** para leer las características de una textura cuando se carga la textura.

</dd> <dt>

*ppDataProcessor* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***

Dirección de un puntero a un búfer que contiene el procesador de datos creado (vea [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno [de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Observaciones

Esta API crea una interfaz de procesador de datos; [**D3DX11CreateAsyncTextureProcessor crea**](d3dx11createasynctextureprocessor.md) la interfaz del procesador de datos y carga la textura.

No hay ninguna implementación del cargador asincrónico fuera de D3DX 10 y D3DX 11.

Para Windows Store, los ejemplos de DirectX (por ejemplo, el [ejemplo de tutorial de Direct3D)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)incluyen el módulo **BasicLoader** que usa el modelo de programación asincrónica de Windows Runtime [**(AsyncBase).**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))

En el caso de las aplicaciones de escritorio Win32, puede usar el Runtime de simultaneidad [para](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) implementar algo similar al modelo de programación asincrónica de Windows Runtime.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX11tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11.lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

