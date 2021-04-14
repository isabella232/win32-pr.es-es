---
description: Establece un vector normal para cada textura de un objeto Texture. Este método se usa para almacenar vectores normales de vértices de una malla (o normales de vértice interpolados si se está calculando la transferencia de Radiance precalculada basada en píxeles).
ms.assetid: 165a3ef6-c142-4988-b4fb-5aafd8ff11fe
title: 'ID3DXPRTEngine:: SetPerTexelNormal (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerTexelNormal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5220ad500312792cd158967e9502381f49b0e3e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424432"
---
# <a name="id3dxprtenginesetpertexelnormal-method"></a>ID3DXPRTEngine:: SetPerTexelNormal (método)

Establece un vector normal para cada textura de un objeto Texture. Este método se usa para almacenar vectores normales de vértices de una malla (o normales de vértice interpolados si se está calculando la transferencia de Radiance precalculada basada en píxeles).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPerTexelNormal(
  [in] LPDIRECT3DTEXTURE9 pNormalTexture
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pNormalTexture* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Puntero a un objeto de textura [**IDirect3DTexture9**](/windows/desktop/api) que actúa como mapa normal de espacio de objeto en el que se almacenan los vectores normales. La textura debe tener las mismas dimensiones que [**ID3DXPRTBuffer**](id3dxprtbuffer.md) y debe poder almacenar formatos de textura firmados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
