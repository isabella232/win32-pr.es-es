---
description: Establece las propiedades de material de malla en la escena 3D. Use este método para especificar parámetros de dispersión de subsuelo.
ms.assetid: 830d73be-bba6-454d-8476-341d291a5b2e
title: Método ID3DXPRTEngine::SetMeshMaterials (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetMeshMaterials
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c90ae72cab5d7a20c2c65b940d28a9b57902d2d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966688"
---
# <a name="id3dxprtenginesetmeshmaterials-method"></a>Método ID3DXPRTEngine::SetMeshMaterials

Establece las propiedades de material de malla en la escena 3D. Use este método para especificar parámetros de dispersión de subsuelo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetMeshMaterials(
  [in] const D3DXSHMATERIAL **ppMaterials,
  [in]       UINT           NumMeshes,
  [in]       UINT           NumChannels,
  [in]       BOOL           bSetAlbedo,
  [in]       FLOAT          fLengthScale
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppMaterials* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXSHMATERIAL**](d3dxshmaterial.md) \* \***

Dirección de un puntero a las propiedades de material de malla deseadas. Vea [**D3DXSHMATERIAL.**](d3dxshmaterial.md)

</dd> <dt>

*NumMeshes* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice de la malla en la que se establecen las propiedades de material.

</dd> <dt>

*NumChannels* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de canales de color que se establecerán en la malla. Establezca en 1 para especificar materiales grises (R = G = B) o 3 para habilitar los efectos de color. Si tiene previsto cambiar este parámetro, primero establezca albedo mediante otro método como [**ID3DXPRTEngine::SetPerTexelAlbedo**](id3dxprtengine--setpertexelalbedo.md) o [**ID3DXPRTEngine::SetPerVertexAlbedo**](id3dxprtengine--setpervertexalbedo.md).

</dd> <dt>

*bSetAlbedo* \[ En\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Si **es TRUE,** establece el albedo de la malla en ppMaterials, sobrescribiendo todos los valores de albedo de vértice y texel existentes. Si **es FALSE,** conserva todos los valores de albedo de vértice y texel existentes establecidos por otros métodos; NumChannels debe coincidir con el parámetro NumChannels usado para crear el búfer en [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) o [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md).

</dd> <dt>

*fLengthScale* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Escala de la escena 3D con respecto a un cubo de 1 mm. Se usa para cálculos de dispersión de subsuelo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
