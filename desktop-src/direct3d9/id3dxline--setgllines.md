---
description: Alterna el modo para dibujar líneas de estilo OpenGL.
ms.assetid: 298bf391-9f2b-4352-b9f8-3bc2ab661eee
title: Método ID3DXLine::SetGLLines (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetGLLines
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bea46421cd259deb87bccaaf9e97073550467674491bba9e1983a7482686efd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748145"
---
# <a name="id3dxlinesetgllines-method"></a>Método ID3DXLine::SetGLLines

Alterna el modo para dibujar líneas de estilo OpenGL.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetGLLines(
  [in] BOOL bGLLines
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bGLLines* \[ En\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Alterna el dibujo de línea de estilo OpenGL. **TRUE** habilita las líneas de estilo OpenGL y **FALSE** habilita las líneas de estilo Direct3D.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
