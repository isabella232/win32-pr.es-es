---
description: Establece las propiedades de muestreo utilizadas por el simulador de transferencia de radiancia precalcalada (PRT).
ms.assetid: a33963a7-fbcb-4e1c-a4f3-fb20a99fcf9f
title: Método ID3DXPRTEngine::SetSamplingInfo (D3DX9Mesh.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476060"
---
# <a name="id3dxprtenginesetsamplinginfo-method"></a>Método ID3DXPRTEngine::SetSamplingInfo

Establece las propiedades de muestreo utilizadas por el simulador de transferencia de radiancia precalcalada (PRT).

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

*NumRays* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de rayos de luz que se dirigen a cada muestra. Debe ser mayor que cero.

</dd> <dt>

*Uso deSphere* \[ En\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Si **es TRUE,** las muestras se calcularán en una esfera completa. Si **es FALSE,** las muestras se calcularán en un hemisferio.

</dd> <dt>

*UseCosine* \[ En\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Si **es TRUE,** use una ponderación de coseno de muestras. Si UseCosine y UseSphere son **TRUE,** se producirá un error en el método y se devolverá un error.

</dd> <dt>

*Adaptable* \[ En\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Debe ser **FALSE.** El muestreo adaptable no está implementado actualmente.

</dd> <dt>

*AdaptiveThresh* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

ignorado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ NOTIMPL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
