---
description: Restaure todos los destinos de representación y, si es necesario, cree todas las caras representados en la superficie del mapa del entorno.
ms.assetid: 57c73787-36e7-4088-b5ff-78894e3a5d90
title: Método ID3DXRenderToEnvMap::End (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 20e62a9d794738ae81ae84a665165f6034958f0c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974755"
---
# <a name="id3dxrendertoenvmapend-method"></a>Método ID3DXRenderToEnvMap::End

Restaure todos los destinos de representación y, si es necesario, cree todas las caras representados en la superficie del mapa del entorno.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT End(
  [in] DWORD MipFilter
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*MipFilter* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación válida de una o varias [marcas D3DX \_ FILTER.](d3dx-filter.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> <dt>

[**ID3DXRenderToEnvMap::Face**](id3dxrendertoenvmap--face.md)
</dt> </dl>

 

 
