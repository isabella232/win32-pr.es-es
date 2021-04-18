---
description: Establece un valor de Albedo para cada vértice de la malla, sobrescribiendo los valores de Albedo anteriores.
ms.assetid: 5220dfe3-8d41-480c-a850-b9aad3d2bb2f
title: 'ID3DXPRTEngine:: SetPerVertexAlbedo (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da7a33a79cc50963e87d0eff15baf22ee8d79ce3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649421"
---
# <a name="id3dxprtenginesetpervertexalbedo-method"></a>ID3DXPRTEngine:: SetPerVertexAlbedo (método)

Establece un valor de Albedo para cada vértice de la malla, sobrescribiendo los valores de Albedo anteriores.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPerVertexAlbedo(
  [in] const VOID *pDataIn,
  [in]       UINT NumChannels,
  [in]       UINT Stride
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDataIn* \[ de\]
</dt> <dd>

Tipo: **const void \***

Puntero a FLOAT Albedo data del primer ejemplo.

</dd> <dt>

*NumChannels* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de canales de color que se van a establecer. Establézcalo en 1 para especificar materiales grises (R = G = B) o 3 para habilitar los efectos de sangrado de color.

</dd> <dt>

*STRIDE* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

STRIDE en bytes necesario para obtener el valor de albedo del siguiente ejemplo. Vea [ancho frente a paso (Direct3D 9)](width-vs--pitch.md).

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

 

 
