---
description: Establece las propiedades de muestreo utilizadas por el simulador Radiance Transfer (PRT) precalculado.
ms.assetid: a33963a7-fbcb-4e1c-a4f3-fb20a99fcf9f
title: 'ID3DXPRTEngine:: SetSamplingInfo (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetSamplingInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ab229652fe9e333519acce7d8474d3c4f0cf7ef9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821191"
---
# <a name="id3dxprtenginesetsamplinginfo-method"></a>ID3DXPRTEngine:: SetSamplingInfo (método)

Establece las propiedades de muestreo utilizadas por el simulador Radiance Transfer (PRT) precalculado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetSamplingInfo(
  [in] UINT  NumRays,
  [in] BOOL  UseSphere,
  [in] BOOL  UseCosine,
  [in] BOOL  Adaptive,
  [in] FLOAT AdaptiveThresh
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NumRays* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de rayos de luz que se dirigen a cada ejemplo. Debe ser mayor que cero.

</dd> <dt>

*UseSphere* \[ de\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Si **es true**, los ejemplos se calcularán en una esfera completa. Si **es false**, los ejemplos se calcularán sobre un hemisferio.

</dd> <dt>

*UseCosine* \[ de\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Si **es true**, se usa una ponderación de muestras de coseno. Si tanto UseCosine como UseSphere son **true**, se producirá un error en el método y se devolverá un error.

</dd> <dt>

*Adaptable* \[ de\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Debe ser **false**. El muestreo adaptable no está implementado actualmente.

</dd> <dt>

*AdaptiveThresh* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

ignorado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, e \_ NOTIMPL e \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
