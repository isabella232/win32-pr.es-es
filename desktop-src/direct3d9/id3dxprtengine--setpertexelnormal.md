---
description: Establece un vector normal para cada elemento de textura de un objeto de textura. Este método se usa para almacenar vectores normales de vértice desde una malla (o normales de vértice interpolado si se está calculando la transferencia de radiancia precalentada (PRT) basada en píxeles).
ms.assetid: 165a3ef6-c142-4988-b4fb-5aafd8ff11fe
title: Método ID3DXPRTEngine::SetPerTexelNormal (D3DX9Mesh.h)
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
ms.openlocfilehash: 75877e8af86a22f80703742f148d5171e3a99e5c0c580bff588c27deba269b98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293379"
---
# <a name="id3dxprtenginesetpertexelnormal-method"></a>Método ID3DXPRTEngine::SetPerTexelNormal

Establece un vector normal para cada elemento de textura de un objeto de textura. Este método se usa para almacenar vectores normales de vértice desde una malla (o normales de vértice interpolado si se está calculando la transferencia de radiancia precalentada (PRT) basada en píxeles).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPerTexelNormal(
  [in] LPDIRECT3DTEXTURE9 pNormalTexture
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pNormalTexture* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Puntero a un [**objeto de textura IDirect3DTexture9**](/windows/desktop/api) que actúa como un mapa normal de espacio de objetos en el que almacenar vectores normales. La textura debe tener las mismas dimensiones que [**ID3DXPRTBuffer**](id3dxprtbuffer.md) y debe ser capaz de almacenar formatos de textura firmados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
