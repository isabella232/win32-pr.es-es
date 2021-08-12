---
description: Calcula los coeficientes de transferencia de radiancia precalutables (LDPRT) de forma local en relación con los vectores normales por muestra para minimizar el error de mínimos cuadrados con respecto a los datos id3DXPRTBuffer de entrada.
ms.assetid: 302c20cd-d495-4a23-9692-7456355471eb
title: Método ID3DXPRTEngine::ComputeLDPRTCoeffs (D3DX9Mesh.h)
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
ms.openlocfilehash: a432f1df1ad905ca3200789aa6245212cc180d4c7ef5a8723cf02695aeeb7454
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118294045"
---
# <a name="id3dxprtenginecomputeldprtcoeffs-method"></a>Método ID3DXPRTEngine::ComputeLDPRTCoeffs

Calcula los coeficientes de transferencia de radiancia precalutables (LDPRT) de forma local en relación con los vectores normales por muestra para minimizar el error de mínimos cuadrados con respecto a los datos [**id3DXPRTBuffer**](id3dxprtbuffer.md) de entrada. Estos coeficientes se pueden usar con vectores normales desenlazados o transformados para modelar los efectos globales en objetos dinámicos.

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

*pDataIn* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto de datos de transferencia de radiancia precalutada (PRT) [**id3DXPRTBuffer**](id3dxprtbuffer.md) de entrada.

</dd> <dt>

*Pedido* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Orden de la evaluación de SH. Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos incluidos. La evaluación genera coeficientes order-to-order. El grado de la evaluación es Order - 1.

</dd> <dt>

*pNormOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Matriz de vectores opcional que se va a rellenar con vectores normales óptimos del sombreador para los que se optimizan los coeficientes LDPRT. Esta matriz debe tener el mismo tamaño que el número de muestras de pDataIn. Si **es NULL,** se usan vectores normales de superficie.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto [**ID3DXPRTBuffer de**](id3dxprtbuffer.md) salida que contiene coeficientes armónicos zonales order por canal de color por muestra.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

Opcionalmente, se pueden obtener soluciones para el sombreado de vectores normales con este método. Estos vectores normales, junto con los coeficientes LDPRT, pueden representar con más precisión la señal PRT. En este caso, los coeficientes representan armónicos zonales orientados en la dirección normal.

Este método no se puede usar con los resultados de [**ID3DXPRTEngine::ComputeSamplesBounce**](id3dxprtengine--computesurfsamplesbounce.md) o [**ID3DXPRTEngine::ComputeSamplesDirectSH.**](id3dxprtengine--computesurfsamplesdirectsh.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
