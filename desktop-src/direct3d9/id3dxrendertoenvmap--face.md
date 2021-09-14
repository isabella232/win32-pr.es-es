---
description: Inicie el dibujo de cada cara de un mapa de entorno.
ms.assetid: c100e138-c5a8-49bb-9a91-e7f70410470f
title: Método ID3DXRenderToEnvMap::Face (D3dx9core.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966655"
---
# <a name="id3dxrendertoenvmapface-method"></a>Método ID3DXRenderToEnvMap::Face

Inicie el dibujo de cada cara de un mapa de entorno.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Face(
  [in] D3DCUBEMAP_FACES Face,
  [in] DWORD            MipFilter
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Face* \[ En\]
</dt> <dd>

Tipo: **[ **CARAS de \_ D3DCUBEMAP**](./d3dcubemap-faces.md)**

Primera cara del mapa del cubo ambiental. Vea [**D3DCUBEMAP \_ FACES**](./d3dcubemap-faces.md).

</dd> <dt>

*MipFilter* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación válida de una o varias [marcas D3DX \_ FILTER.](d3dx-filter.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Se debe llamar a este método una vez para cada tipo de mapa de entorno. La única excepción es un mapa de entorno cúbica que requiere que se llame a este método seis veces, una vez por cada cara de D3DCUBEMAP \_ FACES. Para obtener más información, vea [Asignación de entorno (Direct3D 9).](environment-mapping.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> </dl>

 

 
