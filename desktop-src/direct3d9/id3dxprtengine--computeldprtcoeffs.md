---
description: Calcula los coeficientes de transferencia de Radiance precalculados (LDPRT) precalculados de forma local en relación con los vectores normales de cada muestra para minimizar el error de menos cuadrados con respecto a los datos de ID3DXPRTBuffer de entrada.
ms.assetid: 302c20cd-d495-4a23-9692-7456355471eb
title: 'ID3DXPRTEngine:: ComputeLDPRTCoeffs (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeLDPRTCoeffs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 351ecb8022e06b1a5a24abad8fa8541798d13ba0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718550"
---
# <a name="id3dxprtenginecomputeldprtcoeffs-method"></a>ID3DXPRTEngine:: ComputeLDPRTCoeffs (método)

Calcula los coeficientes de transferencia de Radiance precalculados (LDPRT) precalculados de forma local en relación con los vectores normales de cada muestra para minimizar el error de menos cuadrados con respecto a los datos de [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada. Estos coeficientes se pueden usar con vectores normales con o sin máscaras para modelar los efectos globales en los objetos dinámicos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ComputeLDPRTCoeffs(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      UINT            Order,
  [in, out] D3DXVECTOR3     *pNormOut,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDataIn* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto de datos de Radiance (PRT) precalculado [**ID3DXPRTBuffer**](id3dxprtbuffer.md) esférico (SH) de entrada.

</dd> <dt>

*Pedido* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Orden de la evaluación de SH. Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos incluidos. La evaluación genera coeficientes de pedido ². El grado de evaluación es order-1.

</dd> <dt>

*pNormOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Matriz vector opcional que se va a rellenar con vectores normales de sombreador óptimo para los que se optimizan los coeficientes de LDPRT. Esta matriz debe tener el mismo tamaño que el número de muestras de pDataIn. Si **es null**, se usan vectores normales de superficie.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de salida que contiene los coeficientes armónicos de orden de pedido por canal de color por muestra.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Las soluciones para los vectores normales de sombreado se pueden obtener opcionalmente con este método. Estos vectores normales, junto con los coeficientes de LDPRT, pueden representar con mayor precisión la señal de PRT. En este caso, los coeficientes representan armónicos de zona orientados en la dirección normal.

Este método no se puede usar con los resultados de [**ID3DXPRTEngine:: ComputeSurfSamplesBounce**](id3dxprtengine--computesurfsamplesbounce.md) o [**ID3DXPRTEngine:: ComputeSurfSamplesDirectSH**](id3dxprtengine--computesurfsamplesdirectsh.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
