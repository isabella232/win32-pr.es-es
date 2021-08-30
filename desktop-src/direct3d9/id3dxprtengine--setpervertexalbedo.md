---
description: Establece un valor albedo para cada vértice de malla, sobrescribiendo los valores anteriores de albedo.
ms.assetid: 5220dfe3-8d41-480c-a850-b9aad3d2bb2f
title: Método ID3DXPRTEngine::SetPerVertexAlbedo (D3DX9Mesh.h)
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
ms.openlocfilehash: d40c91ea00be7b1194099764c3c6d029a9cacb10d5265fb560053b093f396c9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095835"
---
# <a name="id3dxprtenginesetpervertexalbedo-method"></a>Método ID3DXPRTEngine::SetPerVertexAlbedo

Establece un valor albedo para cada vértice de malla, sobrescribiendo los valores anteriores de albedo.

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

*pDataIn* \[ En\]
</dt> <dd>

Tipo: **const \* VOID**

Puntero a datos float albedo del primer ejemplo.

</dd> <dt>

*NumChannels* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de canales de color que se establecerán. Establezca en 1 para especificar materiales grises (R = G = B) o 3 para habilitar los efectos de color.

</dd> <dt>

*Stride* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Stride en bytes necesarios para llegar al siguiente valor de albedo de la muestra. Vea [Width frente a Pitch (Direct3D 9).](width-vs--pitch.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
