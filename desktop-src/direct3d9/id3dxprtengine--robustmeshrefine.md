---
description: Subdivide las caras en una malla, lo que permite un muestreo adaptable conservador que no eliminará las características de la malla.
ms.assetid: 0d74a01a-de67-4607-99eb-ed98e239f199
title: Método ID3DXPRTEngine::RobustMeshRefine (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.RobustMeshRefine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 65d49fcec3072956365ce1ed8dc5d7a11ce6c826
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966696"
---
# <a name="id3dxprtenginerobustmeshrefine-method"></a>Método ID3DXPRTEngine::RobustMeshRefine

Subdivide las caras en una malla, lo que permite un muestreo adaptable conservador que no eliminará las características de la malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RobustMeshRefine(
  [in] FLOAT MinEdgeLength,
  [in] UINT  MaxSubdiv
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*MinEdgeLength* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Longitud mínima del borde de la cara que se generará en el muestreo adaptable. Si es cero, se sustituirá un valor predeterminado razonable.

</dd> <dt>

*MaxSubdiv* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Nivel máximo de subdivisión de una cara que se usará en el muestreo adaptable. Si es cero, se sustituirá un valor predeterminado de 5.

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
</dt> <dt>

[**ID3DXPRTEngine::ComputeBounceAdaptive**](id3dxprtengine--computebounceadaptive.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md)
</dt> </dl>

 

 
