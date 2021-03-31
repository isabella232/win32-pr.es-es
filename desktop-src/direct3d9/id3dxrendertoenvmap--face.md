---
description: Inicia el dibujo de cada una de las caras de un mapa de entorno.
ms.assetid: c100e138-c5a8-49bb-9a91-e7f70410470f
title: 'ID3DXRenderToEnvMap:: facial (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.Face
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 452933c0d85a7aad2987011796ff47eff41dc32b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821482"
---
# <a name="id3dxrendertoenvmapface-method"></a>ID3DXRenderToEnvMap:: facial (método)

Inicia el dibujo de cada una de las caras de un mapa de entorno.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Face(
  [in] D3DCUBEMAP_FACES Face,
  [in] DWORD            MipFilter
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Caras* \[ de\]
</dt> <dd>

Tipo: **[ **D3DCUBEMAP \_ caras**](./d3dcubemap-faces.md)**

Primera superficie del mapa de cubo del entorno. Vea [**\_ caras de D3DCUBEMAP**](./d3dcubemap-faces.md).

</dd> <dt>

*MipFilter* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación válida de una o más marcas [de \_ filtro de D3DX](d3dx-filter.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Se debe llamar a este método una vez para cada tipo de asignación de entorno. La única excepción es un mapa de entorno cúbico que requiere que se llame a este método seis veces, una vez para cada cara de D3DCUBEMAP \_ caras. Para obtener más información, vea [asignación de entorno (Direct3D 9)](environment-mapping.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> </dl>

 

 
