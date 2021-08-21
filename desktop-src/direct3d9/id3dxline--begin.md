---
description: Prepara un dispositivo para dibujar líneas.
ms.assetid: c597703d-6466-4b55-b1a6-a4e7c667e50c
title: Método ID3DXLine::Begin (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.Begin
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9daa65558c58849d406056ce3358c26fdf2ce1c604342f993babe6af553d130f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629655"
---
# <a name="id3dxlinebegin-method"></a>Método ID3DXLine::Begin

Prepara un dispositivo para dibujar líneas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Begin();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentarios

Llamar **a ID3DXLine::Begin** es opcional. Si se llama fuera de una secuencia ID3DXLine::Begin/ID3DXLine::End, las funciones draw llamarán internamente a ID3DXLine::Begin e ID3DXLine::End. Para evitar sobrecargas adicionales, se debe usar este método si se llamará sucesivamente a más de una función draw.

Se debe llamar a este método desde dentro de una secuencia [**IDirect3DDevice9::BeginScene**](/windows/desktop/api) [**e IDirect3DDevice9::EndScene.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene)

ID3DXLine::Begin no se puede usar como sustituto de [**IDirect3DDevice9::BeginScene**](/windows/desktop/api) o [**ID3DXRenderToSurface::BeginScene.**](id3dxrendertosurface--beginscene.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
